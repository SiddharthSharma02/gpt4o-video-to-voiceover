Video Frame Extraction, Description, and Voiceover Generation

Overview

This project automates the process of extracting frames from a video, analyzing them using OpenAI's GPT-4 Vision API, generating a step-by-step tutorial-style description, converting the description into a voiceover, and merging the voiceover back with the original video.

Features

Extracts frames from a video at regular intervals.

Uses OpenAI's GPT-4 Vision API to generate descriptions of the extracted frames.

Converts the generated descriptions into an AI-generated voiceover.

Merges the generated voiceover with the original video to create an informative tutorial-style output.

Dependencies

Ensure you have the following Python libraries installed:

pip install opencv-python moviepy openai

File Structure

├── main.py                  # Main script
├── openaiapikey.txt         # File containing the OpenAI API key
├── extracted_frames/        # Folder where extracted frames are stored
├── voiceover.mp3            # Generated voiceover file
├── tt2.mp4                  # Final output video
└── README.md                # Project documentation

How It Works

1. Extract Frames

The script extracts frames from the video at a specified interval (default: every 60 frames) and saves them in the extracted_frames/ folder.

2. Analyze Frames with GPT-4 Vision API

The extracted frames are converted to base64 format and sent to OpenAI's GPT-4 Vision API with a predefined prompt to generate a step-by-step tutorial-style description.

3. Generate Voiceover

The generated text is converted into speech using OpenAI's text-to-speech model and saved as an audio file (voiceover.mp3).

4. Merge Audio with Video

The original video and generated voiceover are merged into a final output video (tt2.mp4).

Usage

Place your video file in the project directory.

Update the video_path variable in the script with the actual video file path.

Store your OpenAI API key in openaiapikey.txt.

Run the script:

python main.py

Configuration

Frame Extraction Interval: Modify frame_interval in extract_frames() to adjust how frequently frames are extracted.

GPT Model: Change the model parameter in get_frame_descriptions() if needed.

Voice Type: Modify voice in create_voiceover() to change the AI-generated voice.

Error Handling

Implements retry logic for API calls in case of server errors.

Checks if video files are valid before processing.

Skips processing if no frames are extracted.
