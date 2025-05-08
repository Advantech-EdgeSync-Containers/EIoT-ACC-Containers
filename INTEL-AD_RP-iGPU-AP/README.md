

# ACC-L3-01-INTEL-AI-enabled-Container


**Version:** 1.0  
**Release Date:** April 2025  
**Copyright:** © 2025 Advantech Corporation. All rights reserved.

## Overview

The  ACC-L3-01-INTEL-AI-enabled-Container is a Retinopathy detection demo Container on Intel 12&13th Gen CPU and iGPU. 

### Key Features

- **AI Application Demo:** Retinopathy detection
- **Hardware Acceleration:** Optimized access to CPU, iGPU.
- **Complete AI Framework Stack:** OpenVINO
- **Industrial Vision Support:** Accelerated OpenCV 
- **Edge AI Capabilities:** Support for computer vision


## Hardware Specifications

| Component | Specification |
|-----------|---------------|
| Target Hardware | ARK-3534 |
| iGPU | Intel UHD Graphics 770 |
| Memory | 16 ~ 64 GB shared CPU memory |
| OpenVINO Runtime SDK | 2023.1.0.12185 |

## Software Components

| Component | Version | Description |
|-----------|---------|-------------|
| OpenVINO Runtime| 2023.1.0.12185 |  OpenVINO Runtime provides AI framework run Model inference, and deploy applications |
| OpenCV | 4.7.0 | Computer vision library |


## Supported AI Capabilities

## Vision Models

| Model Family | Versions | Performance (FPS) | Quantization Support |
|--------------|----------|-------------------|---------------------|
| YOLO | X | YOLOX: 7 @ 1280x720 | INT8, FP16, FP32 |


## Quick Start Guide

### Run on CPU

```bash
sudo docker run -it --privileged=true --ipc host --device /dev/dri:/dev/dri --device-cgroup-rule='c 189:* rmw' -v /tmp/.X11-unix:/tmp/.X11-unix -v /dev/bus/usb:/dev/bus/usb -u root --env DISPLAY=:0  --rm openvino2023.0.1_adf_eye:20231019 /bin/bash -c  "~/omz_demos_build/intel64/Release/object_detection_demo -i /opt/intel/openvino/Eye/object_detection/video/output_4288_2848_FPS=1.mp4 -m /opt/intel/openvino/Eye/object_detection/model-test/last_epoch_ckpt-opset-10.xml -at yolox -output_resolution 1280x720 -t 0.9 -labels "/opt/intel/openvino_2023.0.1.11005/Eye/Eye.labels"" -loop -d CPU

```

### Run on iGPU

```bash
sudo docker run -it --privileged=true --ipc host --device /dev/dri:/dev/dri --device-cgroup-rule='c 189:* rmw' -v /tmp/.X11-unix:/tmp/.X11-unix -v /dev/bus/usb:/dev/bus/usb -u root --env DISPLAY=:0  --rm openvino2023.0.1_adf_eye:20231019 /bin/bash -c  "~/omz_demos_build/intel64/Release/object_detection_demo -i /opt/intel/openvino/Eye/object_detection/video/output_4288_2848_FPS=1.mp4 -m /opt/intel/openvino/Eye/object_detection/model-test/last_epoch_ckpt-opset-10.xml -at yolox -output_resolution 1280x720 -t 0.9 -labels "/opt/intel/openvino_2023.0.1.11005/Eye/Eye.labels"" -loop -d GPU

```

Copyright © 2025 Advantech Corporation. All rights reserved.

