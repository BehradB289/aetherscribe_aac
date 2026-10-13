# 🌌 AetherScribe AAC

> **Intelligent Spatial Air-Writing & Persian Speech Synthesis System**  
> *Empowering touchless communication through spatial computer vision, real-time handwriting recognition, and multi-tier speech synthesis[cite: 1].*

---

## 📖 Overview

**AetherScribe AAC** is an assistive, web-based Augmentative and Alternative Communication (AAC) platform engineered for deaf and hard-of-hearing individuals[cite: 1]. Operating entirely in modern web browsers without backend server requirements, the system leverages computer vision to track hand landmarks in 3D space, translating fingertip motions into digital ink, recognizing Persian handwriting, and vocalizing words through advanced speech synthesis engines[cite: 1].

---

## ✨ Key Features

- **Spatial Air-Writing in 3D:** Built on Three.js and WebGL, allowing fluid air-writing with dynamic buffer geometry, spatial depth scaling, and glowing neon trail effects[cite: 1].
- **Touchless Hand Gesture Controls:**
  - 🤏 **Pinch (Thumb + Index Tip):** Engages the virtual stylus to write in 3D space[cite: 1].
  - ✌️ **Peace Sign (✌️):** Triggers handwriting recognition and automatically reads the text aloud[cite: 1].
  - ✊ **Closed Fist (✊):** Clears the entire 3D drawing canvas and resets all stroke coordinates[cite: 1].
- **Multi-Tier Persian Speech Engine (AAC):**
  - **Google Gemini 2.5 Flash TTS:** Generates studio-grade natural Persian speech using the `Sulafat` voice profile and PCM16-to-WAV conversion[cite: 1].
  - **Native Microsoft Edge Voices:** Provides low-latency speech output supporting voices like *Dilara* and *Farid*, with intelligent regional fallback[cite: 1].
  - **Cloud Audio Stream:** Offers resilient online audio streaming with referrer-bypass headers and timeout handling[cite: 1].
- **Dual-View Telemetry & Radar HUD:** Features an interactive 2D radar minimap with bounding-box interpolation (`LERP`), smooth curve filtering, and a live rotating radar sweep line[cite: 1].
- **High-Precision Vector Smoothing:** Reduces hand jitter in real time using linear vector interpolation (`VectorSmoother`) for clean handwriting[cite: 1].
- **Persian Handwriting Recognition (IME):** Integrates Google Input Tools handwriting recognition with contextual vocabulary booster candidates[cite: 1].
- **Quick-Access Vocabulary Deck:** Provides one-click shortcut chips for high-frequency phrases (e.g., سلام، بهراد، متشکرم، کمک، بله، خیر)[cite: 1].
- **Synthesized Audio Feedback:** Features custom Web Audio API oscillators for sound effects, including clicks, eraser swooshes, and melodic chimes[cite: 1].

---

## 🛠️ Tech Stack

- **Core:** HTML5, CSS3 Glassmorphism HUD, Vanilla JavaScript (ES Modules)[cite: 1]
- **3D Graphics Engine:** [Three.js](https://threejs.org/) (v0.160.0)[cite: 1]
- **Computer Vision:** [MediaPipe Tasks Vision](https://developers.google.com/mediapipe) (`HandLandmarker` v0.10.9 with GPU delegate)[cite: 1]
- **Handwriting Recognition:** Google Input Tools IME API for Persian handwriting[cite: 1]
- **Speech & Audio:** Web Audio API, Web Speech API, and Google Gemini API (`gemini-2.5-flash-preview-tts`)[cite: 1]
- **Typography:** Vazirmatn and Orbitron[cite: 1]

---

## 🖐️ Gesture Guide

- **Pinch (Thumb + Index):** Starts drawing strokes in mid-air; the top navigation meter shows the pinch proximity in real time[cite: 1].
- **Peace Sign (✌️):** Finalizes the current drawing strokes and sends them to the recognition pipeline[cite: 1].
- **Fist (✊):** Clears all spatial geometry and resets the stroke telemetry counters[cite: 1].

---

## 🚀 Getting Started

### Prerequisites

- A modern web browser supporting WebGL and WebRTC (Microsoft Edge or Google Chrome recommended)[cite: 1].
- A connected webcam[cite: 1].

### Running Locally

Because the project is constructed as a self-contained web application, no external package managers or compilation steps are required[cite: 1].

1. **Clone the repository:**
    git clone https://github.com/your-username/aetherscribe-aac.git
    cd aetherscribe-aac

2. **Serve through a local web server (required for webcam permissions):**
    # Using Python 3
    python -m http.server 8080

    # Or using Node.js
    npx http-server -p 8080

3. **Open the application:**
    Navigate to http://localhost:8080/aetherscribe_aac.html in your browser.

---

## ⚙️ Configuration & Settings

Click the **Gear Icon (⚙️)** in the top navigation bar to configure system options[cite: 1]:

- **Gemini API Key:** Enter your Google AI Studio API key to enable Gemini 2.5 Flash neural Persian speech[cite: 1].
- **Camera Selection:** Switch between available video input devices[cite: 1].
- **Resolution:** Toggle between 720p HD, 1080p Full HD, and 480p SD modes[cite: 1].
- **Stroke Smoother:** Adjust stroke interpolation between `0.30` and `0.90` to eliminate hand tremors[cite: 1].
- **Mirror Mode:** Flip webcam display horizontally for intuitive hand coordination[cite: 1].
- **Auto-Speak:** Toggle automatic voice playback immediately after recognition[cite: 1].

---

## 🌐 Recommended Browser

For native Persian voice output without entering an external API key, **Microsoft Edge** is recommended due to its built-in support for the natural *Dilara* and *Farid* neural voices[cite: 1].

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
