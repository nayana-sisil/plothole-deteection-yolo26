# Pothole Detection via YOLO Multi Scale Architecture

## Abstract
This repository contains an implementation of a real time pothole detection system utilizing the Ultralytics YOLO framework. The model is optimized for edge deployment on central processing units (CPUs) by leveraging a native end to end, NMS free architecture.

## Technical Specifications
- Architecture: YOLO (Multi Scale Lightweight Detection)
- Training Environment: Google Colab (Tesla T4 GPU)
- Inference Environment: Local Windows CPU
- Optimization: Elimination of Non Maximum Suppression (NMS) and Distribution Focal Loss (DFL) to reduce computational latency by approximately 40 percent on CPU hardware.

## Installation and Methodology
Deployment requires a Python 3.12 environment with the Ultralytics and PyTorch libraries.
```bash
conda activate yolo-env1
yolo predict model=pothole_best_weights.pt source=pothole_video.mp4 save=True conf=0.25
```

## Performance Benchmarking
Experimental results demonstrate high precision in identifying localized road surface degradations under varying illumination conditions. The YOLO Small variant used in this study maintains consistent inference speeds suitable for real time monitoring applications.
