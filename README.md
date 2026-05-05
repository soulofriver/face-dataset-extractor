# Face Dataset Extractor

A computer vision tool that detects faces in a video and automatically saves cropped face images for dataset creation.

---

##  Features
- Face detection from video file
- Automatic face cropping and saving
- Smart capture delay to avoid duplicates
- Frame skipping for performance optimization
- Real-time preview with bounding boxes

---

##  How It Works

This project processes a video file frame-by-frame to detect and extract faces.

Workflow:
1. Load video file
2. Skip frames for faster processing
3. Detect faces using Haar Cascade
4. Draw bounding boxes for visualization
5. If faces are detected:
   - Crop face regions
   - Save them as images
   - Use a delay to prevent duplicate captures

---

## Requirements

Make sure you have:

video.mp4

The Haar Cascade file will be downloaded automatically if not present.

---

## Run

python main.ipynb

---

## Output

Saved faces will be stored in:

faces/

Example output:

face_1.jpg

face_2.jpg

face_3.jpg...

---

## Parameters

capture_delay = 5

Delay (in seconds) between captures to avoid duplicates

frame_skip = 3

Process every 3rd frame for better performance

---

## Visualization

Blue rectangles = detected faces

Counter = total saved faces

---

## Technical Notes

Uses grayscale conversion for faster detection

Frame skipping improves speed on large videos

Cropped faces are saved directly without resizing

Works best with clear frontal faces

---

## Use Cases

Creating datasets for face recognition models

Collecting training data for AI projects

Preprocessing video data for machine learning

## Installation

```bash
pip install opencv-python
