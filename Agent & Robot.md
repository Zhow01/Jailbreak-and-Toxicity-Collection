# Agent & Robot

### Jailbreak
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

- 【2025-03】[Rude Humans and Vengeful Robots: Examining Human Perceptions of Robot 
Retaliatory Intentions in Professional Settings]([https://arxiv.org/abs/2503.16932]) (arXiv:2503.16932)
  
  <details>
  
    <summary> <点击查看详情> </summary>
  
    - **作者**：Kate R. Letheren
 
    - **机构**：Australian Catholic University;Queensland University of Technology
      
    - **主要内容**：研究在人机协作的专业环境中，人类如何感知机器人违反社交期望的行为，特别是机器人是否会“报复”粗鲁的人类,并探讨机器人在面对人类粗鲁行为时，是选择顺从、保持中立，还是以“报复性”行为回应，哪种方式更容易被接受。主要工作为：(1) 将“期望违背理论（EVT）”拓展至人机交互，揭示人类对机器人行为存在冲突期望（如功能优先vs.社交规范），并验证任务完成是核心“卫生因素”。(2)通过第一人称视角视频模拟人机互动，收集参与者对机器人可靠性、信任度、互动评价、自我效能及意图感知的数据。(3)使用ANCOVA等统计方法验证假设，并分析性别、信任倾向等个体因素的影响。(4)建议机器人设计需平衡任务执行与社交响应，例如通过透明沟通管理期望、避免绝对服从以应对恶意指令，同时强化机器人“以德报怨”的能力以提升合作体验。

#### Toxicity Analysis & Detoxicity

##### Toxicity Analysis




##### Detoxicity
