# Deep Learning with OpenCV 3 — Visual Studio 2015 Win32

[![C++](https://img.shields.io/badge/C%2B%2B-14-blue)](https://isocpp.org/)
[![OpenCV](https://img.shields.io/badge/OpenCV-3.x-5C3EE8?logo=opencv&logoColor=white)](https://opencv.org/)
[![Visual Studio](https://img.shields.io/badge/Visual%20Studio-2015-purple?logo=visualstudio&logoColor=white)](https://visualstudio.microsoft.com/)
[![Windows](https://img.shields.io/badge/Windows-Win32-0078D4?logo=windows&logoColor=white)](https://www.microsoft.com/windows)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Deep Learning integration with OpenCV 3 DNN module — Visual Studio 2015 Win32 build configuration.

## Overview

Setup and examples for using OpenCV 3's Deep Neural Network (DNN) module on Windows with Visual Studio 2015 (Win32/x86 configuration). Demonstrates loading and running pre-trained deep learning models for image classification, object detection, and segmentation.

## Supported Models (OpenCV 3 DNN)

| Model | Framework | Use Case |
|-------|-----------|----------|
| **Caffe** | Caffe/Caffe2 | Image classification, detection |
| **TensorFlow** | TF 1.x/2.x | Classification, detection, segmentation |
| **ONNX** | ONNX Runtime | Cross-framework model inference |
| **Torch/PyTorch** | Torch | Classification, feature extraction |
| **Darknet** | YOLO | Real-time object detection |

## Modern Alternatives (2025-2026)

OpenCV 3 on VS2015 Win32 is legacy. For current projects:

### Recommended Stack

| Component | Recommendation | Notes |
|-----------|---------------|-------|
| **IDE** | Visual Studio 2022 | Latest with C++20 support |
| **OpenCV** | OpenCV 4.10+ | DNN module with more backends |
| **Compiler** | MSVC 14.3+ (v143) | C++17/20 support |
| **Architecture** | x64 | Modern hardware is 64-bit |
| **GPU** | CUDA 12.x + cuDNN | GPU-accelerated inference |
| **Model Format** | ONNX | Cross-framework standard |

### Modern Inference Backends

| Backend | Speed | Hardware | Best For |
|---------|-------|----------|----------|
| **TensorRT** | Fastest | NVIDIA GPU | Production NVIDIA deployment |
| **ONNX Runtime** | Fast | CPU/GPU/NPU | Cross-platform deployment |
| **OpenCV DNN** | Good | CPU/GPU | Quick prototyping |
| **OpenVINO** | Fast | Intel CPU/VPU/GPU | Intel hardware |
| **DirectML** | Fast | Any GPU | Windows-native acceleration |
| **Core ML** | Fast | Apple Neural Engine | macOS/iOS deployment |

### Migration Path

1. **Upgrade OpenCV**: 3.x → 4.10+ (backward compatible)
2. **Upgrade VS**: 2015 → 2022 (better C++ standard support)
3. **Switch to x64**: Drop Win32 for modern hardware
4. **Use ONNX format**: Export models to ONNX for portability
5. **Add TensorRT**: GPU-accelerated inference for NVIDIA hardware

### Key Improvements in OpenCV 4.x DNN

- **ONNX model support** — Native loading without conversion
- **NVIDIA CUDA backend** — GPU-accelerated inference
- **Intel OpenVINO backend** — Optimized for Intel hardware
- **Layer fusion** — Automatic graph optimization
- **Quantization support** — INT8 inference
- **Backend selection API** — Choose optimal inference backend at runtime

## Build Instructions (VS2015 Legacy)

```
1. Install OpenCV 3.x with contrib modules
2. Create Win32 Console Application in VS2015
3. Configure include/lib paths to OpenCV
4. Link: opencv_world3xx.lib
5. Set platform to Win32 (x86)
6. Build and run
```

## Modern Build (Recommended)

```cmake
# CMakeLists.txt
cmake_minimum_required(VERSION 3.20)
project(DeepLearningCV)

find_package(OpenCV 4.10 REQUIRED)
add_executable(main main.cpp)
target_link_libraries(main ${OpenCV_LIBS})
```

## References

- OpenCV DNN Module Documentation (2024): https://docs.opencv.org/4.x/d6/d0f/tutorial_dnn_bottom.html
- TensorRT Developer Guide (2024): https://developer.nvidia.com/tensorrt
- ONNX Runtime Documentation (2024): https://onnxruntime.ai/docs/

## Author

**Dr. Farshid Pirahansiah** — [LinkedIn](https://linkedin.com/in/pirahansiah) | [GitHub](https://github.com/pirahansiah)
