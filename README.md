# 关于大模型处理ERC任务

## Introduction
学习了相关对于大模型ERC任务的处理方法，尝试将 ERC 任务从判别框架重新表述为基于大型语言模型（LLM）的生成框架，并将大语言模型的微调技术应用于对话中的情感识别中。使用的主要技术如下：为帮助模型显式集成多粒度对话监督信息，将ERC 任务重新表述为统一的 Seq2Seq 范式，并提出了一个可以适应不同对话场景的有效指令模板，使用检索模板连接具有高度语义相似性的历史对话内容、标签语句和情感领域演示。针对情感对齐任务，建模对话中的对话角色关系和未来的情感倾向，将其划分为说话者识别和情感预测任务两个子任务。

文件框架如下
```plain
.
├── checkpoint
├── code
│   ├── data_process_mixed.py
│   ├── data_process_plain.py
│   ├── data_process.py
│   ├── data_utils
│   ├── main_new.py
│   ├── train_and_inference_Mixed.sh
│   ├── train_and_inference_Plain.sh
│   └── train_and_inference_Uni.sh
├── data
│   └──iemocap
├── envs
│   └── requirements.txt
├── experiments
├── file_structure.txt
├── LLM_bases
│   └──LLaMA
├── original_data
│   └──iemocap
└── README.md
```

### LLMs download
在huggingface下载
