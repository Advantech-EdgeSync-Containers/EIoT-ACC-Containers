# ACC-L2-01-Qualocmm-AI-enabled-Container


**Version:** 1.0  
**Release Date:** April 2025  
**Copyright:** © 2025 Advantech Corporation. All rights reserved.

## Overview

The ACC-L2-01-Qualocmm-AI-enabled-Container provides a pre-configured Qualcomm SNPE, QIM SDK runtime environment with GPU/DSP passthrough capabilities, designed for industrial AI and machine learning applications. This solution simplifies the deployment of GPU/DSP-accelerated workloads in edge computing environments while ensuring consistent, reproducible results across development and production environments 

### Key Features

- **Hardware Acceleration:** Optimized access to iGPU, DSP
- **Complete AI Framework Stack:** Qualcomm IM SDK, SNPE
- **Edge AI Capabilities:** Support for computer vision


## Hardware Specifications

| Component | Specification |
|-----------|---------------|
| Target Hardware | AOM-2721 |
| CPU | QCS6490 |
| iGPU | Andreo GPU 643 |
| DSP | Hexagon DSP |
| Memory | 8 GB |

## Prerequisite Software on Host OS

| Component | Version | Description |
|-----------|---------|-------------|
| LE Yocto Linux | 1.3 | LE1.3 BSP |

## Software Components

| Component | Version | Description |
|-----------|---------|-------------|
| Qualcomm IM SDK | 2.0.0.r2 | QIM SDK is a unified environment for developing AI and multimedia use cases at the Edge on the Qualcomm® Linux platforms  |




## Quick Start Guide

### Run 

```bash
sudo docker run -it --privileged=true --ipc host --device /dev/dri:/dev/dri --device-cgroup-rule='c 189:* rmw' -v /tmp/.X11-unix:/tmp/.X11-unix -v /dev/bus/usb:/dev/bus/usb -u root --env DISPLAY=:0  --rm eiot/eas-intel-1213-retinopathy-demo:ubuntu22.04-1.0.0 /bin/bash -c  "~/omz_demos_build/intel64/Release/object_detection_demo -i /opt/intel/openvino/Eye/object_detection/video/output_4288_2848_FPS=1.mp4 -m /opt/intel/openvino/Eye/object_detection/model-test/last_epoch_ckpt-opset-10.xml -at yolox -output_resolution 1280x720 -t 0.9 -labels "/opt/intel/openvino_2023.0.1.11005/Eye/Eye.labels"" -loop -d CPU

```

Copyright © 2025 Advantech Corporation. All rights reserved.


