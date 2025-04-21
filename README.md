
# ✋ Real-Time Hand Gesture Recognition with MediaPipe & SVM

This project demonstrates a **real-time hand gesture recognition system** using **MediaPipe**, **OpenCV**, and **Scikit-learn**. A simple **Support Vector Machine (SVM)** model is trained on simulated gesture data to distinguish between **Wave** and **Stop** gestures.

> 🧠 Ideal for beginners exploring real-time computer vision and machine learning integration with webcams.

---

## 🧰 Tech Stack

| Tool | Purpose |
|------|---------|
| [Python](https://www.python.org/) | Programming language |
| [OpenCV](https://opencv.org/) | Real-time video capture and image processing |
| [MediaPipe](https://developers.google.com/mediapipe) | Hand landmark detection |
| [Scikit-learn](https://scikit-learn.org/) | SVM classifier for gesture prediction |
| [Google Colab](https://colab.research.google.com/) | Cloud-based notebook for running the project |

---

## 🚀 Features

- Detects hand in real-time using webcam
- Extracts 3D hand landmark positions using MediaPipe
- Classifies gestures with a linear SVM
- Displays live gesture prediction on screen
- Fully compatible with Google Colab (no GUI issues)

---

## 📂 Project Structure

```
.
├── gesture_recognition.ipynb     # Main notebook
├── README.md                     # This file
```

---

## 🧪 Sample Output

| Gesture Detected | Output |
|------------------|--------|
| Hand raised horizontally and moved – wave | `Wave` |
| Hand held up – stop sign | `Stop` |

---

## ⚙️ How It Works

1. **Hand Detection**: MediaPipe detects 21 hand landmarks per hand.
2. **Feature Extraction**: Landmark (x, y, z) coordinates are flattened into a 63-dim feature vector.
3. **Model Training**: SVM is trained on randomly simulated gestures (Wave = 0, Stop = 1).
4. **Real-Time Prediction**: As webcam frames are processed, detected hand landmarks are passed to the trained model for prediction.

---

## 📦 Installation

Run this in a Colab cell:

```bash
!pip install mediapipe==0.10.9 opencv-python-headless scikit-learn
```

---

## 🏁 How to Run

1. **Open in Google Colab**: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yourusername/your-repo/blob/main/gesture_recognition.ipynb)

2. **Run All Cells**:
   - Train the dummy gesture dataset.
   - Start webcam capture.
   - Watch live predictions on screen.

> 🛑 Press `Ctrl + M + .` or use stop icon in Colab to stop webcam.

---

## 📌 Notes

- The current dataset is **randomly generated** for demonstration.
- For real-world use, **collect real gesture data** and retrain the model.
- This project uses `opencv-python-headless` to work smoothly in **Google Colab**, where normal OpenCV GUI methods aren't supported.

---

## 🧠 Future Improvements

- Replace random data with real gesture samples.
- Add more gesture types (e.g., Thumbs Up, Peace Sign).
- Use advanced models (e.g., LSTM or CNN) for better accuracy.
- Export model to use in web/mobile apps.

---

## 🤝 Contributing

Pull requests are welcome! Feel free to suggest new gestures or improvements to the model or visualization.

