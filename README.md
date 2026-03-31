### ComputerVision_Project_ManikPandey

# CLI Hand Gesture & Finger Counter

## Overview
This Computer Vision project is an automated, Command Line Interface (CLI) based hand gesture tracker. It utilizes OpenCV and Google's MediaPipe framework to detect human hands, extract 21 3D spatial landmarks, and mathematically calculate the number of fingers currently held up. 

The project is engineered with strict headless-server compatibility, ensuring it can run safely in automated grading environments (like Docker containers) without triggering X11/GUI display errors, while still offering a live interactive mode for local testing.

### Core Concepts Applied:
* **Video I/O Processing:** Handling both static image and continuous video streams.
* **Feature Extraction:** Utilizing MediaPipe for robust palm detection and skeletal landmarking.
* **Color Space Conversion:** Managing BGR (OpenCV) to RGB (MediaPipe) pipelines.
* **Heuristic Logic:** Applying Euclidean distance and coordinate geometry to determine finger states.

---

## Prerequisites
* Python 3.8 or higher
* Git

## Setup & Installation

**1. Clone the repository**
```bash
git clone https://github.com/YOUR-USERNAME/gesture-tracker.git
cd 
```

## Execution Instructions

This script is highly flexible and can be run via the CLI for both live webcam demonstrations and automated video processing.

**Option 1: Live Webcam Mode (For Interactive Demo)**
To run the project using your local webcam, use the `-w` flag. Press 'q' in the window to exit.
`python gesture.py -w`

**Option 2: Automated File Processing (For Evaluators/Headless Servers)**
If running in an automated environment without a webcam, pass an input video and define an output path.
`python gesture.py -i input/sample_hand.mp4 -o output/tracked_hand.mp4`

```
project_structure/
│
├── input/                  # Directory for source images/videos
├── output/                 # Directory for processed media
├── gesture.py              # Main application script
├── requirements.txt        # Python dependencies
└── README.md               # Project documentation
```
Technologies Used
Python: Core programming language.

OpenCV (cv2): Image processing, drawing annotations, and file I/O.

MediaPipe: Machine learning pipeline for hand landmark detection.

Argparse & Logging: For robust CLI execution and professional stdout tracking.