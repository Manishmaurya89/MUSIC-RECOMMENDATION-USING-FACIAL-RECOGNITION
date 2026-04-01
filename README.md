# 🎵 Emotion-Based Music Recommendation System

A web app that watches your face, reads your emotion in real time, and recommends music that matches your mood — powered by OpenCV, a trained CNN emotion classifier, and Streamlit.

---

## 🧠 How It Works

```
Webcam Feed
    ↓
Face Detection (Haar Cascade)
    ↓
Crop Face Region
    ↓
Emotion Classification (CNN · model.h5)   ← runs 30–40 times over 2–3 seconds
    ↓
Sort emotions by frequency
    ↓
Recommend songs from dataset (muse_v3.csv) matching top emotions
```

Emotions detected: `Happy · Sad · Angry · Surprised · Neutral · Fear · Disgust`

---

## ✨ Features

- 📸 **Live webcam emotion scanning** — captures multiple frames for stable prediction
- 🧬 **CNN-based classifier** — custom trained model stored as `model.h5`
- 🎶 **Music dataset matching** — maps emotions to songs from `muse_v3.csv`
- 🌐 **Streamlit web interface** — runs locally in your browser, no setup complexity
- 🔒 **100% local** — no data sent anywhere

---

## 🛠️ Tech Stack

`Python` · `Streamlit` · `OpenCV` · `TensorFlow / Keras` · `Pandas` · `NumPy`

---

## 🚀 Getting Started

**Requirements:** Python 3.7+, a webcam

```bash
# Clone the repo
git clone https://github.com/Manishmaurya89/MUSIC-RECOMMENDATION-USING-FACIAL-RECOGNITION.git
cd MUSIC-RECOMMENDATION-USING-FACIAL-RECOGNITION

# Install dependencies
pip install -r requirements.txt

# Run the app
streamlit run app.py
```

Open [http://localhost:8501](http://localhost:8501) in your browser and allow camera access.

---

## 📁 Project Structure

```
MUSIC-RECOMMENDATION-USING-FACIAL-RECOGNITION/
├── app.py                              # Main Streamlit app
├── model.h5                            # Trained CNN emotion classifier
├── haarcascade_frontalface_default.xml # OpenCV face detector
├── muse_v3.csv                         # Music dataset with mood labels
├── requirements.txt
└── README.md
```

---

## 📦 Requirements

```
streamlit
opencv-python
numpy
pandas
tensorflow
keras
```

---

## 📬 Contact

For questions or feedback: **manish.maurya0408@gmail.com**

---

## 📄 License

MIT License — free to use and modify.

