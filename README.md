# FC Barcelona Player Detection and Tracking with YOLOv8

This repository contains a project for detecting and tracking the entire FC Barcelona squad (16 players) in video footage using the YOLOv8 (You Only Look Once version 8) object detection model. The project leverages a custom dataset (`data-v3`). It processes video input to identify players such as Pedri, Gavi, Frenkie, Olmo, Kounde, Inigo, Cubarsi, Lewa, Tek, Casado, Fermin, Araujo, Raphinha, Yamal, Balde, and Ferran, with additional analysis of the defensive line. This project evolved from a focus on detecting a single player (Pedri) to a comprehensive squad analysis, making it a valuable tool for football analytics enthusiasts and researchers.

## Project Overview

- **Objective**: Detect and track 16 FC Barcelona players in real-time video.
- **Model**: YOLOv8 (e.g., YOLOv8n, YOLOv8s, or custom-trained variant), fine-tuned on a custom YOLO-formatted dataset.
- **Dataset**: containing images and labels for the 16 players.
- **Output**: Annotated video (`yolov8_tracked_barca_video.mp4`) with player IDs and defensive line metrics.
- **Environment**: Optimized for Kaggle with T4 GPU (15GB VRAM) or similar Colab setups.


## Features

- **Multi-Object Detection**: Identifies all 16 FC Barcelona players with a reported mAP50 of approximately 0.367 (can be improved with further tuning).
- **Real-Time Tracking**: Uses ByteTrack for robust player tracking across frames.
- **Defensive Line Analysis**: Calculates the average height of defensive players (e.g., Kounde, Inigo, Cubarsi, Araujo, Balde) on the field.
- **Customizable**: Supports dataset adjustments, model size selection (e.g., nano, small, medium), and hyperparameter tuning.

## Prerequisites

- **Hardware**: GPU with at least 15GB VRAM (e.g., T4).
- **Software**:
  - Python 3.x
  - PyTorch
  - OpenCV
  - Ultralytics YOLOv8 (`pip install ultralytics`)
  - Supervision (`pip install supervision`) for tracking
- **Dependencies**: Install required packages via the provided setup script.

