# ACC-L2-01-NXP-AI-enabled-Containers

# NXP-iMX-NPU-RT

This repository provides a runtime container for Advantech platforms based on the NXP i.MX8 series SoCs, leveraging the integrated NPU (Neural Processing Unit) for AI acceleration. The container includes essential runtime components such as `imx-nn` libraries and selected AI inference demos.

## Supported Platforms

- RSB-3720 (i.MX8M Plus)
- ROM-5720 (i.MX8M Plus)
- Other i.MX8MP-based boards with NPU support

## Prerequisites

- Docker installed on target device (see Getting Started guide)
- Yocto-based Linux image with container runtime support
- GPU/NPU enabled kernel and device tree
- Network access to pull containers

## Container Features

- Includes `imx-nn` runtime libraries (from NXP eIQ)
- Pre-installed inference models for object detection and image classification
- Built-in GStreamer support for camera and video input
- Lightweight and optimized for embedded deployment

## Getting Started

Please follow the [Getting Started with Docker](https://github.com/Advantech-EdgeSync-Containers/EIoT-ACC-Containers/blob/main/NXP-iMX-NPU-RT/Getting%20Started%20with%20Docker.pdf) guide to install Docker, enable GPU/NPU support, and pull the container.

### 1. Pull the Container

```bash
docker pull advantech/nxp-imx-npu-rt:latest
```

### 2. Run the Container

```bash
docker run -it --rm \
  --privileged \
  --network host \
  -v /dev:/dev \
  -v /tmp:/tmp \
  -v /run:/run \
  advantech/nxp-imx-npu-rt:latest
```


### 3. Run a Sample Inference

```bash
cd /opt/demo
./run_classification.sh
```

This repo will be used for EIoT Team to submit their container documentation, and detailed instructions and workflow can be found on Getting Started with Docker.pdf.

