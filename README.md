# Custom Avatar Generator

This project generates a talking head animation from text input. It converts text to phonemes, maps phonemes to visemes, generates a TTS audio file, detects silent segments in the audio, and stitches together video clips of visemes to create a talking head video synchronized with the audio.

## Features

- Convert text to phonemes using the `eng_to_ipa` library.
- Map phonemes to visemes.
- Generate TTS audio using the `edge_tts` library.
- Detect silent segments in the audio using the `pydub` library.
- Create a video from visemes using the `moviepy` library.

## Requirements
- Python 3.x
- `eng_to_ipa`
- `moviepy`
- `pydub`
- `edge_tts`
- `asyncio`
- `opencv-python`

## Installation

1. **Clone the repository:**
    ```sh
    git clone https://github.com/yourusername/talking-head-animation.git
    cd talking-head-animation
    ```

2. **Install Python dependencies:**
    ```sh
    pip install -r requirements.txt
    ```

3. **Install `ffmpeg`:**

    - **Windows:**
        Download the `ffmpeg` executable from [ffmpeg.org](https://ffmpeg.org/download.html), extract it, and add the `bin` folder to your system's PATH.

    - **macOS:**
        ```sh
        brew install ffmpeg
        ```

    - **Linux:**
        ```sh
        sudo apt update
        sudo apt install ffmpeg
        ```
    
4. Increase open file limit:
```bash
ulimit -n 4096
```

## Usage
Update the phrase variable in the example usage section of the `main.py` with the text you want to convert to a talking head video. Run the script:
```bash
python main.py
```
The generated video will be saved as `talking_head.mp4`.