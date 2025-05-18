# KMRservice - Lightweight Background Screen Recorder

**KMRservice** is a minimal screen recording utility written in Python, designed to run silently in the background with very low resource usage. It captures your screen continuously and saves the recordings in manageable chunks.

## Features

- 🖥️ Records the primary monitor continuously
- 🔁 Automatically creates a new video file every 10 minutes (or configurable)
- 🧹 Deletes oldest files when total folder size exceeds a defined limit
- 🕵️ Runs in the background without a console window (when built with `--noconsole`)
- 📁 Stores recordings in a user-accessible folder:  
  `%LOCALAPPDATA%\KMRservice`
- ⚙️ No admin privileges required

## Installation

1. **Install dependencies** (Python ≥ 3.8 required):

    ```bash
    pip install opencv-python mss numpy
    ```

2. **Run the script**:

    ```bash
    python KMRservice.py
    ```

3. *(Optional)* **Build to `.exe` for distribution**:

    ```bash
    pyinstaller --onefile --noconsole KMRservice.py
    ```

    This creates a standalone executable in the `dist/` folder.

## Configuration

- `max_duration`: Duration of each video file (default: 10 minutes)
- `max_folder_size`: Maximum total size of recordings (default: 1GB)

You can change both in the script directly.

## Folder Structure

All recordings are saved to:
