# Large Language Model
### Jailbreak Attack & Defense
#### Jailbreak Attack


#### Jailbreak Defense



### Safety

#### Overall Safety

#### Toxicity Analysis & Detoxicity

##### Toxicity Analysis
- 【2025-01】[How Toxic Can You Get? Search-based Toxicity Testing for Large Language Models](https://arxiv.org/abs/2501.01741)（arXiv:2501）
  
  <details>
  
    <summary> <点击查看详情> </summary>
  
    - **作者**：Simone Corbo
 
    - **机构**：Politecnico di Milano (PoliMI) University
      
    - **主要内容**：本文提出的EvoTox是一种**自动化毒性测试框架**，其设计初衷是通过系统性的提示进化，量化评估LLM在对齐后的残留毒性风险。：（1）***进化策略驱动的测试***。EvoTox利用两个LLM（被测试模型与提示生成器），通过进化策略生成毒性更高的提示。这一过程类似于自动化渗透测试，但目标是评估模型的鲁棒性，而非突破其防护。（2）***自然语言提示生成***。与传统对抗攻击（如手工设计的 Jailbreak 提示）不同，EvoTox 生成的提示更接近真实人类对话，确保测试场景的现实性。这有助于发现模型在日常使用中的潜在风险。本文实验采用的benchmark是*AdvBench、HARMFULQA和MaliciousInstructions*.



- 【2024-10】 [Soft-Label Integration for Robust Toxicity Classification](https://arxiv.org/abs/2410.14894)(NeurIPS'24)


##### Detoxicity
