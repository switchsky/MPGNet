# [cite_start]Exploring Bus Stop Mobility Pattern with Temporal Variation: A Multi-Period Prediction Framework [cite: 2]

[![Status](https://img.shields.io/badge/Status-Under_Review-blue.svg)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> [cite_start]**📣 News:** > - **[2026-05]** The paper has been submitted to *IEEE Internet of Things Journal*[cite: 1]. 
> - **Code Availability:** To comply with the double-blind review process and pending publication, the source code is temporarily withheld. **We strictly commit to open-sourcing the complete training code, evaluation scripts, and pre-trained models immediately upon the paper's acceptance.** Please star ⭐ this repository to stay updated!

## 📖 Abstract

[cite_start]Traffic flow prediction is essential for intelligent transportation systems and the Internet of Vehicles (IoV)[cite: 5]. [cite_start]While this data-rich environment provides unprecedented opportunities, predicting bus-related traffic poses unique challenges: passenger flows exhibit both macroscopic spatial clustering across stops and microscopic temporal periodicity[cite: 7, 27]. 

[cite_start]To address this gap, we proposed **MPGNet**, a multi-pattern and multi-period traffic prediction framework[cite: 8]. [cite_start]MPGNet leverages deep clustering on stop distance networks to extract IoV-relevant mobility patterns[cite: 9]. [cite_start]It then applies temporal variation modeling to project 1D flow sequences into a 2D structural space and integrates a spatiotemporal module (STBlock) to learn coupled periodic dependencies across stops[cite: 10].

## 🚀 Key Contributions

1. [cite_start]**Multi-Pattern and Multi-Period Framework:** We propose MPGNet for sensor-equipped urban public transportation, effectively addressing both short-term and long-term prediction tasks[cite: 83, 84].
2. [cite_start]**Spatial Dependency Extraction:** A deep clustering module based on graph neural networks (GCN) is employed to extract mobility patterns from bus stop data[cite: 84, 199].
3. [cite_start]**Temporal Variation Modeling (STBlock):** We transform one-dimensional traffic flow data into two-dimensional space to explore the periodicity patterns of human mobility, capturing both intra-period and inter-period variations via multi-scale visual networks[cite: 87, 255].

## 🧠 Problem Definition

[cite_start]Given a bus stop transportation network $\mathcal{G}_{s}^{dist}=(\mathcal{V}_{s},\mathcal{E}_{s}^{dist},A_{s}^{dist})$ [cite: 167][cite_start], the historical spatiotemporal graph flow feature matrix over the past $T_{h}$ steps is defined as $\mathbf{X}_{t-T_{h}+1:t} \in \mathbf{R}^{T_{h} \times N \times C}$[cite: 174]. [cite_start]Our goal is to predict the future spatiotemporal graph flow feature matrix $\mathbf{X}_{t+1:t+T_{p}} \in \mathbf{R}^{T_{p} \times N \times C}$ for the next $T_{p}$ time steps[cite: 170, 174].

## 📊 Main Results (Preview)

[cite_start]Our model has been extensively evaluated on a real-world bus dataset from Jiangsu Panda Bus Company[cite: 348, 349], demonstrating state-of-the-art performance against recent baselines.

* [cite_start]**Short-Term Prediction:** Outperforms baseline GNN-based models including STGCN, ASTGCN, Graph WaveNet, AGCRN, and HimNet in MSE, RMSE, and MAPE[cite: 508, 511].
* [cite_start]**Long-Term Prediction:** Achieves superior performance compared to SOTA Transformer-based models such as Autoformer, iTransformer, PatchTST, STDN, and PDFormer across various prediction horizons (up to 13 hours)[cite: 513, 514, 516].

[cite_start]*(Detailed performance tables and PCA clustering visualizations will be available upon code release[cite: 440].)*

## ⚙️ Environment & Setup

The upcoming code release is developed using Python and PyTorch, and has been fully tested in the following environment:
* [cite_start]Hardware: NVIDIA GeForce RTX 3090 (24GB VRAM) [cite: 384]
* [cite_start]Key dependencies include spatial graph convolutions (GCN) and visual backbone networks (SqueezeNet)[cite: 199, 329].

## 📅 TODO List

We are actively preparing the repository for the final release:

- [x] Submit manuscript to IEEE IoT-J.
- [ ] [cite_start]Clean up data preprocessing scripts for the real-world bus dataset (passenger swipe records & bus entry/exit data)[cite: 348, 352].
- [ ] Refactor PyTorch training loops for MPGNet.
- [ ] [cite_start]Release the core deep clustering and STBlock modules[cite: 254].
- [ ] Publish instructions for reproducibility.

## ✉️ Contact

If you have any questions about the methodology or wish to discuss related research, please feel free to reach out:

- [cite_start]**Haofei Tan** - haofei_tan@outlook.com [cite: 19]
- [cite_start]**Corresponding Author: Prof. Guojiang Shen** - gjshen1975@zjut.edu.cn [cite: 17, 19]
- [cite_start]**Institution:** College of Computer Science and Technology, Zhejiang University of Technology, Hangzhou, China [cite: 18]

## 📝 Citation

If you find our ideas or framework helpful for your research, please consider citing our work:

```bibtex
@article{kong2026exploring,
  title={Exploring Bus Stop Mobility Pattern with Temporal Variation: A Multi-Period Prediction Framework},
  author={Kong, Xiangjie and Tan, Haofei and Shen, Zhehui and Shen, Guojiang and Zhao, Xiangyu},
  journal={Under Review (IEEE Internet of Things Journal)},
  year={2026}
}
