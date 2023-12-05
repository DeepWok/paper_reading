# Hardware Aware ViT accelerator

## Table of Contents

- [Year 2023](#2023)
- [Year 2022](#2022)
- [Surveys](#awesome-surveys)
- [Implementation references](#implementation-references)
  - [Cuda kernels for quantization](#cuda-kernels-for-quantization)

---
### 2023

|  Title  |   Venue  |   Code   |   Notes  |
|:--------|:--------:|:--------:|:--------:|
| [HeatViT: Hardware-Efficient Adaptive Token Pruning for Vision Transformers](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10071047) | HPCA | - | [HeatViT](#heatvit-hardware-efficient-adaptive-token-pruning-for-vision-transformers) |
| [An Integer-Only and Group-Vector Systolic Accelerator for Efficiently Mapping Vision Transformer on Edge](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10288182) | TCAS | - | - |
### 2022

|  Title  |   Venue  |   Code   |   Notes  |
|:--------|:--------:|:--------:|:--------:|
| [Auto-ViT-Acc: An FPGA-Aware Automatic Acceleration Framework for Vision Transformer with Mixed-Scheme Quantization](https://ieeexplore.ieee.org/document/10035108) | FPL | - | [AUTO-ViT](#auto-vit-acc-an-fpga-aware-automatic-acceleration-framework-for-vision-transformer-with-mixed-scheme-quantization) |
| [ViA: A Novel Vision-Transformer Accelerator Based on FPGA](<https://ieeexplore.ieee.org/abstract/document/9925700?casa_token=_ScpTJ28nSsAAAAA:X-N9eboJZLvOhryk_1UAaWm__tu_KKo9djadmtZcaFgRxDVcfX28YzFyElTy-hJDk8tgBLk>) | TCAD | - | [ViA](#via-a-novel-vision-transformer-accelerator-based-on-fpga) |
---

---

### Surveys

---

### Notes

#### Auto-ViT-Acc: An FPGA-Aware Automatic Acceleration Framework for Vision Transformer with Mixed-Scheme Quantization

This paper is the first FPGA-based ViT Framework. On software part, it employs a **mixed-quantization** (PoT(mainly on LUT) + Fixed-point(mainly on DSP)) to optimize  FPGA resource utilization. On hardware part, the framework is constructed by **HLS**. To address challenges arising from layer-wise multi-precision, it **aligns** the output of different quantization schemes, and uses the same ratio of fixed-point to PoT for each head. Parameter tuning is performed by initially fixing Frames Per Second (FPS), then determining the precision and scheme combination, and finally adjusting other parameters based on resource utilization estimates.

#### ViA: A Novel Vision-Transformer Accelerator Based on FPGA

This paper introduces a novel Vision-Transformer Accelerator designed to address two challenges present in ViT and its variants. One is the path dependency introduced by the shortcut machanism(residual add). The solution involves a half layer mapping technique, leveraging two kinds of hardware design patterns. By incorporating two reuse engines(MSA, MLP) and implementing the streaming pattern within engines. Residual add is relocated from the end of current engine to the start of next engine. The paper also analyzes the data locality of different input dimension of to facilitate parallel computation. It was tested using HLS to generate hardware code and run on a FPGA. To be noted, the data precision used is float16.

#### HeatViT: Hardware-Efficient Adaptive Token Pruning for Vision Transformers

Pruned ViT
