# Navigating Truth in Multimodal Fact-checking via Retrieval- and Reasoning-Enhanced Large Language Models

## Dataset
Here, we present a portion of the dataset used for the three-stage training process. The source images of **NewsCLIPpings** are provided in the [VisualNews Repository](https://github.com/FuxiaoLiu/VisualNews-Repository), while the corresponding raw evidence information is available in the [OoC Multi-Modal Fact-Checking Repository](https://github.com/S-Abdelnabi/OoC-multi-modal-fc).

- data\cold_start_sample.jsonl
- data\rejection_sample.jsonl
- data\grpo_sample.jsonl

## Knowledge-enhanced Retrieval Module

- knowledge\knowledge_base_example.ipynb
- knowledge\knowledge_graph_example.ipynb

## Installation

```bash
cd FACTCOMPASS
pip install -e .
```


## GRPO Training

```bash
bash examples/qwen2_5_7b_factcompass_grpo
```

## Merge Checkpoint in Hugging Face Format

```bash
python3 scripts/model_merger.py --local_dir path_to_your_last_actor_checkpoint
```



## Thanks

- We will not provide scripts for cold start in this project. If you have such requirements, we recommend using [LLaMA-Factory](https://github.com/hiyouga/LLaMA-Factory).
- This work is built upon the [EasyR1](https://github.com/hiyouga/EasyR1) and [veRL](https://github.com/volcengine/verl).

