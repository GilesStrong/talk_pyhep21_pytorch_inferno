[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/GilesStrong/talk_pyhep21_pytorch_inferno/HEAD)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/GilesStrong/talk_pyhep21_pytorch_inferno/blob/main/presentation.ipynb) 

# A PyTorch Drop-In Implementation of The INFERNO Algorithm

**Giles Strong, Originally presented at PyHEP 2021: https://indico.cern.ch/event/1019958/timetable/#21-pytorch-inferno**

The INFERence-aware Neural Optimisation (INFERNO) algorithm (de Castro and Dorigo, 2018 https://www.sciencedirect.com/science/article/pii/S0010465519301948), allows one to fully optimise neural networks for the task of statistical inference by including the effects of systematic uncertainties in the training. This has significant advantages for work in HEP, where the uncertainties are often only included right at the end of an analysis, and spoil the usage of classification as a proxy task to statistical inference.

The loss itself, however, can be somewhat difficult to integrate into traditional frameworks due to its requirements to access the model and the data at different points during the optimisation cycle. Including both a lightweight neural-network framework for PyTorch, and the required inference functions, the PyTorch-INFERNO package provides a "drop-in" implementation of the INFERNO loss. The package also aims to serve as a demonstration of how potential users can implement the loss themselves to drop into their framework of choice.

In this lightning talk, I will give a quick overview of both the algorithm and the package, a well as discuss some of the more general requirements for implementing the algorithm as a drop-in loss.

GitHub: https://github.com/GilesStrong/pytorch_inferno
Docs: https://gilesstrong.github.io/pytorch_inferno/
Blog-posts (part 1 of 5): https://gilesstrong.github.io/website/statistics/hep/inferno/2020/12/04/inferno-1.html

## Usage

### Local installation

- Either install using the pip  (`pip install -r requirements.txt`), or conda (`conda env create -f environment.yml` then `conda activate pytorch_inferno`).
- Launch jupyter (`jupyter notebook`)
- Open presentation.ipynb

### Binder

- Click the Binder badge at the top of the readme, or [here](https://mybinder.org/v2/gh/GilesStrong/talk_pyhep21_pytorch_inferno/HEAD)
- Binder sometimes crashes due to excessive computation and is generally slow. It is sufficient for viewing the presentation, though.

## Colab

- Click the Colab badge at the top of the readme, or [here](https://colab.research.google.com/github/GilesStrong/lumin/blob/main/presentation.ipynb)
- Colab doesn't allow one to view the presentation as slides, but does provide a more-stable computing environment.
