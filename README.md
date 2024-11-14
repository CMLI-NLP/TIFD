# TIFD: 面向大语言模型监督微调的藏语指令数据集

## 项目简介

TIFD (Tibetan Instruction-Following Dataset) 是一个专门用于大语言模型监督微调的藏语指令数据集。该数据集包含11,535条数据，每条数据包含四个属性：唯一标识符、指令、输入和输出。

## 数据集特点

- **规模**: 11,535条高质量藏语指令数据
- **格式**: JSON格式，包含id、instruction、input、output四个字段
- **来源**: 基于GPT-4生成并经专业藏语人员校对修正
- **用途**: 适用于大语言模型的监督微调任务

## 数据处理流程

1. **初始数据生成**: 使用GPT-4基于175个种子指令生成数据
2. **数据选择**: 使用LaBSE模型进行向量化，通过K-Center-Greedy算法选择具代表性的指令
3. **人工审校**: 多位藏语专家进行校对，确保数据质量

## 数据集下载

完整数据集可在以下位置获取：
- [TIFD数据集]([/data/tifd.json](https://huggingface.co/datasets/CMLI-NLP/TIFD/tree/main))

## 应用示例

已成功应用于藏语大语言模型TiLamb（基于LLaMA2-7B）的监督微调，显著提升了模型的藏语指令理解和对话能力。

## 免责申明

本数据集/模型仅供学术研究使用。禁止用于任何商业或不道德的目的。

## Citation

如果您发现该项目对您的研究有用，请考虑引用：

```bibtex
@article{Zhuang2024TIFD,
  title={TIFD: Tibetan Instruction-Following Dataset for Large Language Models Supervised Fine-Tuning},
  author={Wenhao Zhuang and Dawa Cairen and Yuan Sun},
  journal={Data Intelligence},
  year={2024},
  url={}
}
```
