# LLM Quantization

Maintainers - [Aaron Zhao](https://aaron-zhao123.github.io/) and [Cheng Zhang](https://chengzhang-98.github.io/blog/)

A curated list of LLM Quantization papers, partially taken from Sudarsharm Sreeram's [initial effort](<https://www.craft.me/s/WLFc7B9zgH4ncz>).

## Table of Contents

- [Year 2023](#2020)
- [Year 2022](#2019)
- [Surveys](#awesome-surveys)
- [Implementation references](#implementation-references)
  - [Cuda kernels for quantization](#cuda-kernels-for-quantization)

---

### 2023

|  Title  |   Venue  |   Code   |   Notes  |
|:--------|:--------:|:--------:|:--------:|
| [BitNet: Scaling 1-bit Transformers for Large Language Models](<https://arxiv.org/abs/2310.11453>) | Arxiv | - | - |
| [Microscaling Data Formats for Deep Learning](https://arxiv.org/abs/2310.10537) | Arxiv | [Github](https://github.com/microsoft/microxcaling) | - |
| [With Shared Microexponents, A Little Shifting Goes a Long Way](https://arxiv.org/abs/2302.08007) | ISCA | - | - |
| [QuIP: 2-bit quantisation of large language models with guarantees](https://arxiv.org/abs/2307.13304) | Arxiv | [Github](https://github.com/jerry-chee/QuIP) | - |
| [ZeroQuant-FP: A leap forward in LLMs post-training W4A8 quantisation using floating-point formats](https://arxiv.org/abs/2307.09782) | Arxiv | [Github](https://github.com/jerry-chee/QuIP) | - |
| [INT-FP-QSim: Mixed precision and formats for large language models and vision transformers](https://arxiv.org/abs/2307.03712) | Arxiv | [Github](https://github.com/lightmatter-ai/INT-FP-QSim) | - |
| [SqueezeLM: Dense-and-sparse quantisation](https://arxiv.org/abs/2307.03712) | Arxiv | [Github](https://github.com/lightmatter-ai/INT-FP-QSim) | - |
| [Quantizable Transformers: Removing Outliers by Helping Attention Heads Do Nothing](<https://arxiv.org/abs/2306.12929>) | Arxiv | [Github](https://github.com/SqueezeAILab/SqueezeLLM) | [Note](#quantizable-transformers-removing-outliers-by-helping-attention-heads-do-nothing) |
| [SpQR: A sparse-quantised representation for near-lossless LLM weight compression](https://arxiv.org/abs/2306.03078) | Arxiv | [Github](https://github.com/Vahe1994/SpQR) | - |
| [AWQ: Activation-aware weight quantization for LLM compression and acceleration](https://arxiv.org/abs/2306.00978) | Arxiv | [Github](https://github.com/mit-han-lab/llm-awq) | - |
| [LLM-QAT: Data-Free Quantization Aware Training for Large Language Models](<https://arxiv.org/abs/2306.00978>) | Arxiv | [Github](https://github.com/facebookresearch/LLM-QAT) | - |
| [ZeroQuant-V2: Exploring post-training quantisation in LLMs from comprehensive study to low rank compensation](https://arxiv.org/abs/2303.08302) | Arxiv | - | - |
| [QLoRA: Efficient Finetuning of Quantized LLMs](https://arxiv.org/abs/2305.14314) | Arxiv | [Github](https://github.com/artidoro/qlora) | - |
| [Memory-efficient fine-tuning of compressed large language models via sub-4-bit integer quantisation](https://arxiv.org/abs/2305.14152) | Arxiv | [Github](https://github.com/artidoro/qlora) | - |
| [Integer or Floating Point? New Outlooks for Low-Bit Quantization on Large Language Models](https://arxiv.org/abs/2305.12356) | Arxiv | - | - |
| [Understanding INT4 Quantization for Transformer Models: Latency Speedup, Composability, and Failure Cases](https://arxiv.org/abs/2301.12017) | ICML | - | - |
| [The case for 4-bit precision: k-bit Inference Scaling Laws](<https://arxiv.org/abs/2212.09720>) | ICML | - | - |
| [SmoothQuant: Accurate and Efficient Post-Training Quantization for Large Language Models](https://arxiv.org/abs/2211.10438) | ICML | [Github](https://github.com/mit-han-lab/smoothquant) | - |
| [FlexRound: Learnable Rounding based on Element-wise Division for Post-Training Quantization](https://arxiv.org/abs/2306.00317) | ICML | [Github](https://github.com/microsoft/DeepSpeed) | - |
| [GPTQ: Accurate Post-Training Quantization for Generative Pre-trained Transformers](https://arxiv.org/abs/2210.17323) | ICLR | [Github](https://github.com/IST-DASLab/gptq) | - |
| [PreQuant: A Task-agnostic Quantization Approach for Pre-trained Language Models](https://arxiv.org/abs/2306.00014) | ACL | - | - |
| [Boost Transformer-based Language Models with GPU-Friendly Sparsity and Quantization](https://aclanthology.org/2023.findings-acl.15.pdf) | ACL | - | - |

---

### 2022

|  Title  |   Venue  |   Code   |   Notes  |
|:--------|:--------:|:--------:|:--------:|
| [ZeroQuant: Efficient and Affordable Post-Training Quantization for Large-Scale Transformers](https://arxiv.org/abs/2206.01861) | Arxiv | [Github](https://github.com/microsoft/DeepSpeed) | - |
| [LLM.int8(): 8-bit matrix multiplication for transformers at scale](https://arxiv.org/abs/2208.07339) | Arxiv | [Github](https://github.com/TimDettmers/bitsandbytes) | - |

---

### Surveys

|  Title  |   Venue  |   Type   |   Code   |
|:--------|:--------:|:--------:|:--------:|
| [A survey on model compression for large language models](https://arxiv.org/abs/2308.07633) | - | - | - |

### Implementation references

#### Cuda kernels for quantization

| Name |  Notes  |
|:--------|:--------|
| [DeepSpeed](https://github.com/microsoft/DeepSpeed) | Microsoft, Multi-GPU |
| [Megatron-LM](https://github.com/NVIDIA/Megatron-LM) | NVIDIA, Multi-GPU |
| [Flash Attention](https://github.com/Dao-AILab/flash-attention) | Dao-AILab (CS Princeton), Single GPU |
| [BitsandBytes](https://github.com/TimDettmers/bitsandbytes)  | Tim Dettmers, LLM.int8(), Single GPU |
| [MXScaling](https://github.com/microsoft/microxcaling) | Microsoft, MX |

---

### Notes

#### Quantizable Transformers: Removing Outliers by Helping Attention Heads Do Nothing

This paper address this with a new Dense-and-Sparse Quantization method. Dense-and-Sparse splits weight matrices into two components: A dense component that can be heavily quantized without affecting model performance, as well as a sparse part that preserves sensitive and outlier parts of the weight matrices With this approach, we are able to serve larger models with smaller memory footprint, the same latency, and yet higher accuracy and quality. For instance, the Squeeze variant of the Vicuna models can be served within 6 GB of memory and reach 2% higher MMLU than the baseline model in FP16 with an even 2x larger memory footprint.
