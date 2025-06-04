# 🚗 Real-Time Vehicle License Plate Recognition System

This project is an end-to-end real-time License Plate Recognition (LPR) system that detects vehicles, localizes license plates, and extracts alphanumeric characters using Optical Character Recognition (OCR). It is optimized for scalable, serverless deployment using AWS services and built with a modular pipeline using OpenCV, YOLOv5, and EasyOCR.

---

## 🔍 Features

- 🎯 **Vehicle Detection** using YOLOv5 (fine-tuned)
- 🔲 **License Plate Localization** with bounding box filtering
- 🔡 **Text Extraction** using EasyOCR for multilingual support
- ☁️ **Cloud Deployment** with AWS Lambda, S3, and SageMaker
- 🌐 **Web API Integration** using Flask (local) or FastAPI (optional)
- 🧪 **Tested on multiple real-world traffic videos** with varying lighting, angles, and plate types

---

## 📁 Project Structure

```bash
.
├── data/
│   └── sample_videos/           # Input vehicle videos
├── src/
│   ├── detector.py              # YOLOv5 vehicle & plate detection logic
│   ├── ocr_reader.py            # OCR logic using EasyOCR
│   ├── utils.py                 # Utility functions for drawing, saving, etc.
│   └── pipeline.py              # End-to-end LPR pipeline
├── app/
│   └── app.py                   # Flask app for local testing
├── aws/
│   └── lambda_handler.py        # AWS Lambda entrypoint (optional)
├── requirements.txt
└── README.md
```


## ⚙️ Technologies Used

Module	Tool/Library
Detection	YOLOv5 (fine-tuned)
OCR	EasyOCR
Backend	Python, OpenCV, Flask / FastAPI
Deployment	AWS Lambda, S3, SageMaker
Packaging	Docker, Git, CI/CD (optional)

---

## 🚀 Getting Started
🔧 Installation
```
bash
Copy
Edit
git clone https://github.com/yourusername/vehicle-lpr.git
cd vehicle-lpr
pip install -r requirements.txt
```
---

## ▶️ Running Locally
```bash
Copy
Edit
python app/app.py
```
This will run the Flask app where you can upload video files and get annotated results with extracted license plates.

---
## ☁️ AWS Deployment (Optional)
Package lambda_handler.py and dependencies using zip or Docker.

Upload to AWS Lambda with proper role permissions.

Configure S3 triggers for video ingestion and result storage.

## 📊 Performance
Metric	Result (Approx.)
Detection Accuracy	~92%
OCR Accuracy	~89%
Avg. Processing Time	~2 sec/frame

🧠 Future Work
Support for real-time live video feeds (e.g. RTSP, webcam)

Integration with vehicle registration databases

Multilingual and blurred plate correction

Frontend dashboard with Streamlit

