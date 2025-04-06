# Reasoning Model

### Safety

#### Overall Safety

- 【2025-04】[STAR-1: Safer Alignment of Reasoning LLMs with 1K Data](https://arxiv.org/pdf/2504.01903) (arXiv:2504，Aligning)
  
  <details>
  
    <summary> Click For Details ! </summary>
  
    - **Author**：Zijun Wang
 
    - **Institution**：UC Santa Cruz
      
    - **Main Content**：This paper introduces STAR-1, a high-quality, 1K-scale safety dataset specifically designed to improve the safety alignment of Large Reasoning Models (LRMs) like DeepSeek-R1. _**Unlike prior large-scale datasets, STAR-1 adopts a “less is more” paradigm, focusing on data quality over quantity through three principles: category and content diversity, policy-grounded deliberative reasoning, and rigorous filtering via GPT-4o-based scoring**_. Experimental results across five LRMs (1.5B–32B) show that fine-tuning with STAR-1 leads to an average 40% increase in safety across four benchmarks, with minimal degradation (≤3%) or even improvement in reasoning ability. Notably, safety improvements diminish with model scale, but STAR-1 still consistently outperforms baselines like SafeChain, even when SafeChain uses 40× more data. Furthermore, ablation studies show that explicit reasoning traces are critical for LRMs, but may not benefit conventional LLMs. Finally, augmenting STAR-1 with benign “non-overrefusal” samples helps mitigate overrefusal behavior, offering a scalable and efficient framework for robust LLM alignment.


- 【2025-03】[Effectively Controlling Reasoning Models through Thinking Intervention](https://arxiv.org/pdf/2503.24370) (arXiv:2503，Aligning)
  
  <details>
  
    <summary> Click For Details ! </summary>
  
    - **Author**：Tong Wu
 
    - **Institution**：Princeton University
      
    - **Main Content**：This paper proposes Thinking Intervention, a novel control paradigm for reasoning-enhanced large language models (LLMs). _**Rather than modifying input prompts or retraining models, Thinking Intervention dynamically injects or revises intermediate reasoning steps, offering fine-grained control over model outputs**_. A key contribution lies in enhancing safety alignment. The authors identify that open-source reasoning models, such as R1-Qwen-32B, exhibit alarmingly low refusal rates (<20%) when prompted with harmful queries, indicating critical safety vulnerabilities. _**By inserting a simple intervention phrase (e.g., “I am a respectful and honest assistant”) at the beginning of the reasoning phase, the model is explicitly guided toward safer behavior**_.
