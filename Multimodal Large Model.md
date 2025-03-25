# Multimodal Large Model
### Jailbreak Attack & Defense
#### Jailbreak Attack


#### Jailbreak Defense



### Safety

#### Overall Safety

- 【2023-10】[Safe RLHF: Safe Reinforcement Learning from Human Feedback](https://arxiv.org/pdf/2310.12773)（ICLR'24，Aligning）
  
  <details>
  
    <summary> <点击查看详情> </summary>
  
    - **作者**：Josef Dai
 
    - **机构**：Peking University
      
    - **主要内容**：本文提出了一种Safe Reinforcement Learning from Human Feedback（Safe RLHF）算法，旨在解决LLM在训练过程中有用性和无害性目标之间的矛盾【​***有用性指模型提供有价值、相关且实用信息的能力，而无害性则指模型避免生成有害、冒犯性或不当内容的能力。​这两个目标之间存在矛盾，即在追求提高模型有用性的同时，可能增加生成有害内容的风险***】，以实现人类价值观的对齐。​Safe RLHF通过明确区分人类对有用性和无害性的偏好，避免了众包工作者的混淆，使我们能够分别训练奖励模型和成本模型。​该方法将安全问题形式化为在满足特定成本约束的同时最大化奖励函数的优化任务。​通过拉格朗日方法求解这一约束问题，Safe RLHF在微调过程中动态调整两个目标之间的平衡。​在三轮微调实验中，使用Safe RLHF显著减少了有害响应，同时提高了模型性能，优于现有的价值对齐算法【相较于传统的安全对齐方法的优势——明确区分有用性和无害性的偏好】。

#### Toxicity





 #### Bias
