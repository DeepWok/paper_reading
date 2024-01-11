# LLM Quantization

Maintainers - [Aaron Zhao](https://aaron-zhao123.github.io/) and [Cheng Zhang](https://chengzhang-98.github.io/blog/)

A curated list of LLM Quantization papers, partially taken from Sudarsharm Sreeram's [initial effort](<https://www.craft.me/s/WLFc7B9zgH4ncz>).

## Table of Contents

- [Year 2023](#2023)
- [Year 2022](#2022)
- [Surveys](#awesome-surveys)
- [Implementation references](#implementation-references)
  - [Cuda kernels for quantization](#cuda-kernels-for-quantization)

---

### 2024

| Title                                                                                                                                                 | Venue | Code | Notes                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-------|------|------------------------------------------------------------------|
| [LRQ: Optimizing Post-Training Quantization for Large Language Models by Learning Low-Rank Weight-Scaling Matrices](https://arxiv.org/abs/2309.14717) | Arxiv | -    | PTQ, A low-rank version of FlexRound with fewer trainable params |

### 2023

| Title                                                                                                                                            |  Venue  |                            Code                            |                                           Notes                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------:|:----------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| [AffineQuant: Affine Transformation Quantization for Large Language Models](https://openreview.net/forum?id=of2rhALq8l)                          |  ICLR   | [Github](https://github.com/anonymousiclr1842/AffineQuant) |                                         PTQ, SVD                                          |
| [AWQ: Activation-aware weight quantization for LLM compression and acceleration](https://arxiv.org/abs/2306.00978)                               |  Arxiv  |      [Github](https://github.com/mit-han-lab/llm-awq)      |                                             -                                             |
| [BitNet: Scaling 1-bit Transformers for Large Language Models](<https://arxiv.org/abs/2310.11453>)                                               |  Arxiv  |                             -                              |                                             -                                             |
| [Boost Transformer-based Language Models with GPU-Friendly Sparsity and Quantization](https://aclanthology.org/2023.findings-acl.15.pdf)         |   ACL   |                             -                              |                                             -                                             |
| [Enhancing Computation Efficiency in Large Language Models through Weight and Activation Quantization](https://openreview.net/pdf?id=4Ggw1DsgRQ) |  EMNLP  |                             -                              |                       SmoothQuant for some layers, AWQ for others?                        |
| [FlexRound: Learnable Rounding based on Element-wise Division for Post-Training Quantization](https://arxiv.org/abs/2306.00317)                  |  PMLR   |      [Github](https://github.com/microsoft/DeepSpeed)      |               Does this method really benefit hardware? I doubt it doesn't                |
| [GPTQ: Accurate Post-Training Quantization for Generative Pre-trained Transformers](https://arxiv.org/abs/2210.17323)                            |  ICLR   |        [Github](https://github.com/IST-DASLab/gptq)        |                                             -                                             |
| [INT-FP-QSim: Mixed precision and formats for large language models and vision transformers](https://arxiv.org/abs/2307.03712)                   |  Arxiv  |  [Github](https://github.com/lightmatter-ai/INT-FP-QSim)   |                                             -                                             |
| [Integer or Floating Point? New Outlooks for Low-Bit Quantization on Large Language Models](https://arxiv.org/abs/2305.12356)                    |  Arxiv  |                             -                              |                                             -                                             |
| [LLM-QAT: Data-Free Quantization Aware Training for Large Language Models](<https://arxiv.org/abs/2306.00978>)                                   |  Arxiv  |   [Github](https://github.com/facebookresearch/LLM-QAT)    |                                             -                                             |
| [LoftQ: LoRA-Fine-Tuning-Aware Quantization for Large Language Models](https://arxiv.org/abs/2310.08659v4)                                       |  Arxiv  |        [Github](https://github.com/yxli2123/LoftQ)         |            Uses iterative SVD to initialize low-rank A, B in QLoRA style PEFT             |
| [Memory-efficient fine-tuning of compressed large language models via sub-4-bit integer quantisation](https://arxiv.org/abs/2305.14152)          |  Arxiv  |        [Github](https://github.com/artidoro/qlora)         |                                             -                                             |
| [Microscaling Data Formats for Deep Learning](https://arxiv.org/abs/2310.10537)                                                                  |  Arxiv  |    [Github](https://github.com/microsoft/microxcaling)     |                                             -                                             |
| [OmniQuant: Omnidirectionally Calibrated Quantization for Large Language Models](https://arxiv.org/abs/2308.13137)                               |  ICLR   |      [Github](https://github.com/OpenGVLab/OmniQuant)      |  PTQ, uses SGD to learn row/column scaling factors and fuses them back like SmoothQuant   |
| [PB-LLM: Partially Binarized Large Language Models](https://arxiv.org/pdf/2310.00034.pdf)                                                        |  ICLR   |        [Github](https://github.com/hahnyuan/PB-LLM)        |                             QAT, Partially binary weight LLM                              |
| [PreQuant: A Task-agnostic Quantization Approach for Pre-trained Language Models](https://arxiv.org/abs/2306.00014)                              |   ACL   |                             -                              |                                             -                                             |
| [QA-LoRA: Quantization-Aware Low-Rank Adaptation of Large Language Models](https://arxiv.org/pdf/2309.14717.pdf)                                 |  ICLR   |      [Github](https://github.com/yuhuixu1993/qa-lora)      |                                      Quantized PEFT                                       |
| [QLoRA: Efficient Finetuning of Quantized LLMs](https://arxiv.org/abs/2305.14314)                                                                | NeurIPS |        [Github](https://github.com/artidoro/qlora)         |                                             -                                             |
| [Quantizable Transformers: Removing Outliers by Helping Attention Heads Do Nothing](<https://arxiv.org/abs/2306.12929>)                          |  Arxiv  |    [Github](https://github.com/SqueezeAILab/SqueezeLLM)    | [Note](#quantizable-transformers-removing-outliers-by-helping-attention-heads-do-nothing) |
| [QuIP: 2-bit quantisation of large language models with guarantees](https://arxiv.org/abs/2307.13304)                                            |  Arxiv  |        [Github](https://github.com/jerry-chee/QuIP)        |                                             -                                             |
| [SmoothQuant: Accurate and Efficient Post-Training Quantization for Large Language Models](https://arxiv.org/abs/2211.10438)                     |  ICML   |    [Github](https://github.com/mit-han-lab/smoothquant)    |                                             -                                             |
| [SpQR: A sparse-quantised representation for near-lossless LLM weight compression](https://arxiv.org/abs/2306.03078)                             |  Arxiv  |         [Github](https://github.com/Vahe1994/SpQR)         |           PTQ, smaller block size and more quantization scalars and zero-points           |
| [SqueezeLM: Dense-and-sparse quantisation](https://arxiv.org/abs/2307.03712)                                                                     |  Arxiv  |  [Github](https://github.com/lightmatter-ai/INT-FP-QSim)   |                                             -                                             |
| [The case for 4-bit precision: k-bit Inference Scaling Laws](<https://arxiv.org/abs/2212.09720>)                                                 |  ICML   |                             -                              |                                             -                                             |
| [Understanding INT4 Quantization for Transformer Models: Latency Speedup, Composability, and Failure Cases](https://arxiv.org/abs/2301.12017)    |  ICML   |                             -                              |                                             -                                             |
| [With Shared Microexponents, A Little Shifting Goes a Long Way](https://arxiv.org/abs/2302.08007)                                                |  ISCA   |                             -                              |                                             -                                             |
| [ZeroQuant-FP: A leap forward in LLMs post-training W4A8 quantisation using floating-point formats](https://arxiv.org/abs/2307.09782)            |  Arxiv  |        [Github](https://github.com/jerry-chee/QuIP)        |                                             -                                             |
| [ZeroQuant-V2: Exploring post-training quantisation in LLMs from comprehensive study to low rank compensation](https://arxiv.org/abs/2303.08302) |  Arxiv  |                             -                              |                                             -                                             |

---

### 2022

| Title                                                                                                                           | Venue |                         Code                          | Notes |
|:--------------------------------------------------------------------------------------------------------------------------------|:-----:|:-----------------------------------------------------:|:-----:|
| [LLM.int8(): 8-bit matrix multiplication for transformers at scale](https://arxiv.org/abs/2208.07339)                           | Arxiv | [Github](https://github.com/TimDettmers/bitsandbytes) |   -   |
| [ZeroQuant: Efficient and Affordable Post-Training Quantization for Large-Scale Transformers](https://arxiv.org/abs/2206.01861) | Arxiv |   [Github](https://github.com/microsoft/DeepSpeed)    |   -   |

---

### Surveys

| Title                                                                                       | Venue | Type | Code |
|:--------------------------------------------------------------------------------------------|:-----:|:----:|:----:|
| [A survey on model compression for large language models](https://arxiv.org/abs/2308.07633) |   -   |  -   |  -   |

### Implementation references

#### Cuda kernels for quantization

| Name                                                            | Notes                                |
|:----------------------------------------------------------------|:-------------------------------------|
| [BitsandBytes](https://github.com/TimDettmers/bitsandbytes)     | Tim Dettmers, LLM.int8(), Single GPU |
| [DeepSpeed](https://github.com/microsoft/DeepSpeed)             | Microsoft, Multi-GPU                 |
| [Flash Attention](https://github.com/Dao-AILab/flash-attention) | Dao-AILab (CS Princeton), Single GPU |
| [Megatron-LM](https://github.com/NVIDIA/Megatron-LM)            | NVIDIA, Multi-GPU                    |
| [MXScaling](https://github.com/microsoft/microxcaling)          | Microsoft, MX                        |

---

### Notes

#### Quantizable Transformers: Removing Outliers by Helping Attention Heads Do Nothing

This paper address this with a new Dense-and-Sparse Quantization method. Dense-and-Sparse splits weight matrices into two components: A dense component that can be heavily quantized without affecting model performance, as well as a sparse part that preserves sensitive and outlier parts of the weight matrices With this approach, we are able to serve larger models with smaller memory footprint, the same latency, and yet higher accuracy and quality. For instance, the Squeeze variant of the Vicuna models can be served within 6 GB of memory and reach 2% higher MMLU than the baseline model in FP16 with an even 2x larger memory footprint.
