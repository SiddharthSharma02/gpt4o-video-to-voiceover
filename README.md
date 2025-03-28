AI-Powered Video Narration with GPT-4 Vision & TTS
This Python script automates the process of generating an AI-driven voiceover for a given video using OpenAI's GPT-4 Vision API and Text-to-Speech (TTS) models. It extracts frames from the video, analyzes them to create a step-by-step tutorial-style narration, converts the text into speech, and merges the voiceover with the original video.

Features
✅ Extracts frames from a video at regular intervals.
✅ Uses GPT-4 Vision to analyze frames and generate a descriptive narration.
✅ Converts the narration into a natural-sounding voiceover using OpenAI's TTS API.
✅ Merges the generated voiceover with the original video.
✅ Handles API errors with a retry mechanism for robustness.

Installation
Prerequisites
Python 3.x

Required libraries (install with the following command):

bash
Copy
Edit
pip install openai opencv-python moviepy
Usage
Set up OpenAI API Key

Store your OpenAI API key in a file named openaiapikey.txt.

Modify Video Path

Update the video_path variable in the script with your video file path.

Run the Script

bash
Copy
Edit
python script.py
How It Works
Extracts Key Frames → Saves frames from the video at a defined interval.

Analyzes Frames with GPT-4 Vision → Generates a step-by-step explanation.

Creates a Voiceover → Converts the generated text into speech.

Merges Voiceover with Video → Produces a final narrated video.

Output
The script outputs:

voiceover.mp3: AI-generated narration.

tt2.mp4: The final video with merged audio narration.

Future Enhancements
Support for multiple voice options.

Improved frame selection for better contextual analysis.

GUI-based input selection for ease of use.
