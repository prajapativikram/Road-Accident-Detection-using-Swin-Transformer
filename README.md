# AI-Powered Road Accident Detection and Video Summarization

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat&logo=streamlit&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![Computer Vision](https://img.shields.io/badge/Computer%20Vision-AI-blue)
![Deep Learning](https://img.shields.io/badge/Deep%20Learning-Powered-red)
![Accuracy](https://img.shields.io/badge/Accuracy-94%25-brightgreen)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

An AI-powered computer vision system that detects road accidents from uploaded videos using a Swin Transformer model. The application identifies accident scenes, extracts important accident frames, generates a summarized accident video, and provides an interactive Streamlit interface.

---

## Features

- Upload traffic surveillance videos
- Detect Accident / Non-Accident scenes
- Deep learning model using Swin Transformer
- Confidence-based accident prediction
- Accident frame extraction
- Grid view of key accident frames
- Accident summary video generation
- Download processed videos
- Interactive Streamlit interface



### Accident Summary

(Add screenshot)

---

## 🏗️ Project Architecture

```mermaid
flowchart TD
    A[📹 User Uploads Video] --> B[🎞️ Frame Extraction<br/>OpenCV]
    B --> C[🖼️ Image Preprocessing<br/>Resize • Normalize • Transform]
    C --> D[🧠 Swin Transformer Model]
    D --> E{Prediction}

    E -->|Accident| F[🚨 Accident Frame Detection]
    E -->|Non-Accident| G[✅ Ignore Frame]

    F --> H[📸 Store Accident Frames]
    H --> I[🖼️ Generate Grid View]
    H --> J[🎬 Generate Accident Summary Video]

    I --> K[📊 Streamlit Dashboard]
    J --> K

    K --> L[⬇️ Download Summary Video]
```

## Tech Stack

- Python
- PyTorch
- Swin Transformer
- OpenCV
- Streamlit
- NumPy
- Pillow
- TorchVision

---

## Project Structure

```text
app.py
README.md
requirements.txt
models/
sample_videos/
outputs/
images/
```

---

## Installation

Clone repository

```bash
git clone https://github.com/prajapativikram/Road-Accident-Detection-using-Swin-Transformer
.git
```

Move inside folder

```bash
cd Road-Accident-Detection-using-Swin-Transformer

```

Install dependencies

```bash
pip install -r requirements.txt
```

Run Streamlit

```bash
python -m streamlit run app.py
```

---

## Model

The project uses a fine-tuned Swin Transformer for binary classification.

Classes:

- Accident
- Non Accident

Framework:

PyTorch

---

## Dataset

The model was trained on a road accident dataset containing accident and non-accident images extracted from traffic videos.

If the dataset cannot be redistributed, include a link to the original source instead of uploading it.

---

## Results

| Metric | Score |
|---------|------:|
| Accuracy | 94% |
| Precision | 95% |
| Recall | 94% |
| F1 Score | 94% |

Classification Report

```
Accident

Precision : 1.00
Recall : 0.87
F1 Score : 0.93

Non Accident

Precision : 0.90
Recall : 1.00
F1 Score : 0.95

Overall Accuracy : 94%
```

---

## Future Improvements

- YOLO based vehicle localization
- Automatic accident timeline
- Whisper transcript generation
- Multi-camera support
- Cloud deployment
- Real-time CCTV monitoring

---

## Author

Vikram Kumar

B.Tech Computer Science & Engineering

AI • Machine Learning • Computer Vision

LinkedIn: https://www.linkedin.com/in/vikram-kumar-0b19a9248/


---

## License

MIT License
