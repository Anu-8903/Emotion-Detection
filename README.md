Emotion-Aware Speech Recognition
This project performs emotion-aware speech recognition from video files. It uses OpenAI's Whisper model for transcription and a custom emotion recognition model using audio features such as MFCCs and pitch.

🔧 Features
🎙️ Speech Transcription using Whisper.

😄 Emotion Detection from speech audio.

📼 MP4 to WAV conversion using MoviePy.

🔍 MFCC and pitch feature extraction using Librosa.

🤖 Support Vector Machine (SVM) for emotion classification.

🧱 Dependencies
Make sure to install the following Python packages:

bash
Copy
Edit
pip install openai-whisper librosa numpy scikit-learn moviepy
Note: Whisper may also require PyTorch to be installed. You can install it with:

bash
Copy
Edit
pip install torch
📁 Project Structure
bash
Copy
Edit
emotion_speech_recognition/
│
├── main.py                    # Main script with all functionality
├── audio.ogg                  # Example input audio (replaceable)
├── Ducky_Happy_Juice.wav      # Auto-generated WAV file from MP4
└── README.md                  # Documentation (this file)
🚀 How to Use
Train Emotion Classifier (done once):

python
Copy
Edit
emotion_classifier, label_encoder = train_emotion_classifier()
Run Emotion-Aware Transcription:

python
Copy
Edit
audio_path = "your_video.mp4"
emotion_aware_speech_recognition(audio_path)
Output:

The program prints:

Transcription of the audio

Detected language

Detected emotion (e.g., happy, sad, angry, neutral)

🧠 How It Works
Convert video (MP4) to audio (WAV)

Use Whisper to transcribe speech and detect language

Extract MFCC and pitch features

Use a trained SVM to classify the emotional tone

⚠️ Notes
The emotion recognition model is trained on random data as a placeholder. You should train it with real labeled emotion datasets (e.g., RAVDESS, CREMA-D).

Whisper can handle multiple languages, but the emotion model is language-agnostic and based purely on vocal features.

📌 TODO
Integrate real-world emotion-labeled datasets

Improve emotion classification accuracy

Add GUI or web interface for usability

