# PictureHandle

## Web UI (NextUI / HeroUI)
- Backend: `run_backend.ps1` (Python 3.12)
- Frontend: `cd web` -> `npm install` -> `npm run electron:dev`
- Build backend: `build_backend.ps1`
- Build app: `cd web` -> `npm run electron:build`

桌面小工具：支持图片高清放大、指定尺寸压缩、格式转换，以及一键抠图（rembg）。界面基于 PySide6，风格现代。

## 功能
- 高清放大：高质量（Lanczos）放大 1-6 倍。
- 尺寸缩放：可设定目标宽/高，支持保持比例或自由缩放。
- 格式转换：在 PNG/JPEG/WEBP/原格式间切换。
- 抠图：调用 rembg 移除背景。
- 批量：列表中可多选或全部处理。

## 环境要求
- Python 3.10+
- Windows / macOS / Linux

## 安装
```bash
python -m venv .venv
.\.venv\Scripts\activate  # Windows
# source .venv/bin/activate # macOS/Linux
pip install -r requirements.txt
```
首次使用抠图功能时，rembg 会自动下载模型，需保持网络可用。

## 运行
```bash
python -m src.app
```

## 使用提示
- 放大倍数和目标尺寸可同时设置：先放大后再按目标尺寸收敛。
- 目标宽/高为 0 表示保持原值；勾选“保持比例”以按最小边适配。
- 输出目录留空则写回原目录，文件名追加 `_processed`。

## 项目结构
- `src/app.py`：应用入口。
- `src/ui/main_window.py`：界面与交互逻辑。
- `src/processing.py`：图片处理逻辑（放大、缩放、格式转换、抠图）。
- `src/style.qss`：界面样式。

## 后续改进想法
- 增加进度条与任务队列。
- 支持实时对比预览。
- 接入更高质量的超分模型（如 Real-ESRGAN）。
