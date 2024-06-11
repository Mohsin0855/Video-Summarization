# Video-Summarization
This tool processes local video files by extracting audio, chunking the audio into manageable segments, transcribing the audio into text, and summarizing the transcriptions. The entire workflow is designed to handle large video files and provide concise summaries of their content.
# Features
- Extracts audio from video files.
- Chunks audio into specified segment lengths.
- Transcribes audio segments into text using OpenAI's Whisper model.
- Summarizes the transcriptions using OpenAI's GPT-3.5-turbo model.
# Requirements
- Python 3.7 or higher
- librosa
- openai
- soundfile
- shutil
- os
# Installation
Install the required Python libraries using pip:
``` bash
pip install librosa openai soundfile
```
# Setup
**Set up your OpenAI API key:**
Replace the placeholder in the code with your actual OpenAI API key.
``` bash
os.environ["OPENAI_API_KEY"] = "your_openai_api_key_here"
openai.api_key = os.getenv("OPENAI_API_KEY")
```

# Usage
- Place your video file in a desired directory.
- Set the video_file_path variable to the path of your video file.
- Set the outputs_dir variable to the desired output directory.
- Run the script.
# Example
``` bash
video_file_path = r"C:\path\to\your\video.mp4"
outputs_dir = "outputs/"

short_summary = summarize_local_video(video_file_path, outputs_dir)

print("Video - TL;DR")
print("=" * 80)
print(short_summary)
```
