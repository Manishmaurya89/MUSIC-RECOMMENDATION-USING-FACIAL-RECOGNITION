# Emotion-Based Music Recommendation

A small web app that looks at your face through the webcam, works out how you're feeling and suggests songs to
match. It uses OpenCV to find your face, a CNN to classify the emotion and Streamlit for the page.

## How it works

When you click **SCAN EMOTION**, the app reads 20 frames from your webcam. In each frame it finds your face with
a Haar cascade, crops it to 48×48 grayscale and asks the CNN in `model.h5` which of 7 emotions it shows: happy,
sad, angry, surprised, neutral, fear or disgust.

It then counts how often each emotion came up and picks 30 songs from `muse_v3.csv`. The most frequent emotion
gets the most songs. The songs are split into five groups (happy, neutral, angry, fear and sad), and sad, disgust
and surprised all draw from the sad group. Each song links to its Last.fm page.

```
Webcam (20 frames)
  -> find the face (Haar cascade)
  -> crop to 48x48 grayscale
  -> classify the emotion (CNN, model.h5)
  -> count the emotions, most frequent first
  -> pick 30 matching songs from muse_v3.csv
```

Everything runs on your own computer. Nothing is uploaded.

## Running it

You need Python 3.9 or newer and a webcam.

```bash
git clone https://github.com/Manishmaurya89/MUSIC-RECOMMENDATION-USING-FACIAL-RECOGNITION.git
cd MUSIC-RECOMMENDATION-USING-FACIAL-RECOGNITION
pip install -r requirements.txt
streamlit run app.py
```

Open http://localhost:8501 and allow camera access. The scan opens a separate video window; press `x` to close it
early.

## Files

| File | What it is |
| --- | --- |
| `app.py` | The Streamlit app |
| `model.h5` | Trained CNN weights for the 7 emotions |
| `haarcascade_frontalface_default.xml` | OpenCV face detector |
| `muse_v3.csv` | Song dataset with mood tags |
| `requirements.txt` | Python packages |
| `Report (1).pdf`, `PPT.pptx` | Project report and slides |

## Built with

Python, Streamlit, OpenCV, TensorFlow/Keras, Pandas and NumPy.

## Contact

Questions or feedback: manish.maurya0408@gmail.com
