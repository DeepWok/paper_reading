# Diffusion Models and score-based generative models

Maintainers - [Bakhtiar Zadeh](https://bakhtiarz.github.io/)

A curated list of diffusion model papers, these are generative models based on probabilistic methods. The list is ordered by year and some notes are available (slightly opinionated)

This is a good video on this paper by the authors:[Elucidating the design space of diffusion models video](https://www.youtube.com/watch?v=T0Qxzf0eaio&list=WL&index=3&t=709s&pp=gAQBiAQB) 

A tutorial by Nvidia introducing diffusion models, covers many aspects and is overall very useful [Tutorial on Denoising Diffusion-based Generative Modeling: Foundations and Applications](https://www.youtube.com/watch?v=cS6JQpEY9cs&list=WL&index=4&t=535s&pp=gAQBiAQB)


| Title                                                                                                                                            |  Venue  |                             Year                              |                                                              Notes                                                              |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------:|:-------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------------------:|
| [Q-diffusion: Quantizing diffusion models]()|IEEE/CVF |2023| Quantisation on diffusion models, involves the timestep which is important.
| [Speed is all you need: On-device acceleration of large diffusion models via gpu-aware optimization]()|IEEE/CVF|2023|Some optimisations to be done on a system level to speed up inference.
| [Consistency Models](https://arxiv.org/abs/2303.01469)|ICML| 2023| One step generation greatly accelerating the inference process but has some drawbacks, builds from score-based generative modelling paper and other work.
| [Elucidating the design space of diffusion-based generative models](https://arxiv.org/abs/2206.00364)|NeurIPS| 2022| Good paper describing the entire design space of diffusion and score based generative models
| [High-resolution image synthesis with latent diffusion models](https://arxiv.org/abs/2112.10752) | CVPR | 2022 | Develops a diffusion model to operate in the latent space and achieves great resuts in terms of accuracy and latency
| [Diffusion models beat gans on image synthesis](https://arxiv.org/abs/2105.05233)| | 2021 | Shows the strength of diffusion models. 
| [Denoising diffusion implicit models](https://arxiv.org/abs/2010.02502)                               |  ICLR  |    2021        |             This paper builds on the theory and reduces sampling time by using a non-markovian reverse process. 
| [Score-based generative modeling through stochastic differential equations](https://arxiv.org/abs/2011.13456)                                               |  ICLR  | 2021 | Stochastic differential equation framework for representing diffusion models. Has pronounced benefits over the markovian representation.
|[Denoising Diffusion Probabilistic Models](https://proceedings.neurips.cc/paper/2020/hash/4c5bcfec8584af0d967f1ab10179ca4b-Abstract.html)                          |  NeurIPS   | 2020   |This paper introduced denoising diffusion models as a generative model and provides a lot of the foundational mathematics.
| [Generative Modeling by Estimating Gradients of the Data Distribution]()| NeurIPS| 2019 | Mathematical background for the score based generative models. A score function is a measure of the probability distrubution and is closely related to the denoising networks. 
| [Deep Unsupervised Learning using Nonequilibrium Thermodynamics](https://arxiv.org/abs/1503.03585)                                               |  PMLR  | 2015 | Original paper leading to the rise of diffusion probabilistic models        
---
