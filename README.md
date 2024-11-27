# Powerformer: A Section-adaptive Transformer for Power Flow Adjustment

[![License: Apache](https://img.shields.io/badge/License-Apache-blue.svg)](LICENSE)

This repo is building for the source code and corresponding data of paper 'Powerformer: A Section-adaptive Transformer for Power Flow Adjustment'. Full data and code for reproducing our work will be uploaded within a week.

Official codebase for paper [Factorizable State Attribution for Adjusting Power Flow at Transmission Interface]. This codebase is based on the open-source [Tianshou](https://github.com/thu-ml/tianshou) and [PandaPower](https://github.com/e2nIEE/pandapower) framework and please refer to those repo for more documentation. Baseline methods include [Soft-Module](https://github.com/RchalYang/Soft-Module) and a traditional full-connected neural network.

## Overview

**TLDR:**
We present a novel transformer architecture tailored for learning robust power system state representations, which strives to optimize power dispatch for the power flow adjustment across different transmission sections. Specifically, our proposed approach, named Powerformer, develops a dedicated section-adaptive attention mechanism, separating itself from the self-attention employed in conventional transformers. This mechanism effectively integrates power system states with transmission section information, which facilitates the development of robust state representations. Furthermore, by considering the graph topology of power system and the electrical attributes of bus nodes, we introduce two customized strategies to further enhance the expressiveness: graph neural network propagation and multi-factor attention mechanism.

![image](https://github.com/Cra2yDavid/Powerformer/blob/main/method.png)

## Prerequisites

### Install dependencies
* Python 3.8.13 or higher
* dgl 1.1 or higher
* Pytorch 1.13
* Pandapower 2.11
* gym 0.23
* tianshou 0.4.11
* numpy 1.22.4
* numba 0.55.2
* pandas 1.4.2

## Usage

Please follow the instructions below to replicate the results in the paper. Note that the model of China realistic 300-bus system is not available due to confidentiality policies of SGCC.

```bash
# IEEE 118-bus System under S10 (10-section) task
python train.py --case='case118' --task='S10' --method='Powerformer'
```

```bash
# IEEE 9241-bus System under S4 (4-section) task
python train.py --case='case9241' --task='S4' --method='Powerformer' 
```

## Contact

Please feel free to contact me via email (<chenkx@zju.edu.cn>, <davidluo@zju.edu.cn>, <liushunyu@zju.edu.cn>) if you are interested in my research :)
