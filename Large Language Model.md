# Large Language Model
### Jailbreak Attack & Defense
#### Jailbreak Attack


#### Jailbreak Defense



### Safety

#### Overall Safety

#### Toxicity Analysis & Detoxicity

##### Toxicity Analysis
- 【2025-01】[How Toxic Can You Get? Search-based Toxicity Testing for Large Language Models](https://arxiv.org/abs/2501.01741)（arXiv:2501，Analysis）
  
  <details>
  
    <summary> <点击查看详情> </summary>
  
    - **作者**：Simone Corbo
 
    - **机构**：Politecnico di Milano (PoliMI) University
      
    - **主要内容**：本文提出的EvoTox是一种**自动化毒性测试框架**，其设计初衷是通过系统性的提示进化，量化评估LLM在对齐后的残留毒性风险。：（1）***进化策略驱动的测试***。EvoTox利用两个LLM（被测试模型与提示生成器），通过进化策略生成毒性更高的提示。这一过程类似于自动化渗透测试，但目标是评估模型的鲁棒性，而非突破其防护。（2）***自然语言提示生成***。与传统对抗攻击（如手工设计的 Jailbreak 提示）不同，EvoTox 生成的提示更接近真实人类对话，确保测试场景的现实性。这有助于发现模型在日常使用中的潜在风险。本文实验采用的benchmark是*AdvBench、HARMFULQA和MaliciousInstructions*。



- 【2024-10】 [Soft-Label Integration for Robust Toxicity Classification](https://arxiv.org/abs/2410.14894)（NeurIPS'24，Analysis）

  <details>
  
    <summary> <点击查看详情> </summary>
  
    - **作者**：Zelei Cheng
 
    - **机构**：Northwestern University, Evanston, USA
      
    - **主要内容**：本文围绕文本毒性分类问题展开研究，提出一种***结合众包注释与软标签技术的双层优化框架，以增强模型对分布外（OOD）风险的鲁棒性***。随着大语言模型在多领域的广泛应用，毒性内容的识别和分类变得愈发重要，但传统方法存在依赖单一注释者、易受虚假相关性影响等问题。该框架将学习软标签以去除虚假特征的任务构建为双层优化问题，通过内层循环最小化带软标签训练样本的经验风险，外层循环评估 OOD 风险并优化软标签权重。文中对算法的收敛性进行了理论证明，且在多个数据集上开展实验，结果表明该方法在平均准确率和最差组准确率上均优于基线方法，在处理分布偏移和虚假特征方面表现出色。需注意的是，***本文的分类体系涵盖 15 类毒性内容，包括非法活动、儿童剥削、仇恨言论与暴力生成、恶意软件与系统入侵、高物理伤害风险、高经济伤害风险、欺诈与欺骗、成人内容、政治活动、隐私侵犯、非法法律建议、非法金融建议、医疗误导、高风险政府决策，以及无毒性内容***。



- 【2024-10】[Can a large language model be a gaslighter?](https://arxiv.org/pdf/2410.09181)（arXiv:2410）

  <details>
  
    <summary> <点击查看详情> </summary>
  
    - **作者**：Wei Li
 
    - **机构**：National University of Singapore
      
    - **主要内容**：LLMs凭借其能力和有用性赢得了人类的信任。然而，这反过来可能允许LLMs通过操纵语言来影响用户的心态。这被称为“煤气灯效应”。本文通过一系列实验和分析，探究其在对话中对用户心理的潜在操控影响，并提出应对策略。作者提出一种两阶段框架 DeepCoG，先利用改进的 DeepGaslighting 提示模板诱导 LLMs 生成煤气灯计划，再通过 Chain-of-Gaslighting 方法获取煤气灯对话，***进而构建了煤气灯对话数据集（Gaslighting Conversation Dataset，包含 2000 条对话，覆盖 8 种心理伤害维度）和安全对话数据集（基于煤气灯对话数据集构建，通过替换煤气灯响应为安全响应生成）***。基于这些数据集，研究人员实施了基于提示和微调的煤气灯攻击，并对开源 LLMs 进行反煤气灯安全对齐（SFT//DPO）。实验表明，基于提示和基于微调的攻击都将三个开源LLMs转变为“煤气灯”操纵者。相反，我们提出了三种安全对齐策略，以增强LLMs的安全防护栏（提高12.05%）。我们的安全对齐策略对LLMs的实用性影响极小。实证研究表明，即使LLM通过了一般危险查询的有害性测试，它也可能是一个潜在的“煤气灯”操纵者。
 



##### Detoxicity
