pip install torch torchaudio librosa numpy soundfile matplotlib wordcloud transformers
.
├── main.py                # Main script with full pipeline
├── hardvard.wav           # Input audio file (example)
├── noisy_output.wav       # Output noisy audio (optional)
├── transcription.txt      # (Optional) Output text
└── README.md              # This file
audio = load_audio("hardvard.wav")
noisy_audio = add_noise(audio, noise_level=0.05)
transcription = transcribe(noisy_audio)
4. Analyze & Visualize Text
Frequency bar chart

Word cloud

Homophone matches

5. Detect Homophones
python
Copy
Edit
homophone_matches = find_homophones_in_text(transcription)
📊 Sample Output
Transcription:

css
Copy
Edit
THEIR DOG ATE THE FLOWER FROM THE RIGHT SIDE OF THE GARDEN
Detected Homophones:

arduino
Copy
Edit
their → there, they're
flower → flour
right → write
🛠️ Customization
🔄 Replace hardvard.wav with your own audio file.

📈 Extend the homophone dictionary in homophones = { ... }.

🧹 Adjust noise level via add_noise(audio, noise_level=0.05).

🤖 Credits
Facebook AI Wav2Vec2

Hugging Face Transformers

Librosa, Torchaudio, SoundFile

WordCloud & Matplotlib for visualization

📌 License
MIT License – use, modify, and share freely.

