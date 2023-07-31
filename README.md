# [ICDE 2024] Factorizable State Attribution for Adjusting Power Flow at Transmission Interface

[![License: Apache](https://img.shields.io/badge/License-Apache-blue.svg)](LICENSE)

This repo is building for the source code and corresponding data of paper 'Factorizable State Attribution for Adjusting Power Flow at Transmission Interface'.
Full data and code for reproducing our work will be uploaded within a week.

Official codebase for paper [Factorizable State Attribution for Adjusting Power Flow at Transmission Interface]. This codebase is based on the open-source [Tianshou](https://github.com/thu-ml/tianshou) and [PandaPower](https://github.com/e2nIEE/pandapower) framework and please refer to those repo for more documentation. Baseline methods include [Soft-Module](https://github.com/RchalYang/Soft-Module) and a traditional full-connected neural network.

We introduce a factorizable state representation learning (FSRL) scheme that disentangles the node state features into four essential electrical factors and employs a state-of-theart GNN to obtain efficient representations of each distinct state factor, effectively alleviating and mitigating the high coupling issue among features. We develop a State Factor Attribution (FSA) map that generates task-adaptive attention weights for distinct state factors. This enables the acquisition of an expressive power system state representation and enhances the interpretability of efficient strategies to address the problem of transmission interface power flow adjustment.

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
