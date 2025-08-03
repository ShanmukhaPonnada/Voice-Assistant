<div align="center">
<h1 align="center">
🤖<br>All-in-One Offline Voice Assistant
</h1>
<p align="center">
A self-contained, offline-first voice assistant that runs entirely in your browser.
</p>
</div>

<p align="center">
<img src="https://www.google.com/search?q=https://img.shields.io/badge/Made_with-HTML_%26_JavaScript-orange%3Fstyle%3Dfor-the-badge%26logo%3Dhtml5" alt="Made with HTML & JS">
<img src="https://www.google.com/search?q=https://img.shields.io/badge/AI_Engine-Transformers.js-blue%3Fstyle%3Dfor-the-badge" alt="AI Engine">
<img src="https://www.google.com/search?q=https://img.shields.io/badge/License-MIT-green%3Fstyle%3Dfor-the-badge" alt="License">
</p>

🚀 Demo
A short GIF demonstrating the application's core functionality, including offline mode, would be placed here.

✨ Features
Local Speech-to-Text (STT): Utilizes the Xenova/whisper-tiny.en model to transcribe user audio directly in the browser.

Local Text-to-Speech (TTS): Employs the Xenova/speecht5_tts model and a corresponding vocoder to synthesize audio responses locally.

Offline First: After the initial load, the application and its AI models are cached, allowing for full functionality without an internet connection.

Performance-Optimized: All AI model processing is offloaded from the main UI thread to Web Workers, preventing the interface from freezing during computation.

Latency Monitoring: The UI displays real-time latency measurements for each stage of the pipeline (STT, API, TTS, Playback).

Zero Dependencies: The application is a single HTML file with no required build steps or external package installations.

🛠️ How to Run
Clone this repository or download the index.html file.

To ensure proper functionality (especially for microphone access), you must serve the file from a local web server.

The easiest way to do this is with the Live Server extension in Visual Studio Code.

Install the Live Server extension.

Right-click on index.html and select "Open with Live Server".

The application will open in your default web browser.

🏗️ Project Architecture
The application operates in a clear, sequential pipeline:

Audio Capture: The browser's MediaRecorder API captures audio from the user's microphone.

STT Processing: The raw audio data is sent to a Web Worker running the Whisper model, which transcribes it into text.

AI Logic (Mocked): The transcribed text is sent to a (currently simulated) AI backend. In a real-world scenario, this would be a fetch call to a secure server endpoint.

TTS Processing: The AI's text response is sent to a second Web Worker running the SpeechT5 model, which converts the text into raw audio data.

Audio Playback: The synthesized audio is played back to the user through the browser's Web Audio API.

🤝 Contributing
Contributions are welcome! If you have suggestions for improvements or find any issues, please feel free to open an issue or submit a pull request.

📜 License
This project is licensed under the MIT License. See the LICENSE file for details.
TTS Processing: The AI's text response is sent to a second Web Worker running the SpeechT5 model, which converts the text into raw audio data.

Audio Playback: The synthesized audio is played back to the user through the browser's Web Audio API.
