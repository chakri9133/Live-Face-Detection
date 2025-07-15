# Face Liveness Detection

This project is a **real-time face liveness detection system** built using **Flask** and **OpenCV**. It detects faces and eyes via webcam and determines whether the face is "Real" (live) or "Spoof" (e.g., a photo) based on blink detection.

---

## 💡 Features

- 🎥 Real-time face detection using webcam
- 👁️ Eye detection to verify liveness (checks for blinks)
- 🔄 Blink counting and display
- ⚠️ Spoof detection alert
- 🖥️ Clean, modern web interface

---

## 🛠️ Technologies Used

- Python 3
- Flask
- OpenCV
- HTML & CSS

---

## 🚀 Getting Started

### ✅ Prerequisites

- Python 3.x installed
- Webcam connected and working

### 📥 Installation

1. **Clone the repository**

```bash
git clone https://github.com/chakri9133/Live-Face-Detection.git
cd Live-Face-Detection
```

2. **Install dependencies**

```bash
pip install flask opencv-python
```

### ▶️ Run the application

```bash
python face.py
```

- Open your browser and navigate to: **http://127.0.0.1:5000/**
- Allow access to your webcam when prompted.

---

## 🗂️ Project Structure

```
face-liveness-detection/
│
├── face.py          # Main Flask application and video processing logic
├── templates/
│   └── index.html   # Web front-end interface
└── README.md        # Project documentation (this file)
```

---

## ⚙️ How It Works

- **Face & eye detection**:  
  Uses OpenCV Haar cascades (`haarcascade_frontalface_default.xml` and `haarcascade_eye.xml`) to detect faces and eyes.

- **Liveness verification (blink detection)**:  
  - If two eyes are detected → labeled as "Real"
  - Eyes disappear and reappear (blink) → blink count increments
  - If no eyes are detected in the face region → labeled as "Spoof"

- **Web video streaming**:  
  The `/video_feed` route continuously streams processed frames to the front-end using MJPEG.

---

## ⚠️ Limitations

- May not detect advanced spoofing attacks (e.g., videos, 3D masks).
- Blink detection relies on consistent lighting and frontal face position.

---

## 🌟 Possible Improvements

- Use CNN-based liveness detection models for stronger spoof prevention.
- Support for multiple faces in the frame.
- Integrate additional liveness cues (e.g., head movements, texture analysis).

---

## 🤝 Contributing

Contributions are welcome! Feel free to fork this repository, make changes, and submit a pull request.

---

### 💬 Questions?

If you have any questions or need help, feel free to open an issue or contact me.

---

🚀 Happy coding and stay secure!
