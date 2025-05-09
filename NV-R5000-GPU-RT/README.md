# ACC-L2-01-NVIDIA-RTX-AI-enabled-Container


**Version:** 1.0  
**Release Date:** April 2025  
**Copyright:** © 2025 Advantech Corporation. All rights reserved.

## Overview

The ACC-L2-01-NVIDIA-RTX-AI-enabled-Container provides a pre-configured CUDA, TensorRT, DeepStream development environment with GPUpassthrough capabilities, designed for industrial AI and machine learning applications. This solution simplifies the deployment of GPU-accelerated workloads in edge computing environments while ensuring consistent, reproducible results across development and production environments 

### Key Features

- **Hardware Acceleration:** Optimized access to GPU
- **Complete AI Framework Stack:** CUDA, TensorRT, DeepStream
- **Edge AI Capabilities:** Support for computer vision


## Hardware Specifications

| Component | Specification |
|-----------|---------------|
| Target Hardware | AIR-510 |
| Memory | 32 ~ 192 GB |
| GPU | RTX-A5000 |
| vRAM | 24 GB |


## Prerequisite Software on Host OS

| Component | Version | Description |
|-----------|---------|-------------|
| NVIDIA Driver | 535.171.04 | NVIDIA RTX Card Driver |
| nvidia-container-toolkit | 1.15.0 | It is an open-source suite of tools and libraries that enables Docker and other container runtimes to utilize NVIDIA GPUs. |
| nvidia-docker2 | 2.14.0 | nvidia-docker2 is a legacy package developed by NVIDIA to enable Docker containers to access NVIDIA GPU |
| Gstreamer | 1.20.3 | GStreamer is an open-source, cross-platform multimedia framework designed to build a wide range of media-handling applications. |

## Software Components

| Component | Version | Description |
|-----------|---------|-------------|
| CUDA | 12.0 | CUDA is a parallel computing platform and programming model developed by NVIDIA. It enables software developers to harness the power of NVIDIA GPUs for general-purpose processing  |
| TensorRT | 8.6.1.6 | TensorRT is a high-performance deep learning inference SDK designed to optimize and accelerate the deployment of trained neural networks on NVIDIA GPUs  |
| DeepStream | 6.4 | NVIDIA DeepStream is a high-performance AI streaming analytics SDK designed to help developers build applications that can analyze and understand real-time video and sensor data efficiently using NVIDIA GPU  |



## Quick Start Guide

### Run 

```bash
docker run -d --gpus all -it --rm --net=host --privileged -v /tmp/.X11-unix:/tmp/.X11-unix -e DISPLAY=$DISPLAY -w /opt/nvidia/deepstream/deepstream-6.4 eiot/nvidia-deepstream6.4:ubuntu22.04-1.0.0
```

Copyright © 2025 Advantech Corporation. All rights reserved.



