# LLM Quantization

Maintainers - [Aaron Zhao](https://aaron-zhao123.github.io/) and [Cheng Zhang](https://chengzhang-98.github.io/blog/)

A curated list of neural radiance field (NeRF) papers. 

## Table of Contents

- [Papers](#papers)
- [Surveys](#surveys)

---

## Papers

|  Title  |   Year   |   Venue  |   Code   |   Notes  |
|:--------|:--------:|:--------:|:--------:|:--------:|
| [NeRF: Representing Scenes as Neural Radiance Fields for View Synthesis](https://arxiv.org/abs/2003.08934) | 2020 | ECCV | [TF (Original)](https://github.com/bmild/nerf); [Torch](https://github.com/yenchenlin/nerf-pytorch) | [Notes](#nerf-representing-scenes-as-neural-radiance-fields-for-view-synthesis) |
| [ICARUS: A Specialized Architecture for Neural Radiance Fields Rendering](https://arxiv.org/pdf/2203.01414.pdf) | 2022 | Arxiv | - | - |

---

## Surveys

|  Title  |   Year   |   Venue  |   Code   |
|:--------|:--------:|:--------:|:--------:|
| [NeRF: Neural Radiance Field in 3D Vision, Introduction and Review](https://arxiv.org/pdf/2210.00379.pdf) | - | - | - |

---

## Notes

### NeRF: Representing Scenes as Neural Radiance Fields for View Synthesis

This is the first paper introducing NeRF. A 3D scene is modelled as a radiance field - a 5D continuous function mapping each point in the scene, and the direction at which the point is being observed, to a colour and opacity. The inputs to this function are the 3D coordinates of a point in the scene and the 2D 'viewing direction' (the direction from which the point is being observed). The output of the function is the RGB colour of the point, and the colour density of the point.

The authors find that the radiance field function can be approximated by a shallow MLP. A NeRF dataset consists of many pictures of a single scene taken from different viewing directions. Points in the scene are sampled by shooting camera rays from different pixels of a view. The MLP is trained to reduce the loss between the predicted colour and density of a point and its 'real' value obtained by sampling. 

(This explanation is very simplified.)