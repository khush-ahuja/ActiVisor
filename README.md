# ActiVisor

Real-time sign recognition from a webcam: MediaPipe Holistic tracks the body, face and hands, and an LSTM classifies short sequences of keypoints into signs, shown as on-screen text for deaf and hard-of-hearing users.

## How it works

```
webcam frame ─► MediaPipe Holistic ─► 1,662 keypoints per frame (pose, face, both hands)
                                              │
                         last 30 frames ──────┘
                                              ▼
                     LSTM(64) ─► LSTM(128) ─► LSTM(64) ─► Dense ─► softmax over 10 signs
```

- **Signs:** hello, thanks, father, mother, yes, no, help, A, B, C
- **Data:** 30 recorded sequences per sign, 30 frames each, stored as NumPy keypoint arrays
- **Model:** 3-layer LSTM in TensorFlow/Keras, trained with categorical cross-entropy
- **Real time:** a rolling 30-frame window is classified every frame; a prediction is shown only above 0.8 confidence
- **App:** a Flask app streams the annotated webcam feed with the recognised signs

## Files

| File | What it does |
|---|---|
| `Action Detection .ipynb` | keypoint extraction, data collection, training |
| `Real_Time Testing.ipynb` | live webcam inference |
| `app.py.ipynb`, `camera.py.ipynb` | Flask streaming app |
| `action.h5`, `action.keras` | trained model weights |

## Status

Early prototype trained on a small self-recorded dataset, so it works best for the recording signer and setting. Next steps: more signers and samples per sign, a held-out signer for testing, and a hand-only feature set to cut the 1,662-value input.

## Tech

Python · OpenCV · MediaPipe · TensorFlow/Keras · scikit-learn · Flask
