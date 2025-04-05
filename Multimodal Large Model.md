# Multimodal Large Model

### Jailbreak Attack & Defense

### Jailbreak Attack

- 【2025-03】[Metaphor-based Jailbreaking Attacks on Text-to-Image Models](https://arxiv.org/abs/2503.18681)（arXiv:2503）
    
    <details>
    
    <summary> <点击查看详情> </summary>
    
    - **作者**：Chenyu Zhang
    - **机构**：Tianjin University
    - **Main content**：This paper proposes MJA (Metaphor-based Jailbreaking Attack), a jailbreaking attack method designed to bypass safety filters in text-to-image (T2I) models to generate sensitive images. Compared to existing methods, MJA significantly reduces the number of queries required while improving attack effectiveness. The MJA method consists of two main modules: ***(1) Multi-Agent Generation Module based on LLM (MLAG):*** This module decomposes the process of generating metaphorical adversarial prompts into three sub-tasks: metaphor retrieval, context matching, and adversarial prompt generation. MLAG coordinates three LLM agents to explore various combinations of metaphors and contexts, generating a diverse set of adversarial prompts. ***(2) Adversarial Prompt Optimization Module (APO):*** This module first trains a proxy model to predict the attack effectiveness of adversarial prompts and then designs an acquisition strategy to adaptively identify the optimal adversarial prompts, thereby enhancing attack efficiency.

### Jailbreak Defense

### Safety

### Overall Safety

### Toxicity

### Others

- 【2025-03】[Commander-GPT: Fully Unleashing the Sarcasm Detection Capability of Multi-Modal Large Language Models](https://arxiv.org/abs/2503.18681)（arXiv:2503，Sarcasm Detection）
    
    <details>
    
    <summary> <点击查看详情> </summary>
    
    - **作者**：Yazhou Zhang
    - **机构**：None
    - **Main content**：This paper introduces Commander-GPT, a multimodal large model (MLLM) framework designed to fully leverage ***multimodal information for sarcasm detection***. Inspired by military strategy, the authors divide the sarcasm detection task into six sub-tasks: text sentiment analysis, image content recognition, text-image consistency check, contextual relationship analysis, application of cultural and background knowledge, and sarcasm judgment. ***A central commander (the decision-maker) assigns the most suitable large language model to each sub-task,*** and the detection results from each model are ultimately aggregated to identify sarcastic content. In terms of model architecture, Commander-GPT adopts a commander-troop structure from military strategy, where each sub-task is treated as an independent "troop" dispatched by the central "commander." Specifically, the commander assigns the most appropriate large language model (such as GPT-4o mini, O3 mini, etc.) to each sub-task based on the task requirements. Each model independently processes its assigned sub-task, and their respective output results are then aggregated to identify sarcasm.
