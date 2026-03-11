# Hand Gesture Controlled YouTube Player

A real-time computer vision project that allows users to control YouTube playback using hand gestures captured through a webcam.

The system uses **OpenCV** and **MediaPipe** to detect hand landmarks, interpret finger positions, and trigger media control actions such as play, pause, forward, backward, and volume control.

## Demo

Control YouTube without touching your keyboard or mouse using simple hand gestures.

## Features

* Real-time hand tracking using MediaPipe
* Detection of **21 hand landmarks**
* Finger counting using landmark coordinate comparison
* Gesture-to-action mapping for YouTube control
* Debounce mechanism to avoid repeated triggers
* Works using a standard webcam
* Runs efficiently on CPU

## Tech Stack

* Python
* OpenCV
* MediaPipe
* PyAutoGUI
* NumPy

## System Architecture

Webcam
↓
OpenCV Frame Processing
↓
MediaPipe Hand Landmark Detection
↓
Finger Counting Logic
↓
Gesture Recognition
↓
PyAutoGUI Keyboard Simulation
↓
YouTube Player Control

## Hand Landmarks

MediaPipe detects **21 key hand landmarks** which are used to determine finger positions and gestures.

## Gesture Mapping

| Fingers Detected | Action       |
| ---------------- | ------------ |
| 0                | Volume Down  |
| 1                | Fullscreen   |
| 2                | Forward      |
| 3                | Backward     |
| 4                | Volume Up    |
| 5                | Play / Pause |

## How It Works

1. Webcam captures real-time video
2. Frames are processed using OpenCV
3. MediaPipe extracts hand landmarks
4. Finger positions are analyzed
5. Number of raised fingers is calculated
6. Gesture is mapped to a YouTube control action
7. PyAutoGUI triggers keyboard commands

## Installation

Clone the repository:

```
git clone https://github.com/YOUR_USERNAME/hand-gesture-youtube-controller.git
cd hand-gesture-youtube-controller
```

Install dependencies:

```
pip install -r requirements.txt
```

Run the project:

```
python gesture_controller.py
```
## Future Improvements

* Dynamic gesture recognition
* Two-hand gesture support
* Machine learning based gesture classification
* Custom gesture configuration
* Integration with smart home devices
