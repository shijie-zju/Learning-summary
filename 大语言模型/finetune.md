# FineTune

## 吴恩达课程

### 优势：behavior change & gain knowledge

微调能够为LLM提供比prompt多得多的数据，如gpt3指令微调为chatgpt

微调能让模型回答出更一致的输出或行为，且能帮模型减少幻觉，能让你将模型用到特定的场景

对话时的性能提升；本地或VPC(私有云)部署保护了隐私；降低成本；减少部分程序的延迟

### 使用示例

Pytorch(底层接口) - Huggingface（数据集和模型） - Llama library（第三方库，更简易接口）

### 操作
**Pre-training**

参数完全随机，自监督学习-预测下一个token词，数据集海量

**Base Model**
基础模型，只能向后补充词汇，不具备聊天性能

**Finetuning**
改变训练数据，使其以一种更结构化的方式呈现，然后对原模型进行训练

1. 选取一个大LLM
2. 了解所选取的LLM适合做的任务方向
3. 确定特定的某个任务
4. 为任务收集一些文本输入和输出(常为json格式，起始数据量1000。)

格式1：问答对形式紧密连接起来。

格式2-指令微调格式：让模型知道接下来干什么 

prompt_template_qa = """### Qusetion:{question} ### Answer:{answer}"""

5. 预训练小LLM在这组数据上

**Finetuned Model**
性能更好的模型，如Alpacav

### 指令微调详解
LMS指示模型遵循指令并表现的更像一个聊天机器人

**数据**
使用现有的易得数据，如客户问答记录

数据准备 -> 训练 -> 评估 -> 数据...

#### Data Preparation 
1. 收集指令问答对
2. 配对连接数据对（增加提示模板）
3. tokenize向量化:pad添加填充、truncate截断数据，使其大小适合模型输入

将文本转换为数字向量，分词--encoding-->向量--decoding-->分词

4. 切分成train/test

#### Train Process

加载数据:huggingface上或本地加载

指定模型：huggingface上的模型

分词器：切分数据 -> pad -> 划分训练和验证集

指定模型训练方式（CPU,GPU）

训练：

推理inference: encode -> generate -> decode -> 剔除prompt -> 计算loss













