

# ACC-L3-01-RK3588-AI-enabled-Container


**Version:** 1.0  
**Release Date:** April 2025  
**Copyright:** © 2025 Advantech Corporation. All rights reserved.

## Overview

The  ACC-L3-01-RK3588-AI-enabled-Container is a object detection demo Container on RK3588 NPU. 

### Key Features

- **AI Application Demo:** Object detection
- **Hardware Acceleration:** NPU
- **Complete AI Framework Stack:** RKNN
- **Industrial Vision Support:** Accelerated OpenCV 
- **Edge AI Capabilities:** Support for computer vision


## Hardware Specifications

| Component | Specification |
|-----------|---------------|
| Target Hardware | ROM-6881 |
| CPU | RK3588 |
| NPU | 3 Cores |
| Memory | shared system memory |

## Software Components

| Component | Version | Description |
|-----------|---------|-------------|
| RKNN Runtime| 2.0.0b0 |  RKNN Runtime provides AI framework run Model inference |
| OpenCV | 4.6.0 | Computer vision library |
| python | 3.11.2 | python library |


## Supported AI Capabilities

## Vision Models

| Model Family | Versions | Performance (FPS) | Quantization Support |
|--------------|----------|-------------------|---------------------|
| YOLO | v10 | YOLOv10: 30 @ 640x640 | INT8 |


## Quick Start Guide

### Run on NPU
plugin a UVC camera into board and then run docker cmd

```bash
sudo docker run -d -it --privileged --rm --device=/dev/dri/card0 -e DISPLAY=$DISPLAY -e XAUTHORITY=/tmp/.Xauthority  -v ~/.Xauthority:/tmp/.Xauthority:ro -v /tmp/.X11-unix:/tmp/.X11-unix:rw -v /dev/:/dev/ docker-image-name /bin/bash -c ai-demo
```

Copyright © 2025 Advantech Corporation. All rights reserved.

