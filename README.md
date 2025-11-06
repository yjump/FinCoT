# FinCoT
 Federated Financial Reasoning Distillation

## Overview
This work, "Federated Financial Reasoning Distillation: Training A Small Financial Expert by Learning From Multiple Teachers", has been accepted by the 6th ACM International Conference on AI in Finance (ICAIF), Singapore, 2025 ([https://icaif25.org/](https://icaif25.org/)).

Recent advancements in Large Language Models (LLMs) have significantly enhanced reasoning capabilities for complex tasks. However, the substantial computational demands and high deployment costs of these LLMs remain significant barriers to their widespread adoption. Although progress has been made in applying knowledge distillation to improve the performance of resource-friendly small LMs on general tasks, developing compact yet powerful financial reasoning expert LMs remains underexplored.

This repository provides the refined financial Chain-of-Thought (CoT) dataset introduced in the paper. The dataset is selected from public finance question-answer datasets (FinEval and FinanceIQ) and serves as a key resource for training compact financial expert models.

## Dataset Details
The dataset contains high-quality financial reasoning CoTs, which are:
- Derived from leading reasoning and non-reasoning LLMs' responses to financial problems
- Refined using an "LLM-as-a-Judge" mechanism to ensure quality and relevance
- Suitable for training small financial expert models through SFT-based knowledge distillation

## Framework Context
The dataset supports the federated reasoning distillation framework, where refined CoTs from multiple teacher LLMs supervise the training of student financial experts. Our experiments show that a 7B distilled LM trained with this dataset can achieve competitive performance on financial reasoning tasks.

![FinCoT Framework Pipeline](pipeline.jpg)


## Citation
If you use this dataset or find our work helpful, please cite our paper:
```bibtex
@inproceedings{liu2025federated,
    title={Federated Financial Reasoning Distillation: Training A Small Financial Expert by Learning From Multiple Teachers},
    author={Liu, Shuoling and Yan, Jiangpeng and Wang, Xiaoyu and Jiang, Yuhang and others},
    booktitle={Proceedings of the 6th ACM International Conference on AI in Finance},
    year={2025},
    publisher={ACM}
}