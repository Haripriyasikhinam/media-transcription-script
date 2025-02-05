# Media Transcription Project

This project is a Python script that scans a directory for media files (audio/video), transcribes them using OpenAI Whisper, and saves the results in a structured format.

## Features
- Automatically detects media files in the specified directory.
- Uses OpenAI Whisper for high-quality transcription.
- Saves transcriptions in structured text files.

## Installation
### 1. Clone the Repository
```bash
git clone https://github.com/your-username/media-transcription-project.git
cd media-transcription-project
```

### 2. Create a Virtual Environment (Optional but Recommended)
```bash
python -m venv venv
source venv/bin/activate  # On Windows, use: venv\Scripts\activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Install FFmpeg (Required for Whisper)
- **Windows**: Download from [https://www.gyan.dev/ffmpeg/builds/](https://www.gyan.dev/ffmpeg/builds/), extract, and add to PATH.
- **Linux/macOS**: Install via package manager:
  ```bash
  sudo apt install ffmpeg  # Ubuntu/Debian
  brew install ffmpeg      # macOS
  ```

## Usage
1. **Place media files in the `input_media/` directory.**
2. **Run the transcription script:**
   ```bash
   python transcribe.py
   ```
3. **Check the `output/` folder for transcriptions.**

## Troubleshooting
### 1. "Error: No such file or directory"
- Ensure the file exists in `input_media/`.
- Use absolute paths instead of relative paths.

### 2. "Failed to load audio: FFmpeg error"
- Make sure FFmpeg is installed and correctly added to PATH.
- Convert the file manually:
  ```bash
  ffmpeg -i input_media/file.mp3 -ac 1 -ar 16000 input_media/file_fixed.wav
  ```
  Then retry transcription with `file_fixed.wav`.

## Contributing
Pull requests are welcome! If you find any issues, please open an issue on GitHub.



