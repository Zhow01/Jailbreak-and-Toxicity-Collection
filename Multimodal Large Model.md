# Multimodal Large Model
### Jailbreak Attack & Defense
#### Jailbreak Attack

- 【2025-03】[Metaphor-based Jailbreaking Attacks on Text-to-Image Models](https://arxiv.org/abs/2503.18681)（arXiv:2503）

  <details>
  
    <summary> <点击查看详情> </summary>
  
    - **作者**：Chenyu Zhang
 
    - **机构**：Tianjin University
      
    - **主要内容**：本文提出了MJA（Metaphor-based Jailbreaking Attack）的越狱攻击方法，旨在绕过文本生成图像（T2I）模型的安全过滤器，以生成敏感图像。​与现有方法相比，MJA在提高攻击效果的同时，显著减少了所需查询次数。MJA方法包括两个主要模块：（1）***基于LLM的多代理生成模块（MLAG）***：​将生成隐喻式对抗提示的过程分解为三个子任务：隐喻检索、上下文匹配和对抗提示生成。MLAG协调三个LLM代理，探索多种隐喻和上下文组合，生成多样化的对抗提示。（2）***对抗提示优化模块（APO）***：​首先训练一个代理模型，预测对抗提示的攻击效果，然后设计获取策略，适应性地识别最优对抗提示，以提高攻击效率。


#### Jailbreak Defense



### Safety

#### Overall Safety



#### Toxicity





 #### Others

- 【2025-03】[Commander-GPT: Fully Unleashing the Sarcasm Detection Capability of Multi-Modal Large Language Models](https://arxiv.org/abs/2503.18681)（arXiv:2503，Sarcasm）

  <details>
  
    <summary> <点击查看详情> </summary>
  
    - **作者**：Yazhou Zhang
 
    - **机构**：None
      
    - **主要内容**：本文提出了一种名为Commander-GPT的多模态大模型（MLLM）框架，旨在充分发挥***多模态信息在讽刺检测中的作用***。​受军事战略启发，作者将讽刺检测任务划分为六个子任务（文本情感分析、图像内容识别、文本与图像一致性检查、上下文关系分析、文化和背景知识应用、讽刺判断），由中央指挥官（决策者）***将最适合的大型语言模型分配给每个子任务***，最终将各模型的检测结果汇总以识别讽刺内容。在模型架构方面，Commander-GPT采用了军事战略中的指挥官-部队结构，将每个子任务视为一个独立的“部队”，由中央“指挥官”负责调度。​具体而言，指挥官根据任务需求，将最适合的大型语言模型（如GPT-4o mini、O3 mini等）分配给各个子任务。​每个模型独立处理分配给它的子任务，最终将各自的输出结果汇总，以识别讽刺内容。​





