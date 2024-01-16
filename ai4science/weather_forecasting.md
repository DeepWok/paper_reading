
# Neural Weather Forecasting

Maintainers - [Aaron Zhao](https://aaron-zhao123.github.io/) and [Cheng Zhang](https://chengzhang-98.github.io/blog/)

A curated list of papers about weather forecasting using data driven approaches i.e. machine learning. 


## Model Comparison

KeislerNet (2022)

- deterministic model
- 1 degree resolution
- competitve performance versus ECMWF-HRES, NOAA-GFS

FourCastNet (2022)

- first 0.25 degree model
- competitive performance against HRES on some variables

Pangu-Weather (2022)

- 0.25 deg 7-day lead times
- outperformed HRES on more variables
- outperformed FourCast Net

GraphCast (2023)

- 0.25 deg 10-day lead times
- definitvely outperforms HRES (better on 90% of lead-time / variable combinations)

FengWu (2023)

https://arxiv.org/abs/2304.02948

- 0.25 deg 10-day lead times
- transformer based
- replay buffer mechanism
- competitive performance with GraphCast (better on 80% reported metrics)

Stormer (2023)

https://arxiv.org/abs/2312.03876

- 1.4 deg - outperforms HRES and GraphCast on lower resolution
- transformer based

Fuxi (2023)

https://www.nature.com/articles/s41612-023-00512-1

- cascade model
    - combine several different models each fine tuned for a different forecast window

GenCast (2023)

https://arxiv.org/abs/2312.15796

- previous models generate a single deterministic forecast which minimises mean error
    - this causes features to be oversmoothed
- use a diffusion model to generate an ensemble of predictions
    - more closely aligned with NWP


## Timeline of papers for Graph Neural Networks for Weather / Physics

**Neural LAM (2023)**

https://arxiv.org/abs/2309.17370

- inspired by GraphCast and MultiScaleGraphNets
- use a hierarchal (multi-layer) mesh for message passing
- first to investigate weather forecasting in a local area
- NeurIPS 2023


**GraphCast (2023)**

https://arxiv.org/abs/2212.12794

- inspired by KeislerNet
- use a multi-scale icosahedral mesh to allow message passing over longer distances
- first NeurWP to definitively outperform HRES


**Keisler (Graph Weather) (2022)**

https://arxiv.org/pdf/2202.07575.pdf

- first paper applying GNNs for weather forecasting
- icosahedral mesh across globe
- inspired by MeshGraphNets
- matches HRES performance


************************************************Multiscale MeshGraphNets (2022)************************************************

https://arxiv.org/pdf/2210.00612.pdf

- Improves over MeshGraphNets
- **************Problem:**************
    - spatial convergence
- ******************Solution******************
    - hierarchal graph

**************************MeshGraphNets (2021)**************************

https://arxiv.org/pdf/2010.03409.pdf

- ****************Problem:****************
    - mesh-based finite element simulations are important in various areas
        - mechanics, aerodynamics, electromagnetics
    - however they are expensive to run
- **************************Contribution:**************************
    - apply Graph Neural Networks to mesh simulation problem
    - ‘learn’ a simulator by using large amounts of mesh data
    - developed MeshGraphNets framework
    - adaptive meshes?

**Learning to simulate
complex physics with graph networks (2020)**

https://arxiv.org/abs/2002.09405

- introduces encode - decode - process architecture for GNN models

**Relational Inductive Biases (2018)**

https://arxiv.org/pdf/1806.01261.pdf

- review/unification paper giving a general, high level view about ‘relational inductive bias’
- formalises recent research about different architectures
- propose ‘graph neural network’ as a building block

**Graph Attention Networks (2018)**

https://arxiv.org/abs/1710.10903

- generalising graph convolution networks by learning aggregation weights

****************************************Interaction Networks (2016)****************************************

https://arxiv.org/abs/1612.00222