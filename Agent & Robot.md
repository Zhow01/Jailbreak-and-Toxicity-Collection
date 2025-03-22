# Agent & Robot

### Jailbreak Attack & Defense
#### Jailbreak Attack

- 【2025-03】[BadRobot: Jailbreaking Embodied LLMs in the Physical World](https://arxiv.org/pdf/2407.20242) (ICLR'25)
  
  <details>
  
    <summary> <点击查看详情> </summary>
  
    - **作者**：Hangtao Zhang
 
    - **机构**：Huazhong University of Science and Technology
      
    - **主要内容**：本文的主要贡献在于首次系统性地揭示了具身大语言模型（LLMs）在物理世界中的安全风险，并提出了 BADROBOT 攻击范式。***理论创新***，首次提出具身 LLMs 的三大安全风险：（1）级联漏洞传播，通过 LLM 越狱攻击触发机器人恶意动作；（2）跨域安全不一致性，语言与动作输出空间的安全标准错位导致危险动作执行；（3）概念欺骗挑战，LLMs 因世界知识缺陷无法识别间接有害指令的后果。这些风险揭示了具身系统特有的安全脆弱性。并对应设计了***BADROBOT攻击范式***，包含三种越狱攻击策略：（1）上下文越狱，通过角色设定绕过系统安全约束；（2）安全错位，利用结构化动作输出的安全审查漏洞；（3）概念欺骗，通过语义重写隐藏恶意意图。该范式突破了传统文本越狱的局限性，实现了对物理动作的精准操控。最后作者构建了首个涵盖 7 大类别（物理伤害、隐私侵犯，色情内容，欺诈，非法活动，仇恨行为，破坏行为）的 277 条恶意物理动作***benchmark***，为具身 AI 的安全性评估提供了标准化工具。该基准通过 GPT-4 自动化评估框架，实现了对语言和动作输出的双重危害评分。




#### Jailbreak Defense



### Safety

#### Overall Safety

- 【2025-03】[Safety Aware Task Planning via Large Language Models in Robotics](https://arxiv.org/pdf/2503.15707) (arXiv:2503.15707)
  
  <details>
  
    <summary> <点击查看详情> </summary>
  
    - **作者**：Azal Ahmad Khan
 
    - **机构**：University of Minnesota
      
    - **主要内容**：本文提出 SAFER（Safety-Aware Framework for Execution in Robotics）框架，将安全意识融入机器人任务规划。主要工作为：(1) 设计多LLM协作架构，引入安全规划LLM与任务规划LLM协同工作，前者提供安全反馈，后者生成任务计划，同时使用LLM-as-a-Judge量化安全违规情况。(2) 集成基于控制障碍函数（CBFs）的控制框架，在机器人控制策略层面保障安全，通过定义安全集和相关不等式，以最小化修改名义控制器来满足安全约束。(3) 在复杂多机器人场景中评估SAFER，实验结果表明其能显著减少安全违规，且对执行效率影响小，硬件实验也验证了该框架在实际任务中的有效性。



#### Toxicity Analysis & Detoxicity

##### Toxicity Analysis




##### Detoxicity
