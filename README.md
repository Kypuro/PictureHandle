# Picture Handle Studio

[中文说明](README.zh-CN.md)

Picture Handle Studio is a desktop application built with PySide6 and Python, designed for common image processing tasks. It provides a user-friendly interface for operations such as image resizing, upscaling, and background removal.

## Features

*   **Image Resizing**: Resize images by specifying exact dimensions or scaling percentage. Includes options to maintain aspect ratio.
*   **Image Upscaling**: Enhance image resolution using interpolation methods.
*   **Background Removal**: Automatically remove image backgrounds using the `rembg` library, with support for various models and alpha matting options.
*   **Image Format Conversion**: Convert images to different formats (PNG, JPEG, WEBP).
*   **Batch Processing**: Process multiple images at once.

## Installation

To set up and run Picture Handle Studio locally, follow these steps:

1.  **Clone the repository**:
    ```bash
    git clone https://github.com/Kypuro/PictureHandle.git
    cd PictureHandle
    ```

2.  **Create and activate a virtual environment** (recommended):
    ```bash
    python -m venv .venv
    # On Windows
    .venv\Scripts\activate
    # On macOS/Linux
    source .venv/bin/activate
    ```

3.  **Install dependencies**:
    ```bash
    pip install -r requirements.txt
    ```
    Note: The `rembg` library (a dependency) may require `onnxruntime` which currently does not support Python 3.14+. If you encounter issues, consider using Python 3.12 or earlier.

## Usage

To run the application:

```bash
python src/app.py
```

## Planned Features (Coming Soon)

*   **Screenshot Dimension Capture**: Easily grab dimensions directly from screen selections for resizing.
*   **Common Size Presets**: Quick selection for standard image dimensions (e.g., 1920x1080, 1280x720).
*   **Live Preview**: Real-time preview of resized/processed images before final output.
*   **Custom Output Directory Selection**: Enhanced UI for easily choosing and managing output folders.

## Project Structure

- `src/app.py`: Application entry point.
- `src/ui/main_window.py`: User interface and interaction logic.
- `src/processing.py`: Image processing logic (upscaling, resizing, format conversion, background removal).
- `src/style.qss`: UI styles.

## Contributing

Contributions are welcome! Please feel free to open issues or submit pull requests.

## License

[Add License Information Here, e.g., MIT License]
