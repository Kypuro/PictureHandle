# Picture Handle Studio

[English README](README.md)

Picture Handle Studio 是一款基于 PySide6 和 Python 的桌面应用，面向常见图片处理场景，提供更直观的批量处理界面。

## 功能

- 图片缩放：支持指定宽高或按百分比缩放，可选择保持比例。
- 高清放大：使用插值算法提升分辨率。
- 智能抠图：基于 `rembg` 自动移除背景，支持多模型与 Alpha Matting。
- 格式转换：支持 PNG、JPEG、WEBP 等格式。
- 批量处理：可一次处理多张图片。

## 安装

1. 克隆仓库：
   ```bash
   git clone https://github.com/Kypuro/PictureHandle.git
   cd PictureHandle
   ```

2. 创建并激活虚拟环境（推荐）：
   ```bash
   python -m venv .venv
   # Windows
   .venv\Scripts\activate
   # macOS/Linux
   source .venv/bin/activate
   ```

3. 安装依赖：
   ```bash
   pip install -r requirements.txt
   ```
   注意：`rembg` 依赖 `onnxruntime`，目前不支持 Python 3.14+。如有问题，请使用 Python 3.12 或更低版本。

## 使用

```bash
python src/app.py
```

## 规划功能（近期）

- 屏幕选区尺寸获取：从截图选区快速填充尺寸。
- 常用尺寸预设：常见尺寸一键选择。
- 实时预览：处理前预览缩放或效果。
- 输出目录选择优化：更直观的路径选择与展示。

## 项目结构

- `src/app.py`：应用入口。
- `src/ui/main_window.py`：界面与交互逻辑。
- `src/processing.py`：图片处理逻辑（放大、缩放、格式转换、抠图）。
- `src/style.qss`：界面样式。

## 贡献

欢迎提交 Issue 或 PR。

## License

[待补充，例如 MIT License]
