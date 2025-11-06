# FinCoT
 FinCoT: The Federated Financial Reasoning Distillation Dataset

## Overview
This work, "Federated Financial Reasoning Distillation: Training A Small Financial Expert by Learning From Multiple Teachers", has been accepted by the 6th ACM International Conference on AI in Finance (ICAIF 2025) ([https://icaif25.org/](https://icaif25.org/)).

Recent advancements in Large Language Models (LLMs) have significantly enhanced reasoning capabilities for complex tasks. However, the substantial computational demands and high deployment costs of these LLMs remain significant barriers to their widespread adoption. Although progress has been made in applying knowledge distillation to improve the performance of resource-friendly small LMs on general tasks, developing compact yet powerful financial reasoning expert LMs remains underexplored.

This repository provides the refined financial Chain-of-Thought (CoT) dataset introduced in the paper. The dataset includes two files corresponding to two public finance question-answer datasets:
- `mtms_dev_financeiq.json`: CoTs sampled from the FinanceIQ dataset
- `mtms_dev_fineval.json`: CoTs sampled from the FinEval dataset

These files serve as key resources for training compact financial expert models.

## Disclaimer
This dataset is provided solely for research purposes in the field of financial reasoning model distillation and is not intended for any commercial use.


## Dataset Details
The dataset contains high-quality financial reasoning CoTs, which are:
- Derived from responses of 5 leading reasoning and non-reasoning LLMs (teacher models) to financial problems
- Selected as optimal outputs through an "LLM-as-a-Judge" framework, ensuring high quality and relevance for financial reasoning tasks
- Suitable for training small financial expert models through data-based knowledge distillation

## Framework Context
The dataset supports the federated reasoning distillation framework, where refined CoTs from multiple teacher LLMs supervise the training of student financial experts. Our experiments show that a 7B distilled LM trained with this dataset can achieve competitive performance on financial reasoning tasks, see more details in our paper.

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