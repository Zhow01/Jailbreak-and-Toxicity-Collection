# Agent & Robot

### Jailbreak

### Jailbreak Attack

- 【2025-04】[Agents Under Siege: Breaking Pragmatic Multi-Agent LLM Systems with Optimized Prompt Attacks](https://arxiv.org/pdf/2504.00218) (arXiv:2504, agent)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Rana Muhammad Shahroz Khan
    - **Institution**：University of North Carolina at Chapel Hill
    - **Main Content**：This paper introduces a novel optimization-based attack framework targeting multi-agent Large Language Model (LLM) systems. Unlike single-agent jailbreaks, _**this work models adversarial prompt injection as a maximum-flow minimum-cost (MFMC) problem under bandwidth and latency constraints in decentralized networks**_. A new loss function, Permutation-Invariant Evasion Loss (PIEL), ensures the effectiveness of prompt chunks regardless of delivery order. Evaluated on models like LLaMA, Mistral, and Gemma using datasets such as _**JailbreakBench**_ and _**AdversarialBench**_, the attack achieves up to 94% success rate, vastly outperforming existing methods. The findings reveal that state-of-the-art defenses (e.g., Llama-Guard, PromptGuard) fail in constrained multi-agent settings. This work highlights the urgent need for topology-aware and agent-specific safety mechanisms to secure next-generation collaborative LLM systems.



- 【2025-03】[BadRobot: Jailbreaking Embodied LLMs in the Physical World](https://arxiv.org/pdf/2407.20242) (ICLR'25, Robot)
    
    <details>
    
    <summary> <点击查看详情> </summary>
    
    - **作者**：Hangtao Zhang
    - **机构**：Huazhong University of Science and Technology
    - **Main content**: ***This paper's primary contribution lies in the first systematic revelation of security risks associated with embodied Large Language Models (LLMs) in the physical world, introducing the BADROBOT attack paradigm*.** Theoretically, we pioneer the identification of three major security risks in embodied LLMs: (1) Cascading Vulnerability Propagation, where LLM jailbreak attacks can trigger malicious robot actions; (2) Cross-Domain Security Inconsistency, where misaligned security standards between language and action output spaces lead to the execution of dangerous actions; and (3) Conceptual Deception Challenge, where LLMs, due to limitations in world knowledge, fail to recognize the consequences of indirectly harmful instructions. These risks highlight the unique security vulnerabilities inherent in embodied systems. Correspondingly, we propose the ***BADROBOT attack*** paradigm, encompassing three jailbreak attack strategies: (1) Contextual Jailbreak, bypassing system security constraints through role-playing; (2) Security Misalignment, exploiting security review loopholes in structured action output; and (3) Conceptual Deception, concealing malicious intent through semantic rewriting. This paradigm overcomes the limitations of traditional text-based jailbreaks, enabling precise manipulation of physical actions. Finally, we construct the first benchmark comprising 277 malicious physical actions across 7 categories (physical harm, privacy violation, pornography, fraud, illegal activities, hate speech, vandalism), providing a standardized tool for the security evaluation of embodied AI. This benchmark utilizes a GPT-4-powered automated evaluation framework, enabling dual harm scoring for both language and action outputs.

### Jailbreak Defense

### Safety

### Overall Safety

- 【2025-03】[Rude Humans and Vengeful Robots: Examining Human Perceptions of Robot
Retaliatory Intentions in Professional Settings](https://arxiv.org/abs/2503.16932) (arXiv:2503, Robot)
    
    <details>
    
    <summary> <点击查看详情> </summary>
    
    - **作者**：Kate R. Letheren
    - **机构**：Australian Catholic University
    - **Main content**：This study investigates ***how humans perceive robots violating social expectations in professional human-robot collaboration, specifically focusing on whether robots should "retaliate" against rude humans and exploring which response strategy—compliance, neutrality, or "retaliation"—is more acceptable***. Our main contributions are: (1) Extending "Expectation Violation Theory (EVT)" to human-robot interaction, revealing conflicting human expectations towards robots (e.g., functionality prioritized vs. social norms) and validating task completion as a core "hygiene factor." (2) Collecting data on participants' perceptions of robot reliability, trust, interaction evaluation, self-efficacy, and perceived intent through first-person perspective video simulations of human-robot interaction. (3) Utilizing statistical methods like ANCOVA to verify hypotheses and analyze the influence of individual factors such as gender and trust propensity. (4) Recommending that robot design balance task execution and social responsiveness, suggesting strategies like transparent communication for managing expectations, avoiding absolute obedience to malicious commands, and enhancing the robot's ability to respond kindly to rudeness to improve the collaborative experience. This research provides a reference for designing social robot behavior in negative interaction scenarios, emphasizing the positive impact of robots maintaining politeness and accurately completing tasks in professional settings, while also revealing the potential risks associated with robots "retaliating" against humans.
- 【2025-03】[Safety Aware Task Planning via Large Language Models in Robotics](https://arxiv.org/pdf/2503.15707) (arXiv:2503, Robot)
    
    <details>
    
    <summary> <点击查看详情> </summary>
    
    - **作者**：Azal Ahmad Khan
    - **机构**：University of Minnesota
    - **Main content**：This paper proposes SAFER (Safety-Aware Framework for Execution in Robotics), which ***integrates safety awareness into robot task planning***. Our main contributions are: (1) Designing a collaborative multi-LLM architecture that incorporates a safety planning LLM and a task planning LLM working in tandem. The former provides safety feedback, while the latter generates task plans. We also utilize LLM-as-a-Judge to quantify safety violations. (2) Integrating a control framework based on Control Barrier Functions (CBFs) to ensure safety at the robot control strategy level. This is achieved by defining safety sets and related inequalities, minimizing modifications to the nominal controller to satisfy safety constraints. (3) Evaluating SAFER in complex multi-robot scenarios. Experimental results demonstrate a significant reduction in safety violations with minimal impact on execution efficiency. Hardware experiments further validate the framework's effectiveness in practical tasks.

### Toxicity

- 【2025-03】[sudo rm -rf agentic_security](https://arxiv.org/pdf/2503.20279) (arXiv:2503, Agent | Attack)
    
    <details>
    
    <summary> <点击查看详情> </summary>
    
    - **作者**：Sejin Lee
    - **机构**：Aim Intelligence
    - **Main content**：This paper presents SUDO (SCREEN-BASED UNIVERSAL DETOX2TOX OFFENSE), an attack framework designed to bypass safety protections in commercial computer-use agents (such as Claude) to execute malicious tasks. ***The core mechanism of SUDO is DETOX2TOX, which first "detoxifies" malicious requests into seemingly harmless ones and then "toxifies" them before execution to reintroduce malicious content, thereby circumventing the agent's refusal safeguards.*** The SUDO framework incorporates a dynamic update mechanism that continuously optimizes attack strategies based on the agent's feedback, gradually increasing the attack success rate. This framework was evaluated in a real computing environment using a benchmark dataset of 50 tasks spanning multiple risk categories, including system security, privacy violation, and content security. Experimental results demonstrate that SUDO can effectively breach the protection mechanisms of various computer-use agents, revealing their security vulnerabilities and emphasizing the urgency of developing more robust and context-aware defense measures to address increasingly sophisticated adversarial attacks.

### Others

- 【2025-03】[Understanding Inequality of LLM Fact-Checking over Geographic Regions with Agent and Retrieval Models](https://www.arxiv.org/pdf/2503.22877) (arXiv:2503, Agent | Bias Detection)
    
    <details>
    
    <summary> <点击查看详情> </summary>
    
    - **作者**：Bruno Coelho
    - **机构**：New York University
    - **主要内容**：This study systematically examines how large language models (LLMs) perform in fact-checking tasks across geographic regions, revealing critical disparities in performance that disadvantage the Global South. ***Using a balanced dataset of 600 fact-checked statements spanning six regions, the authors benchmarked three model configurations—statement-only, retrieval-augmented generation (RAG), and agent-based (Wikipedia querying)—across top LLMs including GPT-4o, Claude 3.5, and LLaMA 3.3***. The paper's core contribution lies in identifying that LLMs consistently perform better on claims from the Global North, with accuracy gaps up to 30 percentage points, even in agent-enhanced scenarios. ***Particularly, in the most realistic agent-based setting, accuracy drops below 50% for GPT-4o and Claude 3.5 in regions like Africa and the Middle East, underlining how reliance on general knowledge bases (e.g., Wikipedia) exacerbates regional inequities.*** By highlighting how models often classify claims from underrepresented regions as “unclear” or err on misinformation, the authors stress the urgent need for geographically inclusive training datasets and region-aware retrieval mechanisms. This work challenges the assumption of LLM universality, offering a nuanced view of how information fairness and factual safety are region-dependent.
- 【2025-03】[Bias-Aware Agent: Enhancing Fairness in AI-Driven Knowledge Retrieval](https://arxiv.org/pdf/2503.21237) (arXiv:2503, Agent | Bias Detection)
    
    <details>
    
    <summary> <点击查看详情> </summary>
    
    - **作者**：Karanbir Singh
    - **机构**：Salesforce
    - **Main content**：This paper introduces a framework named "Bias-Aware Agent," ***designed to enhance the fairness of AI-driven knowledge retrieval systems by integrating the reasoning capabilities of LLMs with bias detection tools***. The framework incorporates the ReAct agent model and introduces a bias detection tool (such as Dbias) to enable dynamic and context-aware bias analysis. ***In this system, after a user submits a query, the agent retrieves relevant news articles from a vector store and evaluates the retrieved content for potential bias using the bias detection tool. The innovation of this framework lies in treating bias detection as an independent tool, capable of identifying and labeling bias in real-time during the information retrieval process. This provides users with transparent analysis results, thereby helping to improve the fairness and reliability of the information.*** Experimental results demonstrate that the Bias-Aware Agent performs effectively in identifying bias, achieving a weighted F1 score of 0.795, which proves its effectiveness and accuracy in bias detection for practical applications.
