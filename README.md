# Renaissance Capstone Project 2020

This project aims to create a framework for applying Local Differential Privacy (LDP) to data analysis using Federated Learning (FL). This framework allows multiple parties to cooperate in training the same model even if they have different end goals, overcoming the problem of model heterogeneity.

## Table of Contents

- [Renaissance Capstone Project 2020](#renaissance-capstone-project-2020)
  - [Table of Contents](#table-of-contents)
  - [Getting Started](#getting-started)
    - [Conda Pre-Installation](#conda-pre-installation)
      - [For Windows/Linux](#for-windowslinux)
      - [For OSX](#for-osx)
    - [Installation](#installation)
    - [Running the Code](#running-the-code)

## Getting Started

This project currently uses the [Pysyft](https://github.com/OpenMined/PySyft) Library for Federated Learning built on the [Pytorch](https://github.com/pytorch/pytorch) Python Package. The Differential Privacy is coded into the model optimizer.

> Note that Python 3.7 should be used as some of the libraries do not support newer versions of Python.

### Conda Pre-Installation

Conda is a virtual environment manager for Python that will make package management much easier.

First, download the appropriate version of [Miniconda](https://docs.conda.io/en/latest/miniconda.html) for your system. This is a more lightweight version of Anaconda that will suit our purposes.

Run the following commands in the Conda prompt (directory not important). The current environment being used can be seen at the start of the command line in parentheses, initially set as `(base)`.

```bash
conda create -n rcp2020 python=3.7
conda activate rcp2020
```

At this point, the environment should change from `(base)` to `(rcp2020)`. Run the following commands.

#### For Windows/Linux

```bash
# Run for CUDA 9.2
conda install pytorch==1.4.0 torchvision==0.5.0 cudatoolkit=9.2 -c pytorch

# Run for CUDA 10.1
conda install pytorch==1.4.0 torchvision==0.5.0 cudatoolkit=10.1 -c pytorch

# Run for CPU Only
conda install pytorch==1.4.0 torchvision==0.5.0 cpuonly -c pytorch
```

#### For OSX

```bash
conda install pytorch==1.4.0 torchvision==0.5.0 -c pytorch
```

### Installation

Run these commands in bash to install Pysyft and Jupyter Notebook

<!-- This is for when Opacus decides to support windows :3 -->
<!-- pip install opacus
conda install torchcsprng=1.0.2 cpuonly -c pytorch -->

```bash
pip install syft[udacity]==0.2.9
conda install jupyter notebook==5.7.8 tornado==4.5.3
```

### Running the Code

To begin running the code, ensure the right conda environment is activated and run the following command in the git directory.

```bash
conda activate rcp2020
jupyter notebook
```
