# [ICDE 2024] Factorizable State Attribution for Adjusting Power Flow at Transmission Interface

[![License: Apache](https://img.shields.io/badge/License-Apache-blue.svg)](LICENSE)

This repo is building for the source code and corresponding data of paper 'Factorizable State Attribution for Adjusting Power Flow at Transmission Interface'.
Full data and code for reproducing our work will be uploaded within a week.

Official codebase for paper [Factorizable State Attribution for Adjusting Power Flow at Transmission Interface]. This codebase is based on the open-source [Tianshou](https://github.com/thu-ml/tianshou) and [PandaPower](https://github.com/e2nIEE/pandapower) framework and please refer to those repo for more documentation. Baseline methods include [Soft-Module](https://github.com/RchalYang/Soft-Module) and a traditional full-connected neural network.

## Overview

**TLDR:**
We introduce a factorizable state representation learning (FSRL) scheme that disentangles the node state features into four essential electrical factors and employs a state-of-theart GNN to obtain efficient representations of each distinct state factor, effectively alleviating and mitigating the high coupling issue among features. We develop a State Factor Attribution (FSA) map that generates task-adaptive attention weights for distinct state factors. This enables the acquisition of an expressive power system state representation and enhances the interpretability of efficient strategies to address the problem of transmission interface power flow adjustment.

![image](https://github.com/Cra2yDavid/FSA/blob/main/method.png)

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
# IEEE 9241-bus System under S4 (Single 4-Interface) task
python train.py --case='case9241' --task='S4' --method='MAM' --model='Attention'
# IEEE 118-bus System under S10 (Single 10-Interface) task
python train.py --case='case118' --task='S10' --method='MAM' --model='Attention'
```

## Contact

Please feel free to contact me via email (<chenkx@zju.edu.cn>, <davidluo@zju.edu.cn>, <liushunyu@zju.edu.cn>) if you are interested in my research :)
