# video-compress-to-2-minutes

This repository contains a Jupyter notebook for removing audio from a video and compressing the video length so it fits into 2 minutes.

## File

- `video-compress.ipynb` — notebook used to process a video so the final output is 2 minutes long

## What it does

The notebook:

- loads a video file
- checks the original video duration
- removes the audio
- speeds up or adjusts the video to fit a 2 minute target length
- saves the processed video as a new file

## Requirements

You need:

- Python 3
- FFmpeg
- FFprobe

`ffprobe` usually comes with FFmpeg.

## Python libraries used

This notebook only uses standard Python libraries:

- `pathlib`
- `subprocess`
- `json`

No extra Python packages need to be installed for this notebook.

## Important note

The notebook may contain Mac-specific FFmpeg paths such as:

```python
ffmpeg_path="/opt/homebrew/opt/ffmpeg-full/bin/ffmpeg"
ffprobe_path="/opt/homebrew/opt/ffmpeg-full/bin/ffprobe"
```

If FFmpeg is already installed and available in terminal, these can be changed to:

```python
ffmpeg_path="ffmpeg"
ffprobe_path="ffprobe"
```

## How to use

1. Open `video-compress.ipynb` in Jupyter Notebook or VS Code.
2. Make sure FFmpeg and FFprobe are installed.
3. Update the input video filename in the notebook.
4. Run the notebook cells from top to bottom.
5. The notebook will create a new video file with no audio and a duration adjusted to 2 minutes.

## Output

The output video is saved as a new file, usually with a name similar to:

```text
your_video_2min_noaudio.mp4
```

## Summary

This notebook is a simple tool for turning a longer video into a silent 2 minute version.
