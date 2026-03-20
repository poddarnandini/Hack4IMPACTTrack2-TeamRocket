# NutriLens — AI-Based Food Recognition & Nutrition Tracker

**Team Name:** Team Rocket  
**Hackathon:** HACK4IMPACT Track 2 — KIIT Bhubaneswar  
**Domain:** AI & Automation in Smart Healthcare  

---

## Team Members

- Nandini Poddar — Lead
- Prachi Mohanty
- Meethi Saxena
- Khushi Khushwaha

---

## Problem Statement

Millions of people in India struggle to track their daily calorie and
nutritional intake accurately. Apps like MyFitnessPal were built for
Western diets and carry little to no reliable data for Indian cuisine,
which changes dramatically across regions, recipes, and cooking methods.
People managing diabetes, obesity, PCOD, and other lifestyle diseases
need precise nutritional monitoring but have no tool that actually
understands what they eat. Manual calorie logging is tedious, often
inaccurate, and most people give up within weeks. NutriLens aims to fix
this by building an AI-powered nutrition tracker trained specifically on
Indian food, removing the need for any manual input through automated
food recognition, portion estimation, and barcode scanning.

---

## Proposed Solution

NutriLens is an end-to-end AI pipeline that allows users to:
- Upload a photo of any Indian food dish
- Automatically identify the dish using EfficientNetB1
- Estimate portion size using MiDaS depth estimation
- Calculate calories and macronutrients instantly
- Scan barcodes of packaged foods via Open Food Facts API
- Log all meals in a daily food diary and track progress

---

## Tech Stack

- Python
- TensorFlow / Keras
- PyTorch
- EfficientNetB1
- MiDaS
- OpenCV
- Open Food Facts API

---

## Repository Structure
```
├── notebooks/
│   ├── 01_train_Classifier.ipynb   # EfficientNetB1 training
│   ├── 02_depth_estimation.ipynb   # MiDaS depth estimation
│   └── 03_barcode_scanner.py       # Barcode + Open Food Facts
├── saved_models/
│   └── labels.json                 # Food category labels
├── test_images/
│   ├── sample1.jpg
│   └── sample2.jpg
├── utils/
│   └── calorie_db.py               # Calorie and macro database
├── app.py                          # Main application
├── main.ipynb                      # End-to-end pipeline
├── requirements.txt
├── .gitignore
└── README.md
```

---

## Checkpoint Status

### Checkpoint 1 — [24hr stable]
- Project structure set up
- EfficientNetB1 classifier training notebook ready
- Food category labels defined
- Calorie database module built
- Requirements documented

### Checkpoint 2 — [12hr stable]
- Depth estimation module integrated
- Barcode scanner connected to Open Food Facts API
- End-to-end pipeline connected
- App interface ready
- Test images added
- Full repository structured and pushed

---

## Note on Dataset

The training dataset consists of self-collected Indian food images.
It is not pushed to this repository and remains local for privacy.
Data augmentation techniques used: rotation, zoom, brightness
adjustment, and horizontal flipping.
The trained model file food_classifier.h5 is excluded from GitHub
due to file size and is available locally for live demonstration.

---

## How to Install
```bash
pip install -r requirements.txt
```

## How to Run
```bash
python app.py
```
