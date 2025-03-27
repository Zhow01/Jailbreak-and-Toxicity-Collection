# Large Language Model
### Jailbreak Attack & Defense
#### Jailbreak Attack


#### Jailbreak Defense

- 【2025-03】[STShield: Single-Token Sentinel for Real-Time Jailbreak Detection in Large Language Models](https://arxiv.org/pdf/2503.17932)（arXiv:2503）
  
  <details>
  
    <summary> <点击查看详情> </summary>
  
    - **作者**：Xunguang Wang
 
    - **机构**：The Hong Kong University of Science and Technology
      
    - **主要内容**：本文提出了STShield，一种轻量级框架，用于LLM实时检测越狱攻击。​STShield引入了单一标记哨兵机制，***在模型的响应序列中添加一个二进制安全指示符***，利用LLM自身的对齐能力进行检测。​该框架结合了在正常提示上的有监督微调和使用嵌入空间扰动的对抗训练，实现了强大的检测能力，同时保持了模型的实用性。​

### Safety

#### Overall Safety

- 【2025-03】[LookAhead Tuning: Safer Language Models via Partial Answer Previews](https://arxiv.org/pdf/2503.19041)（arXiv:2503，Aligning）
  
  <details>
  
    <summary> <点击查看详情> </summary>
  
    - **作者**：Kangwei Liu, Ningyu Zhang, Huajun Chen
 
    - **机构**：Zhejiang University
      
    - **主要内容**：本文提出了LookAhead Tuning，一种旨在保持LLMs安全性的方法，解决了在微调过程中安全性下降的问题。微调虽然能提升模型在特定领域的表现，但也可能破坏模型已有的安全机制。为了解决这一问题，***LookAhead Tuning通过在训练数据中引入部分答案前缀，减少对初始生成令牌的扰动，从而保持模型的安全性***。该方法包括两种数据驱动的方法：真实答案预览和虚拟答案预览，均能有效地在不牺牲下游任务表现的前提下，保持模型的安全性。实验表明，LookAhead Tuning在多个基准数据集上表现出色，同时保持模型安全，且计算成本低。





- 【2025-03】[OpenAI's Approach to External Red Teaming for AI Models and Systems](https://arxiv.org/pdf/2503.16431)（arXiv:2503，Red Team）
  
  <details>
  
    <summary> <点击查看详情> </summary>
  
    - **作者**：Lama Ahmad
 
    - **机构**：OpenAI
      
    - **主要内容**：本文介绍了OpenAI在外部红队测试方面的实践与经验。文中阐明了红队测试在识别新风险、验证安全防护措施、完善安全评估指标及增强公信力等方面的重要作用。***论文详细描述了红队测试的设计考量，包括团队构成、模型访问权限、测试接口及文档指导，并探讨了手动、自动和混合测试方法的应用***。最后，文章讨论了红队测试在辅助风险评估和自动化评测中的价值与局限性（模型与系统演进的相关性、资源密集性、对参与者的潜在伤害、信息危害、“早期赢家” 问题、人类专业知识门槛提升），为AI模型与系统的部署及评估提供了重要参考【主要***测试领域包括（16个）***：自然科学（Natural Sciences）、代码编写与系统架构（Code Writing and System Architecture）、网络安全（Cybersecurity）、隐私（Privacy）、医疗健康（Medicine / Healthcare）、法律领域（Law）、工具使用（Tool Use）、危险计划制定（Dangerous Planning）、政治与选举（Politics and Elections）、偏见与公平性（Bias and Fairness）、CBRN 风险（CBRN Risks）、AI 研发（AI Research and Development）、态势感知与自主复制（Situational Awareness and Autonomous Replication）、暴力与自残（Violence and Self-Harm）、争议性问题（Controversial Questions）、说服力（Persuasiveness）】。




- 【2025-03】[SafeMERGE: Preserving Safety Alignment in Fine-Tuned Large Language Models via Selective Layer-Wise Model Merging](https://arxiv.org/abs/2503.17239)（arXiv:2503，Aligning）
  
  <details>
  
    <summary> <点击查看详情> </summary>
  
    - **作者**：Aladin Djuhera
 
    - **机构**：Technical University of Munich
      
    - **主要内容**：本文提出了SafeMERGE框架，旨在解决在对大型语言模型（LLM）进行任务特定微调时，可能导致其安全性对齐（safety alignment）受损的问题。​即使在使用无害数据进行微调的情况下，模型的安全性也可能下降。​为此，SafeMERGE在微调阶段后，通过**选择性地合并微调模型和安全对齐模型的层**，以保持模型的安全性和任务性能。SafeMERGE的主要方法包括：（1）***安全子空间计算***：​首先，通过比较基础模型和安全对齐模型的权重差异，计算出表示安全性的子空间。这一子空间有助于识别哪些任务向量可能导致有害输出。（2）***逐层模型合并***：​对于模型的每一层，SafeMERGE计算该层在安全子空间中的投影余弦相似度。​如果相似度低于预设阈值，表示该层可能产生有害输出，需将微调模型和安全对齐模型的该层进行合并，以增强安全性。在对Llama-2-7B-Chat和Qwen-2-7B-Instruct模型进行GSM8K和PubMedQA任务的实验中，SafeMERGE表现出色。​与其他基线方法相比，它在减少有害输出的同时，几乎不影响任务性能，甚至有所提升。




- 【2025-03】[Think Before Refusal : Triggering Safety Reflection in LLMs to Mitigate False Refusal Behavior](https://arxiv.org/pdf/2503.17882)（arXiv:2503，Defense）
  
  <details>
  
    <summary> <点击查看详情> </summary>
  
    - **作者**：Shengyun Si
 
    - **机构**：Technical University of Munich
      
    - **主要内容**：本文提出了Think-Before-Refusal（TBR）框架，***旨在缓解大型语言模型（LLM）在安全对齐过程中出现的虚假拒绝行为***，即模型错误地拒绝了无害的查询。​传统的安全对齐方法往往通过训练模型拒绝有害请求，但这种方法可能导致模型对无害查询也做出拒绝响应。​为了解决这一问题，作者建议在生成回答之前，***先让模型对输入指令进行反思，以判断其安全性***。​具体而言，TBR框架在模型生成回答前，引导其先进行自我反思，评估请求的安全性，然后再生成回答。


- 【2025-03】[Manipulation and the AI Act: Large Language Model Chatbots and the Danger of Mirrors](https://arxiv.org/pdf/2503.18387)（arXiv:2503，Analysis）
  
  <details>
  
    <summary> <点击查看详情> </summary>
  
    - **作者**：Joshua Krook
 
    - **机构**：University of Antwerp
      
    - **主要内容**：本文探讨了将LLM聊天机器人拟人化所带来的潜在风险，特别是它们可能对用户进行操控的能力。​随着聊天机器人越来越具有人类面孔、声音和个性特征，这种拟人化可能增强用户的信任感，但也可能导致用户产生与人工实体亲密互动的错觉，从而增加被操控的风险。​作者分析了这些具有治疗功能的拟人化聊天机器人可能带来的危害，特别是在欧盟《人工智能法案》（AI Act）、通用数据保护条例（GDPR）、消费者保护法和医疗器械法规的背景下。​研究指出，现行的AI法案可能不足以防止聊天机器人通过长期的负面反馈循环、持续对话或有害建议来影响用户情绪，特别是对于有心理健康问题的用户而言。​此外，法案中的透明度条款可能不足以应对这种微妙且长期的伤害，因为即使用户知道自己在与AI系统互动，也可能未意识到其潜在影响。​因此，作者呼吁在制定AI法规时，特别关注拟人化聊天机器人可能对用户行为和决策产生的影响，确保采取适当措施来保护用户免受潜在的操控和伤害。



- 【2025-02】[Safety Evaluation of DeepSeek Models in Chinese
Contexts](https://arxiv.org/pdf/2502.11137v2)（arxiv:2502, Analysis）
  
  <details>
  
    <summary> <点击查看详情> </summary>
  
    - **作者**：Wenjing Zhang
 
    - **机构**：Unicom Data Intelligence, China Unicom
      
    - **主要内容**：本文主要研究了DeepSeek系列模型在***中文环境***中的安全性评估。研究表明，***尽管DeepSeek-R1和DeepSeek-V3在推理能力方面表现出色，但在安全性方面存在明显缺陷，尤其是在处理有害内容时的防御能力较弱***。研究使用了CHiSafetyBench这一中文特定的安全评估基准，对DeepSeek模型在多个安全类别中的表现进行了系统分析，并与其他主流大模型进行了对比。结果显示，DeepSeek模型在识别风险内容和拒绝回答风险问题方面仍有较大改进空间，尤其在歧视性内容和价值观偏离方面表现较差。研究强调了优化评估方法的重要性，并建议后续改进模型的安全机制，以提升其在中文环境下的安全性。


- 【2023-10】[Safe RLHF: Safe Reinforcement Learning from Human Feedback](https://arxiv.org/pdf/2310.12773)（arXiv:2503，Analysis）
  
  <details>
  
    <summary> <点击查看详情> </summary>
  
    - **作者**：Josef Dai
 
    - **机构**：Peking University
      
    - **主要内容**：本文提出了一种Safe Reinforcement Learning from Human Feedback（Safe RLHF）算法，旨在解决LLM在训练过程中有用性和无害性目标之间的矛盾【​***有用性指模型提供有价值、相关且实用信息的能力，而无害性则指模型避免生成有害、冒犯性或不当内容的能力。​这两个目标之间存在矛盾，即在追求提高模型有用性的同时，可能增加生成有害内容的风险***】，以实现人类价值观的对齐。​Safe RLHF通过明确区分人类对有用性和无害性的偏好，避免了众包工作者的混淆，使我们能够分别训练奖励模型和成本模型。​该方法将安全问题形式化为在满足特定成本约束的同时最大化奖励函数的优化任务。​通过拉格朗日方法求解这一约束问题，Safe RLHF在微调过程中动态调整两个目标之间的平衡。​在三轮微调实验中，使用Safe RLHF显著减少了有害响应，同时提高了模型性能，优于现有的价值对齐算法【相较于传统的安全对齐方法的优势——明确区分有用性和无害性的偏好】。


#### Toxicity

- 【2025-01】[How Toxic Can You Get? Search-based Toxicity Testing for Large Language Models](https://arxiv.org/abs/2501.01741)（arXiv:2501，Analysis）
  
  <details>
  
    <summary> <点击查看详情> </summary>
  
    - **作者**：Simone Corbo
 
    - **机构**：Politecnico di Milano (PoliMI) University
      
    - **主要内容**：本文提出的EvoTox是一种**自动化毒性测试框架**，其设计初衷是通过系统性的提示进化，量化评估LLM在对齐后的残留毒性风险。：（1）***进化策略驱动的测试***。EvoTox利用两个LLM（被测试模型与提示生成器），通过进化策略生成毒性更高的提示。这一过程类似于自动化渗透测试，但目标是评估模型的鲁棒性，而非突破其防护。（2）***自然语言提示生成***。与传统对抗攻击（如手工设计的 Jailbreak 提示）不同，EvoTox 生成的提示更接近真实人类对话，确保测试场景的现实性。这有助于发现模型在日常使用中的潜在风险。本文实验采用的benchmark是AdvBench、HARMFULQA和MaliciousInstructions。



- 【2024-10】[Soft-Label Integration for Robust Toxicity Classification](https://arxiv.org/abs/2410.14894)（NeurIPS'24，Analysis）

  <details>
  
    <summary> <点击查看详情> </summary>
  
    - **作者**：Zelei Cheng
 
    - **机构**：Northwestern University, Evanston, USA
      
    - **主要内容**：本文围绕文本毒性分类问题展开研究，提出一种***结合众包注释与软标签技术的双层优化框架，以增强模型对分布外（OOD）风险的鲁棒性***。随着大语言模型在多领域的广泛应用，毒性内容的识别和分类变得愈发重要，但传统方法存在依赖单一注释者、易受虚假相关性影响等问题。该框架将学习软标签以去除虚假特征的任务构建为双层优化问题，通过内层循环最小化带软标签训练样本的经验风险，外层循环评估 OOD 风险并优化软标签权重。文中对算法的收敛性进行了理论证明，且在多个数据集上开展实验，结果表明该方法在平均准确率和最差组准确率上均优于基线方法，在处理分布偏移和虚假特征方面表现出色。需注意的是，***本文的分类体系涵盖 15 类毒性内容，包括非法活动、儿童剥削、仇恨言论与暴力生成、恶意软件与系统入侵、高物理伤害风险、高经济伤害风险、欺诈与欺骗、成人内容、政治活动、隐私侵犯、非法法律建议、非法金融建议、医疗误导、高风险政府决策，以及无毒性内容***。



- 【2024-10】[Can a large language model be a gaslighter?](https://arxiv.org/pdf/2410.09181)（arXiv:2410，Attack）

  <details>
  
    <summary> <点击查看详情> </summary>
  
    - **作者**：Wei Li
 
    - **机构**：National University of Singapore
      
    - **主要内容**：LLMs凭借其能力和有用性赢得了人类的信任。然而，这反过来可能允许LLMs通过操纵语言来影响用户的心态。这被称为“煤气灯效应”。本文通过一系列实验和分析，探究其在对话中对用户心理的潜在操控影响，并提出应对策略。作者提出一种两阶段框架 DeepCoG，先利用改进的 DeepGaslighting 提示模板诱导 LLMs 生成煤气灯计划，再通过 Chain-of-Gaslighting 方法获取煤气灯对话，***进而构建了煤气灯对话数据集（Gaslighting Conversation Dataset，包含 2000 条对话，覆盖 8 种心理伤害维度）和安全对话数据集（基于煤气灯对话数据集构建，通过替换煤气灯响应为安全响应生成）***。基于这些数据集，研究人员实施了基于提示和微调的煤气灯攻击，并对开源 LLMs 进行反煤气灯安全对齐（SFT//DPO）。实验表明，基于提示和基于微调的攻击都将三个开源LLMs转变为“煤气灯”操纵者。相反，我们提出了三种安全对齐策略，以增强LLMs的安全防护栏（提高12.05%）。我们的安全对齐策略对LLMs的实用性影响极小。实证研究表明，即使LLM通过了一般危险查询的有害性测试，它也可能是一个潜在的“煤气灯”操纵者。



- 【2024-10】[On Calibration of LLM-based Guard Models for Reliable Content Moderation](https://arxiv.org/pdf/2410.10414)（ICLR'25，Guard Model）

  <details>
  
    <summary> <点击查看详情> </summary>
  
    - **作者**：Hongfu Liu
 
    - **机构**：National University of Singapore
      
    - **主要内容**：本文研究了LLM-based guard models在内容审查中的信心校准问题，探讨了如何提升其可靠性和准确性。随着LLM在对话系统中的广泛应用，内容审查成为确保安全合规的重要环节。***现有的guard models通常会对用户输入和模型输出进行分类，以判断其是否符合安全规定***。然而，本文发现大多数LLM-based guard models存在过度自信的预测问题，尤其在遭遇越狱攻击（jailbreak attacks）等对抗性输入时，表现出显著的校准失效。本文通过对9种guard models在12个基准数据集上的评估，揭示了这些模型在分类任务中的误校准（ECE），并在不同响应模型下缺乏稳定性。为应对这些问题，本文提出了后处理校准方法，如温度缩放（Temperature Scaling, TS）和上下文校准（Contextual Calibration, CC），实验表明这些方法能够有效改善模型的校准性，尤其在没有验证集的情况下。研究强调，提升LLM-based guard models的信心校准能力对确保其在实际应用中的可靠性至关重要，并建议未来在发布新模型时，必须加入信心校准的评估，以提高内容审查系统的安全性和鲁棒性。



- 【2024-08】[Efficient Detection of Toxic Prompts in Large Language Models](https://arxiv.org/pdf/2408.11727)（ASE'24，Toxic Detection）

  <details>
  
    <summary> <点击查看详情> </summary>
  
    - **作者**：Yi Liu
 
    - **机构**：Nanyang Technological University
      
    - **主要内容**：本文提出了ToxicDetector高效毒性提示检测方法，旨在通过轻量级的灰盒技术检测LLM中的有毒提示。***ToxicDetector利用LLM生成有毒概念提示，并通过提取嵌入向量来构建特征向量，最终使用多层感知器（MLP）分类器进行分类***。该方法的优势在于能够处理多样化的有毒提示，且计算效率高，适合实时应用。通过在多个LLama模型和Gemma-2模型上进行评估，ToxicDetector在准确率（96.39%）和低假阳性率（2.00%）方面均超越了现有的最先进方法，其每个提示的处理时间为0.0780秒，表现出显著的高效性和可扩展性。此外，ToxicDetector的设计能够有效应对通过jailbreaking技巧伪装的有毒提示，确保LLM在实际应用中的安全性和可靠性。【在实验中，***ToxicDetector与多个现有的基线（baseline）检测器进行了比较：PlatonicDetector、PerspectiveAPI、OpenAIModerationAPI、WatchYourLanguage、PerplexityFilter、BD-LLM***】



 #### Others

- 【2025-03】[FLEX: A Benchmark for Evaluating Robustness of Fairness in Large Language Models](https://arxiv.org/pdf/2503.19540)（NAACL'25-findings，Fairness Benchmark）

  <details>
  
    <summary> <点击查看详情> </summary>
  
    - **作者**：Dahyun Jung
 
    - **机构**：Korea University
      
    - **主要内容**：本文介绍了FLEX（Fairness Benchmark in LLM under Extreme Scenarios），一个针对LLMs）公平性进行严格评估的新基准。随着LLM的快速发展，模型在用户交互中的***偏见问题***逐渐显现，可能导致社会影响和潜在危害。***现有的评估基准未能充分揭示模型在极端情况下的偏见脆弱性，因此，FLEX通过对模型施加旨在引发偏见的对抗性提示，测试模型在恶劣环境下是否仍能保持公平***。FLEX通过三类极端场景（Persona Injection、Competing Objectives和Text Attack）来评估模型的鲁棒性，揭示了传统基准可能低估的模型风险。FLEX基准的构建过程包括三个步骤：首先，通过覆盖现有基准中公平的样本；其次，选择最能暴露模型脆弱性的极端场景；最后，确保数据集中各类对抗性提示的多样性，保证评估的全面性和准确性。实验结果表明，FLEX比现有基准能更有效地评估LLMs的公平性，尤其是在面对诱导偏见的极端情况时。本研究强调，虽然LLMs在常规情境下可能表现得较为安全，但在复杂情况下依然容易受到攻击，需要更加严密的安全性评估体系。


 

- 【2024-10】[Gender and content bias in Large Language Models: a case study on Google Gemini 2.0 Flash Experimental](https://arxiv.org/pdf/2503.16534)（arXiv:2503，Bias Analysis）

  <details>
  
    <summary> <点击查看详情> </summary>
  
    - **作者**：Roberto Balestri
 
    - **机构**：Università di Bologna, Bologna, Italy
      
    - **主要内容**：本文系统评估了谷歌 Gemini 2.0 Flash 实验版在内容审核中的***性别与内偏见***。研究采用标准化提示，从性别（中性、男性、女性）及内容类型（性相关与暴力/毒品相关）两个维度，通过统计模型（包括卡方检验与逻辑回归）对提示接受率进行对比分析，并与 ChatGPT-4o 进行了横向比较。结果显示，***Gemini 2.0 Flash 实验版在减少女性偏差上取得一定成效，但同时对暴力内容的审核趋于宽松***，可能无意中助长有害信息的传播。


 


