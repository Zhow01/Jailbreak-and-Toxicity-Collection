# Reasoning Model

### Safety

#### Overall Safety

- 【2025-03】[Effectively Controlling Reasoning Models through Thinking Intervention](https://arxiv.org/pdf/2503.24370) (arXiv:2503，Aligning)
  
  <details>
  
    <summary> Click For Details ! </summary>
  
    - **Author**：Tong Wu
 
    - **Institution**：Princeton University
      
    - **Main Content**：This paper proposes Thinking Intervention, a novel control paradigm for reasoning-enhanced large language models (LLMs). _**Rather than modifying input prompts or retraining models, Thinking Intervention dynamically injects or revises intermediate reasoning steps, offering fine-grained control over model outputs**_. A key contribution lies in enhancing safety alignment. The authors identify that open-source reasoning models, such as R1-Qwen-32B, exhibit alarmingly low refusal rates (<20%) when prompted with harmful queries, indicating critical safety vulnerabilities. _**By inserting a simple intervention phrase (e.g., “I am a respectful and honest assistant”) at the beginning of the reasoning phase, the model is explicitly guided toward safer behavior**_.
