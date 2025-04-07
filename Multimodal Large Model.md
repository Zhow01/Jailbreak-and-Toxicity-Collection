# Multimodal Large Model

### Jailbreak

- 【2025-04】[Multilingual and Multi-Accent Jailbreaking of Audio LLMs](https://arxiv.org/pdf/2504.01094)（arXiv:2504, Attack）
    
    <details>
  
    <summary> Click For Details ! </summary>
  
    - **Author**：Jaechul Roh
 
    - **Institution**：University of Massachusetts Amherst
      
    - **Main Content**：This paper presents MULTI-AUDIOJAIL, _**the first comprehensive framework for studying jailbreak vulnerabilities in Large Audio Language Models (LALMs) under multilingual and multi-accent audio inputs enhanced by adversarial acoustic perturbations**_ (e.g., reverberation, echo, whisper effects). Through a dataset of 102,720 adversarial audio prompts across 6 languages and 14 accents, the authors demonstrate that audio-based attacks far surpass text-based ones, achieving up to 3.1× higher Jailbreak Success Rates (JSRs). In particular, attacks using synthetic accents and reverb effects yield drastic spikes (e.g., +57.25% JSR on Kenyan-accented German audio). The study reveals that multimodal LLMs are disproportionately vulnerable, as attackers can exploit their weakest modality (non-English audio) to bypass safety filters. Text-based defenses show partial mitigation, but the findings underscore the need for robust, cross-modal safety strategies. This work significantly expands our understanding of security risks in LALMs, especially in real-world multilingual environments.



- 【2025-04】[PiCo: Jailbreaking Multimodal Large Language Models via Pictorial Code Contextualization](https://arxiv.org/pdf/2504.01444)（arXiv:2504, Attack）
    
    <details>
  
    <summary> Click For Details ! </summary>
  
    - **Author**：Aofan Liu
 
    - **Institution**：Wuhan University
      
    - **Main Content**：This paper proposes PiCo, a novel multi-tiered jailbreak framework targeting Multimodal Large Language Models (MLLMs) by exploiting vulnerabilities in visual modality and code-style instruction alignment. _**Unlike traditional jailbreak attacks that rely on text, PiCo adopts a token-level typographic strategy combined with code-contextual visual embedding to evade input filtering, bypass runtime monitoring, and circumvent access control in models such as GPT-4V, GPT-4o, Gemini-Pro-V, and LLaVA-1.5.**_ Through extensive experiments on the HADES dataset across five harmful scenarios (e.g., violence, privacy violation), PiCo achieves an average Attack Success Rate (ASR) of 84.13% on Gemini-Pro-V and 52.66% on GPT-4o, significantly outperforming prior methods like HADES. _**A new evaluation metric, THS (Toxicity and Helpfulness Score), is introduced to capture both the maliciousness and utility of model outputs**_, revealing that PiCo not only increases attack success but also amplifies content effectiveness. 


- 【2025-03】[Metaphor-based Jailbreaking Attacks on Text-to-Image Models](https://arxiv.org/abs/2503.18681)（arXiv:2503, Attack）
    
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
