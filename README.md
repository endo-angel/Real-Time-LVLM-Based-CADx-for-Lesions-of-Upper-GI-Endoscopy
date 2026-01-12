# Real-Time-LVLM-Based-CADx-for-Lesions-of-Upper-GI-Endoscopy

Real Time LVLM Based CADx for Lesions of Upper GI Endoscopy

## Main dependent tools

* python: 3.10+
* transformers: 4.41.2+
  
## Getting Started

### Data Preparation

Please refer to [data/README.md](https://github.com/hiyouga/LLaMA-Factory/blob/main/data/README.md) for checking the details about the format of dataset files. You can either use datasets on HuggingFace / ModelScope / Modelers hub or load the dataset in local disk.
> [!NOTE]
> update `LLaMA-Factory/data/dataset_info.json` to use  custom dataset.

### Install

Clone the repository and then install relevant dependencies based on [LLaMA-Factory-getting-started](https://github.com/hiyouga/LLaMA-Factory/blob/main/README.md#getting-started)

```bash
git clone --depth 1 https://github.com/hiyouga/LLaMA-Factory.git
```

### Train

We use 4 * NVIDIA A100 GPUs (40GB) for training and can update parameters such as batch_size according to our hardware conditions.

```bash
FORCE_TORCHRUN=1 llamafactory-cli train qwen2vl_lora_sft.yaml
```

### Predict

Using webui for prediction

```bash
llamafactory-cli webui 
```

### Evaluate

See evaluate.ipynb

## Pretrained model

🤗[Qwen2-VL-7B-Instruct](https://huggingface.co/Qwen/Qwen2-VL-7B-Instruct)
[EndoCADx](DOI: https://doi.org/10.5061/dryad.tqjq2bwct)

## Acknowledgement

This repo benefits from [Qwen2-VL](https://github.com/QwenLM/Qwen2-VL) and [LLaMA-Factory](https://github.com/hiyouga/LLaMA-Factory). Thanks for their wonderful works.

## About the author

* Author
  *  Wuhan University & Renmin Hospital of Wuhan University & Wuhan EndoAngel Medical Technology Co., Ltd.
* E-mail
  * <shan.hu@ai-endoangel.com>
  * <jiangyuhan@whu.edu.cn>
  * <tinshun.xiong@ai-endoangel.com>
  * <wu_leanne@whu.edu.cn>
