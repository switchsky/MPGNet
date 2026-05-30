# Exploring Bus Stop Mobility Pattern with Temporal Variation: A Multi-Period Prediction Framework

[![Status](https://img.shields.io/badge/Status-Under_Review-blue.svg)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> **📣 News:** > - **[2026-05]** The paper has been submitted to *IEEE Internet of Things Journal*. 
> - **Code Availability:** To comply with the double-blind review process and pending publication, the source code is temporarily withheld. **We strictly commit to open-sourcing the complete training code, evaluation scripts, and pre-trained models immediately upon the paper's acceptance.** Please star ⭐ this repository to stay updated!

## 📖 Abstract

Traffic flow prediction is essential for intelligent transportation systems and the Internet of Vehicles (IoV). While this data-rich environment provides unprecedented opportunities, predicting bus-related traffic poses unique challenges: passenger flows exhibit both macroscopic spatial clustering across stops and microscopic temporal periodicity. 

To address this gap, we proposed **MPGNet**, a multi-pattern and multi-period traffic prediction framework. MPGNet leverages deep clustering on stop distance networks to extract IoV-relevant mobility patterns. It then applies temporal variation modeling to project 1D flow sequences into a 2D structural space and integrates a spatiotemporal module (STBlock) to learn coupled periodic dependencies across stops.

## 🚀 Key Contributions

1. **Multi-Pattern and Multi-Period Framework:** We propose MPGNet for sensor-equipped urban public transportation, effectively addressing both short-term and long-term prediction tasks.
2. **Spatial Dependency Extraction:** A deep clustering module based on graph neural networks (GCN) is employed to extract mobility patterns from bus stop data.
3. **Temporal Variation Modeling (STBlock):** We transform one-dimensional traffic flow data into two-dimensional space to explore the periodicity patterns of human mobility, capturing both intra-period and inter-period variations via multi-scale visual networks.

## 📊 Main Results (Preview)

Our model has been extensively evaluated on a real-world bus dataset from Jiangsu Panda Bus Company, demonstrating state-of-the-art performance against recent baselines.

* **Short-Term Prediction:** Outperforms baseline GNN-based models including STGCN, ASTGCN, Graph WaveNet, AGCRN, and HimNet in MSE, RMSE, and MAPE.
* **Long-Term Prediction:** Achieves superior performance compared to SOTA Transformer-based models such as Autoformer, iTransformer, PatchTST, STDN, and PDFormer across various prediction horizons (up to 13 hours).

*(Detailed performance tables and PCA clustering visualizations will be available upon code release.)*

## ⚙️ Environment & Setup

The upcoming code release is developed using Python and PyTorch, and has been fully tested in the following environment:
* Hardware: NVIDIA GeForce RTX 3090 (24GB VRAM)
* Key dependencies include spatial graph convolutions (GCN) and visual backbone networks (SqueezeNet).

## 📅 TODO List

We are actively preparing the repository for the final release:

- [x] Submit manuscript to IEEE IoT-J.
- [ ] Clean up data preprocessing scripts for the real-world bus dataset (passenger swipe records & bus entry/exit data).
- [ ] Refactor PyTorch training loops for MPGNet.
- [ ] Release the core deep clustering and STBlock modules.
- [ ] Publish instructions for reproducibility.

## ✉️ Contact

If you have any questions about the methodology or wish to discuss related research, please feel free to reach out:

- **Haofei Tan** - haofei_tan@outlook.com
- **Corresponding Author: Prof. Guojiang Shen** - gjshen1975@zjut.edu.cn
- **Institution:** College of Computer Science and Technology, Zhejiang University of Technology, Hangzhou, China

## 📝 Citation

If you find our ideas or framework helpful for your research, please consider citing our work:

```bibtex
@article{tan2026exploring,
  title={Exploring Bus Stop Mobility Pattern with Temporal Variation: A Multi-Period Prediction Framework},
  author={Kong, Xiangjie and Tan, Haofei and Shen, Zhehui and Shen, Guojiang and Zhao, Xiangyu},
  journal={Under Review (IEEE Internet of Things Journal)},
  year={2026}
}
