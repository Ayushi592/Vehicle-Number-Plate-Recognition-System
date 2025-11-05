## 🚗 Vehicle Number Plate Recognition System
Automated vehicle access control using Computer Vision (OpenCV + YOLO + OCR)
## Overview

This project is an AI-based automated vehicle authorization system that detects vehicle number plates in real-time, extracts text, and verifies it from a database before granting access.

It replaces manual entry systems at gates with accurate & fast computer vision-based automation.

## Objective

✔️ Detect vehicle license plates in live video feeds
✔️ Extract text using OCR
✔️ Validate the number with registered database entries
✔️ Automate access based on authorization

## Key Features

📷 Real-time plate detection	YOLOv8 model for fast & accurate detection
🔤 OCR text extraction	EasyOCR for recognizing plate text
🗄️ SQL Database	Stores authorized vehicle details
⚙️ Automation Ready	Logic for gate unlock/alert system integration
🧠 Image Preprocessing	Noise removal, thresholding, cropping
## Tech Stack
| Component        | Technology              |
|------------------|-------------------------|
| Programming      | Python                  |
| Computer Vision  | OpenCV                  |
| OCR Engine       | EasyOCR / Tesseract     |
| AI Model         | YOLOv8                  |
| Database         | MySQL / SQLite          |
| Visualization    | matplotlib / cv2 GUI    |

## Folder Structure
```bash
Vehicle-Number-Plate-Recognition/
│── model/                 # YOLO model files
│── database/              # Vehicle records
│── examples/              # Test images/videos
│── src/
│   ├── detect.py          # Detection pipeline
│   ├── extract_text.py    # OCR functions
│   ├── validate.py        # Database validation logic
│   └── main.py            # Integrated execution
│── requirements.txt
└── README.md
```

## System Workflow
Live Camera Feed / Video Input 
        ↓
YOLOv8 detects number plate region
        ↓
OpenCV crops / preprocesses plate
        ↓
EasyOCR extracts text characters
        ↓
Compare text with database records
        ↓
✅ If authorized → Access Granted
❌ If not → Alert Triggered

## ▶️ Run Locally
```bash
Install Dependencies
pip install -r requirements.txt
```

## Run Script
```bash
python main.py
```

## Sample Output

✅ Plate Detected
✅ Extracted Number: MH12AB1234
✅ Match Found → Gate Open

⚠️ Plate: MH14XY9876
❌ Unauthorized → Alert Raised

## Challenges Solved
Low-light images	Preprocessing: grayscale + thresholding
Skewed plates / angles	YOLOv8 robustness + frame processing
OCR noise	Image cleaning & cropping
Real-time performance	Model optimization & frame skipping
## Future Enhancements
Feature	Impact
Cloud database	Real-time logs across locations
Mobile app	Admin panel for approvals
Hardware integration	Servo motor for gate automation
ANPR dataset training	Higher accuracy in Indian conditions
Infrared camera support	Night vision accuracy boost
## 🧑‍💻 Developer

Ayushi Nagpure
📍 SIT Nagpur


## Acknowledgments

Ultralytics YOLOv8

EasyOCR

OpenCV
