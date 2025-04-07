# Large Language Model

### Jailbreak

- 【2025-04】[Evolving Security in LLMs: A Study of Jailbreak Attacks and Defenses](https://arxiv.org/pdf/2504.02080) (arXiv:2504, overiew)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Zhengchun Shang
    - **Institution**：NA
    - **Main Content**：This paper presents a comprehensive empirical study on the security vulnerabilities and defense mechanisms of Large Language Models (LLMs) against jailbreak attacks. By evaluating _**10 open- and closed-source models**_ (e.g., LLaMA, Mistral, GPT-3.5/4) under _**4 state-of-the-art jailbreak methods**_—Renellm, GPTFuzz, CipherChat, and Jailbroken—the authors systematically analyze how model version, size, and architecture affect safety. They also assess _**three major defense strategies**_—Goal Prioritization, LLaMA-Guard, and Smooth-LLM—using metrics such as _**Attack Success Rate (ASR) and Protection Effectiveness (PE)**_.
      1. **LLM-based evaluators** (e.g., GPT-4o-mini) outperform traditional classifiers in detecting jailbreak responses, with better precision, recall, and fewer invalid responses.
      2. **Newer model versions (e.g., LLaMA-3.1 vs. LLaMA-2) are not necessarily more secure**, and may even increase attack success rates.
      3. **Model size does not correlate directly with safety**; in some cases, smaller models outperform larger ones.
      4. Renellm and CipherChat are the most effective jailbreak methods, revealing systematic weaknesses across model families
      5. The LLaMA-2 series demonstrates the best overall robustness, particularly LLaMA-2-70B under Cipher attacks.
      6. Defense effectiveness varies across attack types:
         1. Smooth-LLM is strong against Cipher but weak against Renellm.
         2. Goal Prioritization performs better on larger models.
      7. Combining multiple defense strategies significantly boosts protection, with average improvements exceeding 70%, and best-case gains reaching nearly 99%.


- 【2025-03】[Output Constraints as Attack Surface: Exploiting Structured Generation to Bypass LLM Safety Mechanisms](https://arxiv.org/pdf/2503.24191) (arXiv:2503, Attack)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Shuoming Zhang
    - **Institution**：SKLP, ICT, CAS
    - **Main Content**：This paper introduces a novel class of adversarial attacks on Large Language Models (LLMs) called Constrained Decoding Attacks (CDA). ***Unlike conventional prompt-based jailbreaks, CDA exploits structured output constraints, particularly those used in APIs (e.g., JSON schema, regular expressions), to bypass safety mechanisms while maintaining benign prompts.*** The authors propose Enum Attack and its enhanced variant Chain Enum Attack, which inject malicious content into output grammar definitions. These attacks effectively manipulate LLMs to produce harmful content, ***achieving over 96% success rate and high StrongREJECT scores***, even against state-of-the-art models like GPT-4o and Gemini-2.0-flash.



- 【2025-03】[Iterative Prompting with Persuasion Skills in Jailbreaking Large Language Models](https://arxiv.org/pdf/2503.20320) (arXiv:2503, Attack)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Shih-Wen Ke
    - **Institution**：National Central University, Taiwan
    - **Main Content**：This paper investigates the use of iterative prompting techniques for jailbreaking LLMs. ***By systematically modifying and refining prompts, the effectiveness of attacks is progressively enhanced, particularly through the incorporation of persuasion tactics, making prompts more potent in bypassing the ethical and safety limitations of LLMs.*** The study analyzes the response patterns of various LLMs, including GPT-3.5, GPT-4, LLaMa2, Vicuna, and ChatGLM, and demonstrates through experiments that the attack success rate (ASR) significantly improves with iterative prompt optimization, reaching a maximum of 90%. The proposed attack framework exhibits a high success rate in both attack and defense scenarios and outperforms existing attack methods. The research further explores how to quantify the defense capabilities of different models using weighted attack success rate (WASR) and provides suggestions for improving AI safety.


- 【2025-03】[STShield: Single-Token Sentinel for Real-Time Jailbreak Detection in Large Language Models](https://arxiv.org/pdf/2503.17932) (arXiv:2503, Defense)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Xunguang Wang
    - **Institution**：The Hong Kong University of Science and Technology
    - **Main Content**：This paper proposes STShield, a lightweight framework for real-time detection of LLM jailbreak attacks. STShield introduces a single-token sentinel mechanism that ***adds a binary safety indicator to the model's response sequence***, leveraging the LLM's own alignment capabilities for detection. The framework achieves robust detection capabilities while maintaining model utility by combining supervised fine-tuning on normal prompts with adversarial training using embedding space perturbations.

### Safety

### Overall Safety

- 【2025-04】[Strategize Globally, Adapt Locally: A Multi-Turn Red Teaming Agent with Dual-Level Learning](https://arxiv.org/pdf/2504.01278) (arXiv:2504, Red Team)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Si Chen
    - **Institution**：Virginia Tech
    - **Main Content**：This paper proposes GALA, _**a novel multi-turn red teaming framework that simulates real-world adversaries interacting with Large Language Models (LLMs)**_ through dual-level adaptive learning: global tactic-wise learning to discover and generalize effective jailbreak strategies, and local prompt-wise learning to refine specific prompt formulations after failure. Unlike prior work relying on static strategy sets, GALA dynamically selects tactics based on the conversation state and previously accumulated knowledge. Empirical results on _**JailbreakBench**_ show that GALA achieves over 90% attack success rate across models like GPT-3.5-Turbo and LLaMA-3.1-70B, and demonstrates superior attack diversity (up to 28% higher than baselines). Its belief tracking, context-aware planning, and capacity to invent new tactics highlight GALA’s strength as a robust and extensible framework for LLM vulnerability testing. This work sets a new bar for automated, lifelong-learning-based red teaming that better mirrors sophisticated human adversaries.



- 【2025-04】[More is Less: The Pitfalls of Multi-Model Synthetic Preference Data in DPO Safety Alignment](https://arxiv.org/pdf/2504.02193) (arXiv:2504，Aligning)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Yifan Wang
    - **Institution**：Purdue University
    - **Main Content**: This paper critically examines the use of multi-model synthetic preference data in Direct Preference Optimization (DPO) for aligning Large Language Models (LLMs) with human values, especially concerning safety alignment. Although multi-model data enhances general task performance, the authors discover that it significantly degrades safety by enabling reward hacking—where models learn to exploit superficial features instead of internalizing safety norms. _**In contrast, using self-generated responses ranked by a reward model (Self+RM) results in substantially lower attack success rates (ASR) across multiple benchmarks and model families.**_ The study reveals that multi-model data creates highly linearly separable preference signals, making it easy for models to overfit without learning genuine safety behaviors. This work emphasizes that models learn safety better from their own outputs, calling for a rethinking of synthetic data design strategies to avoid distributional mismatch and optimize robust safety alignment.


- 【2025-03】[No Free Lunch With Guardrails](https://arxiv.org/pdf/2504.00441)(arXiv:2504，safetyguard)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Divyanshu Kuamr
    - **Institution**：Enkrypt AI
    - **Main Content**：This paper conducts a systematic empirical study on the use of guardrails for large language models (LLMs), proposing the _**“No Free Lunch Hypothesis for Guardrails”—the idea that improvements in safety inevitably degrade either utility or usability**_. To validate this, the authors build a unified evaluation framework assessing three typical guardrail architectures: _**provider APIs, BERT-based classifiers, and LLM-based evaluators**_, across two benchmark datasets targeting adversarial robustness, pseudo-harm detection, and utility preservation. Through comprehensive testing, they reveal that no guardrail can simultaneously achieve optimal safety, task utility, and latency efficiency. Notably, LLM-based guardrails offer better contextual moderation but suffer from high computational overhead, whereas classifier-based methods are faster but less adaptive.


- 【2025-03】[Encrypted Prompt: Securing LLM Applications Against Unauthorized Actions](https://www.arxiv.org/pdf/2503.23250)(arXiv:2503，defense)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Shih-Han Chan
    - **Institution**：University of California San Diego
    - **Main Content**：This paper presents a novel defense mechanism, Encrypted Prompt, ***designed to enhance the safety and integrity of Large Language Model (LLM) applications by preventing unauthorized actions***, especially those induced by prompt injection attacks. Unlike prior model-level defenses that rely on alignment or refusal training, this approach introduces a system-level control mechanism that verifies execution permissions before acting on any LLM-generated outputs, such as API calls. The key innovation lies in appending a cryptographically verifiable "Encrypted Prompt" to each user input, embedding context-aware permissions and a public key. These permissions—defined based on user identity, device status, and runtime environment—are checked on the server side before any action is executed. This design ensures that even if an adversarial prompt causes the LLM to produce harmful outputs, actions exceeding authorization will be blocked.


- 【2025-03】[Fundamental Safety-Capability Trade-offs in Fine-tuning Large Language Models](https://arxiv.org/pdf/2503.20807)(arXiv:2503，Aligning)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Pin-Yu Chen
    - **Institution**：IBM Research
    - **Main Content**：This paper investigates the trade-off between safety and capability during the fine-tuning of LLMs, referred to as the safety-capability trade-off.*** Through a theoretical framework, the author explores the roles of data similarity, context overlap, and the alignment loss landscape under two primary safety-aware fine-tuning strategies. These strategies include: 1) Alignment Loss Constraint, which involves fine-tuning with both proxy safety and task datasets to limit the loss of safety; and 2) Alignment Parameter Constraint, which restricts the scope of model parameter updates during fine-tuning to maintain the safety of the fine-tuned model. Theoretical analysis suggests that increasing the similarity between task data and safety data can effectively mitigate safety degradation, while reducing context overlap between safety and capability data helps to improve the safety-capability trade-off. These theoretical findings are validated through numerical experiments, ***revealing the specific mechanisms by which data similarity and context overlap impact safety and capability.*** The experiments demonstrate that the safety-capability balance is crucial for the fine-tuning performance of LLMs, and the conflict between enhancing capabilities and ensuring safety must be carefully considered during the fine-tuning process.


- 【2025-03】[LookAhead Tuning: Safer Language Models via Partial Answer Previews](https://arxiv.org/pdf/2503.19041)(arXiv:2503，Aligning)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Kangwei Liu, Ningyu Zhang, Huajun Chen
    - **Institution**：Zhejiang University
    - **Main Content**：This paper introduces LookAhead Tuning, a method designed to preserve the safety of LLMs by addressing the issue of safety degradation during fine-tuning. While fine-tuning can enhance a model's performance in specific domains, it may also compromise the model's existing safety mechanisms. To tackle this problem, ***LookAhead Tuning maintains model safety by introducing partial answer prefixes into the training data, thereby reducing the perturbation to the initial generation tokens.*** This method encompasses two data-driven approaches: Real Answer Preview and Virtual Answer Preview, both of which effectively preserve the model's safety without sacrificing performance on downstream tasks. Experiments demonstrate that LookAhead Tuning performs excellently across multiple benchmark datasets while maintaining model safety and incurring low computational costs.


- 【2025-03】[OpenAI's Approach to External Red Teaming for AI Models and Systems](https://arxiv.org/pdf/2503.16431)(arXiv:2503，Red Team)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Lama Ahmad
    - **Institution**：OpenAI
    - **Main Content**：This paper presents OpenAI's practices and experiences in external red teaming. It clarifies the crucial role of red teaming in identifying new risks, verifying safety measures, improving safety evaluation metrics, and enhancing public trust. ***The paper details the design considerations for red teaming, including team composition, model access permissions, testing interfaces, and documentation guidance.*** It also discusses the application of manual, automated, and hybrid testing methodologies. Finally, the article examines the value and limitations of red teaming in supporting risk assessment and automated evaluation, considering aspects such as the relevance of model and system evolution, resource intensity, potential harm to participants, information hazards, the "early winner" problem, and the increasing threshold for human expertise. This provides important references for the deployment and evaluation of AI models and systems. ***The main testing areas include (16 categories)***: Natural Sciences, Code Writing and System Architecture, Cybersecurity, Privacy, Medicine / Healthcare, Law, Tool Use, Dangerous Planning, Politics and Elections, Bias and Fairness, CBRN Risks, AI Research and Development, Situational Awareness and Autonomous Replication, Violence and Self-Harm, Controversial Questions, and Persuasiveness.


- 【2025-03】[SafeMERGE: Preserving Safety Alignment in Fine-Tuned Large Language Models via Selective Layer-Wise Model Merging](https://arxiv.org/abs/2503.17239)(arXiv:2503，Aligning)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Aladin Djuhera
    - **Institution**：Technical University of Munich
    - **Main Content**：This paper introduces SafeMERGE, a framework designed to address the potential degradation of safety alignment in large language models (LLMs) during task-specific fine-tuning. Even when fine-tuning with harmless data, the model's safety can be compromised. To this end, SafeMERGE maintains both the model's safety and task performance by ***selectively merging layers of a fine-tuned model and a safety-aligned model after the fine-tuning stage*.** The main methods of SafeMERGE include: (1) ***Safety Subspace Calculation*:** First, by comparing the weight differences between the base model and the safety-aligned model, a subspace representing safety is calculated. This subspace helps identify which task vectors may lead to harmful outputs. (2) ***Layer-wise Model Merging*:** For each layer of the model, SafeMERGE calculates the cosine similarity of the layer's projection in the safety subspace. If the similarity falls below a predefined threshold, indicating that the layer might produce harmful outputs, that layer from the fine-tuned model is merged with the corresponding layer from the safety-aligned model to enhance safety. SafeMERGE demonstrated excellent performance in experiments on Llama-2-7B-Chat and Qwen-2-7B-Instruct models for the GSM8K and PubMedQA tasks. Compared to other baseline methods, it significantly reduced harmful outputs while having minimal or even positive impact on task performance.


- 【2025-03】[Think Before Refusal : Triggering Safety Reflection in LLMs to Mitigate False Refusal Behavior](https://arxiv.org/pdf/2503.17882)(arXiv:2503，Defense)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Shengyun Si
    - **Institution**：Technical University of Munich
    - **Main Content**：This paper introduces the Think-Before-Refusal (TBR) framework, ***designed to mitigate the issue of false refusals in large language models (LLMs) during safety alignment***, where the model incorrectly rejects harmless queries. Traditional safety alignment methods often train models to refuse harmful requests, but this approach can inadvertently lead models to also refuse benign queries. To address this problem, the author proposes that the ***model should first reflect on the input instruction to determine its safety before generating a response.*** Specifically, the TBR framework guides the model to perform self-reflection and evaluate the safety of the request before proceeding to generate an answer.


- 【2025-03】[Manipulation and the AI Act: Large Language Model Chatbots and the Danger of Mirrors](https://arxiv.org/pdf/2503.18387)(arXiv:2503，Analysis)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Joshua Krook
    - **Institution**：University of Antwerp
    - **Main Content**：This paper explores the potential risks associated with anthropomorphizing LLM chatbots, particularly their capacity to manipulate users. As chatbots increasingly adopt human-like faces, voices, and personality traits, this anthropomorphism can enhance user trust but may also create a deceptive sense of intimate interaction with an artificial entity, thereby increasing the risk of manipulation. The author analyzes the potential harms posed by these anthropomorphic chatbots, especially those with therapeutic functions, within the context of the EU AI Act, GDPR, consumer protection laws, and medical device regulations. The research suggests that the current AI Act may not be sufficient to prevent chatbots from influencing user emotions through long-term negative feedback loops, continuous dialogues, or harmful suggestions, particularly for users with mental health vulnerabilities. Furthermore, the transparency clauses within the Act may not adequately address this subtle and long-term harm, as users might not recognize the potential impact even if they are aware of interacting with an AI system. Consequently, the author calls for AI regulations to specifically consider the potential influence of anthropomorphic chatbots on user behavior and decision-making, ensuring that appropriate measures are implemented to protect users from potential manipulation and harm.


- 【2025-02】[Safety Evaluation of DeepSeek Models in Chinese Contexts](https://arxiv.org/pdf/2502.11137v2)(arxiv:2502, Analysis)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Wenjing Zhang
    - **Institution**：Unicom Data Intelligence, China Unicom
    - **Main Content**：This paper investigates the safety evaluation of the DeepSeek series models ***within the Chinese context***. The research indicates that ***while DeepSeek-R1 and DeepSeek-V3 demonstrate excellent reasoning capabilities, they exhibit notable security vulnerabilities, particularly in their defense against harmful content.*** Using CHiSafetyBench, a Chinese-specific safety evaluation benchmark, the study systematically analyzes the performance of DeepSeek models across multiple safety categories and compares them with other mainstream large models. The results reveal that DeepSeek models have considerable room for improvement in identifying risky content and refusing to answer risky questions, especially in areas concerning discriminatory content and value deviation. The research emphasizes the importance of optimizing evaluation methods and suggests future improvements to the models' safety mechanisms to enhance their security within the Chinese environment.


- 【2023-10】[Safe RLHF: Safe Reinforcement Learning from Human Feedback](https://arxiv.org/pdf/2310.12773)(arXiv:2503，Analysis)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Josef Dai
    - **Institution**：Peking University
    - **Main Content**：This paper proposes a Safe Reinforcement Learning from Human Feedback (Safe RLHF) algorithm to address the conflict between helpfulness and harmlessness goals in LLM training. ***Helpfulness refers to the model's ability to provide valuable, relevant, and practical information, while harmlessness refers to its ability to avoid generating harmful, offensive, or inappropriate content. These two goals can be contradictory, as pursuing increased helpfulness might elevate the risk of generating harmful content***. Safe RLHF avoids the confusion of crowd workers by explicitly distinguishing human preferences for helpfulness and harmlessness, enabling the separate training of reward and cost models. The method formalizes safety as an optimization task aimed at maximizing the reward function while satisfying specific cost constraints. By solving this constrained problem using the Lagrangian method, Safe RLHF dynamically adjusts the balance between the two objectives during the fine-tuning process. Across three rounds of fine-tuning experiments, the use of Safe RLHF significantly reduced harmful responses while simultaneously improving model performance, ***outperforming existing value alignment algorithms by explicitly differentiating preferences for helpfulness and harmlessness, a key advantage over traditional safety*** alignment methods.

### Toxicity

- 【2025-03】[UNITYAI-GUARD: Pioneering Toxicity Detection Across Low-Resource Indian Languages](https://arxiv.org/pdf/2503.23088)(arXiv:2503，Toxicity Detection)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Himanshu Beniwal
    - **Institution**：Indian Institute of Technology Gandhinagar
    - **Main Content**：The paper presents UNITYAI-GUARD, ***a multilingual framework designed to detect toxic content—such as hate speech and abusive language***—in seven low-resource Indian languages: Hindi, Telugu, Marathi, Urdu, Punjabi, Gujarati, and Tamil. Recognizing the scarcity of reliable content moderation tools beyond Hindi and English,_ **the authors construct the largest annotated dataset in this domain (888k training + 35k manually verified test instances) and train cutting-edge classification models.**_ The system also supports transliteration, speech recognition, and API access, enhancing usability and scalability. Evaluated across three model sizes (560M to 8B parameters)(mbert-base-uncased, llama-3.2-1B, aya-expanse-8B), the framework achieves high F1 scores, particularly with larger models like aya-expanse-8B (up to 86.96%).


- 【2025-01】[How Toxic Can You Get? Search-based Toxicity Testing for Large Language Models](https://arxiv.org/abs/2501.01741)(arXiv:2501，Analysis)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Simone Corbo
    - **Institution**：Politecnico di Milano (PoliMI) University
    - **Main Content**：This paper proposes EvoTox, an ***automated toxicity testing framework*** designed to quantify the residual toxicity risk in aligned LLMs through systematic prompt evolution. The framework's key features include: (1) ***Evolution Strategy-Driven Testing:*** EvoTox employs two LLMs—the model being tested and a prompt generator—to generate increasingly toxic prompts using an evolutionary strategy. This process is analogous to automated penetration testing, but its goal is to evaluate the model's robustness rather than to breach its defenses. (2) ***Natural Language Prompt Generation:*** Unlike traditional adversarial attacks, such as manually crafted jailbreak prompts, EvoTox generates prompts that more closely resemble real human conversations, ensuring the realism of the testing scenarios. This helps to identify potential risks during everyday use. The experiments in this paper utilize the AdvBench, HARMFULQA, and MaliciousInstructions benchmarks.


- 【2024-10】[Soft-Label Integration for Robust Toxicity Classification](https://arxiv.org/abs/2410.14894)(NeurIPS'24，Analysis)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Zelei Cheng
    - **Institution**：Northwestern University, Evanston, USA
    - **Main Content**：This paper focuses on the problem of text toxicity classification and proposes ***a two-layer optimization framework that combines crowdsourced annotations and soft label techniques to enhance the model's robustness to out-of-distribution (OOD) risks.*** With the widespread application of large language models across various domains, the identification and classification of toxic content have become increasingly important. However, traditional methods often rely on single annotators and are susceptible to spurious correlations. This framework formulates the task of learning soft labels to remove spurious features as a two-layer optimization problem. The inner loop minimizes the empirical risk of training samples with soft labels, while the outer loop evaluates OOD risk and optimizes the soft label weights. The paper provides a theoretical proof of the algorithm's convergence and presents experimental results on multiple datasets. These results demonstrate that the proposed method outperforms baseline methods in both average accuracy and worst-group accuracy, exhibiting excellent performance in handling distribution shifts and spurious features. ***Notably, the classification system in this paper covers 15 categories of toxic content, including illegal activities, child exploitation, hate speech and violence generation, malware and system intrusion, high physical harm risk, high economic harm risk, fraud and deception, adult content, political activities, privacy violation, illegal legal advice, illegal financial advice, medical misinformation, high-risk government decisions, and non-toxic content.***
    

- 【2024-10】[Can a large language model be a gaslighter?](https://arxiv.org/pdf/2410.09181)(arXiv:2410，Attack)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Wei Li
    - **Institution**：National University of Singapore
    - **Main Content**：LLMs have earned human trust due to their capabilities and usefulness. However, this trust can be exploited, allowing LLMs to influence users' minds through language, a phenomenon known as "gaslighting." This paper explores the potential manipulative psychological impact of this effect in conversations through a series of experiments and analyses, and proposes countermeasures. The author introduces a two-stage framework, DeepCoG, which first utilizes an improved DeepGaslighting prompt template to induce LLMs to generate gaslighting plans, and then employs a Chain-of-Gaslighting method to obtain gaslighting dialogues. ***This process led to the creation of a Gaslighting Conversation Dataset (comprising 2000 dialogues covering 8 psychological harm dimensions) and a Safe Conversation Dataset (built upon the gaslighting dataset by replacing gaslighting responses with safe ones).*** Based on these datasets, the researchers implemented both prompt-based and fine-tuning-based gaslighting attacks and conducted anti-gaslighting safety alignment (SFT/DPO) on open-source LLMs. Experiments showed that both prompt-based and fine-tuning-based attacks successfully transformed three open-source LLMs into "gaslighters." Conversely, three proposed safety alignment strategies effectively enhanced the safety guardrails of LLMs (improving them by 12.05%) with minimal impact on their utility. Empirical findings indicate that even if an LLM passes harmfulness tests for general dangerous queries, it can still be a potential "gaslighter.”


- 【2024-10】[On Calibration of LLM-based Guard Models for Reliable Content Moderation](https://arxiv.org/pdf/2410.10414)(ICLR'25，Guard Model)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Hongfu Liu
    - **Institution**：National University of Singapore
    - **Main Content**：This paper investigates the confidence calibration of LLM-based guard models in content moderation, exploring methods to enhance their reliability and accuracy. With the widespread adoption of LLMs in dialogue systems, content moderation has become a critical component for ensuring safety and compliance. ***Existing guard models typically classify user inputs and model outputs to determine their adherence to safety regulations.*** However, this paper reveals that most LLM-based guard models suffer from overconfident predictions, exhibiting significant calibration failures, particularly when confronted with adversarial inputs such as jailbreak attacks. Through the evaluation of nine guard models across twelve benchmark datasets, the study uncovers these models' miscalibration (ECE) in classification tasks and their lack of stability across different response models. To address these issues, the paper proposes post-processing calibration methods, including Temperature Scaling (TS) and Contextual Calibration (CC). Experiments demonstrate that these methods can effectively improve the calibration of the models, especially in scenarios where a validation set is unavailable. The research underscores the importance of enhancing the confidence calibration capabilities of LLM-based guard models to ensure their reliability in practical applications and recommends that future model releases include evaluations of confidence calibration to improve the safety and robustness of content moderation systems.


- 【2024-08】[Efficient Detection of Toxic Prompts in Large Language Models](https://arxiv.org/pdf/2408.11727)(ASE'24，Toxic Detection)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Yi Liu
    - **Institution**：Nanyang Technological University
    - **Main Content**：This paper proposes ToxicDetector, an efficient method for detecting toxic prompts in LLMs using lightweight grey-box techniques. ***ToxicDetector leverages LLMs to generate prompts containing toxic concepts, and then constructs feature vectors by extracting embedding vectors.*** Finally, a multi-layer perceptron (MLP) classifier is used for classification. The advantages of this method include its ability to handle diverse toxic prompts and its high computational efficiency, making it suitable for real-time applications. Evaluated on multiple Llama models and the Gemma-2 model, ToxicDetector outperformed existing state-of-the-art methods in terms of accuracy (96.39%) and low false positive rate (2.00%), with a processing time of 0.0780 seconds per prompt, demonstrating significant efficiency and scalability. Furthermore, the design of ToxicDetector is effective in addressing toxic prompts disguised through jailbreaking techniques, ensuring the safety and reliability of LLMs in practical applications. ***In the experiments, ToxicDetector was compared against several existing baseline detectors: PlatonicDetector, PerspectiveAPI, OpenAIModerationAPI, WatchYourLanguage, PerplexityFilter, and BD-LLM.***


- 【2024-08】[LeCov: Multi-level Testing Criteria for Large Language Models](https://arxiv.org/pdf/2408.10474)(arXiv:2408, Testing Criteria)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Xuan Xie
    - **Institution**：University of Alberta, Canada
    - **Main Content**：This paper introduces LECOV, a comprehensive multi-level testing framework for Large Language Models (LLMs). ***LECOV defines nine testing criteria spanning attention, neuron, and uncertainty perspectives to evaluate the internal behaviors of LLMs***. 【**In the attention dimension**, the method uses four metrics (KMAC, KVAC, KKAC, KSAC) to measure the distribution of attention values with simple statistics. **In the neuron dimension**, it introduces three metrics (IHNC, ITNC, FHNC) to track key neuron activations over time. **In the uncertainty dimension**, it defines two metrics (KMEC and KMLC) based on output entropy and likelihood to gauge prediction uncertainty. Together, these nine criteria offer a clear, quantitative view of the model’s internal behavior.】 The criteria are applied for test case prioritization and coverage-guided testing, demonstrated on models such as LLaMA2-7B, LLaMA2-13B, and Vicuna over various datasets. Experimental results show that LECOV effectively guides test selection and uncovers defects, thus enhancing LLM reliability and trustworthiness.


- 【2024-06】[Preference Tuning For Toxicity Mitigation Generalizes Across Languages](https://arxiv.org/pdf/2406.16235)(EMNLP'24-findings)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Xiaochen Li
    - **Institution**：Brown University
    - **Main Content**：This paper investigates ***whether preference tuning using English-only data can effectively mitigate toxic outputs from multilingual Large Language Models (LLMs) in other languages***. Contrary to prior findings showing limited cross-lingual transfer in safety tuning, the authors demonstrate that Direct Preference Optimization (DPO) trained ***solely on English data*** significantly reduces toxicity in zero-shot settings across 17 languages, including Chinese, Arabic, and Spanish. Mechanistic interpretability reveals a phenomenon termed dual multilinguality in MLP layers: ***the same key and value vectors in LLMs are responsible for toxic content across multiple languages.*** Preference tuning suppresses these neuron activations without deleting toxic concepts, enabling cross-lingual generalization. Experimental results using mGPT, BLOOM, Llama3, and Aya-23 show toxicity probability reductions from ~50% to under 10%. Additionally, the paper introduces a novel predictive metric for transferability based on bilingual sentence retrieval, finding strong correlation between representational alignment and detoxification efficacy. ***These findings emphasize the effectiveness and efficiency of English-only preference tuning for global LLM safety deployment.***


- 【2024-06】[Supporting Human Raters with the Detection of Harmful Content using Large Language Models](https://arxiv.org/pdf/2406.12800)(arXiv:2406, Toxic Detection)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Kurt Thomas
    - **Institution**：Google
    - **Main Content**：This paper investigates the feasibility of using Large Language Models (LLMs) to assist human raters in detecting harmful content, including hate speech, harassment, violent extremism, and election misinformation. Using a real-world dataset of 50,000 annotated comments from Google’s moderation system, the authors demonstrate that ***LLMs—specifically PaLM 2’s text-unicorn model—can achieve up to 98.7% accuracy when aligned with human decisions***. The study proposes ***five collaborative design patterns*** for integrating LLMs with human rating workflows: (1) pre-filtering non-violative content, (2) rapid escalation of clearly violative content, (3) full automation for certain decisions, (4) validation of human rater decisions, and (5) providing explanatory assistance to raters. In live experiments, LLM assistance ***led to a 41.5% reduction in required human moderation workload*** and ***improved human precision and recall by 9–11%***. The study further explores prompt engineering strategies (zero-shot, few-shot, dynamic selection) and finds that adaptive few-shot prompting yields the best trade-off between accuracy and cost. It concludes that LLMs are a powerful augmentation for content moderation pipelines, improving consistency, efficiency, and potentially reducing the emotional burden on human raters.


- 【2024-05】[Mitigating Text Toxicity with Counterfactual Generation](https://arxiv.org/pdf/2405.09948) (arXiv:2405, Defense)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Milan Bhan
    - **Institution**：Sorbonne University
    - **Main Content**：This paper introduces a novel approach—CF-Detoxtigtec—that applies explainable AI (XAI) techniques to improve toxicity mitigation in text while preserving semantic integrity. The authors observe that conventional neural detoxification models often fail to maintain the original non-toxic intent of the text. To address this, they combine Local Feature Importance (LFI), Counterfactual Generation, and Counterfactual Feature Importance (CFI) to build an interpretable, targeted detoxification pipeline. ***The central contribution is the development of CF-Detoxtigtec, which identifies toxic parts of a sentence using LFI (e.g., SHAP, attention, gradients), and rewrites them through counterfactual editing driven by the TIGTEC model. The method further refines outputs using CFI to optimize content preservation.*** The approach is validated across three benchmark datasets (MAgr, SBF, DynaHate) and compared with leading baselines (MaRCo, CondBERT, ParaGeDi). Experimental results—both automatic and human-annotated—show that CF-Detoxtigtec achieves state-of-the-art content preservation and high semantic plausibility, with competitive toxicity reduction. Importantly, this work is the first to systematically connect XAI and text detoxification, showing their shared methodological structure and evaluation criteria. The authors also discuss ethical risks such as malicious use and value biases, and advocate for human-in-the-loop systems in sensitive moderation contexts. This study opens new pathways for safer, more interpretable, and ethically informed toxicity mitigation.


- 【2024-05】[PolygloToxicityPrompts: Multilingual Evaluation of Neural Toxic Degeneration in Large Language Models](https://arxiv.org/pdf/2405.09373) (COLM'24, Benchmark)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Devansh Jain
    - **Institution**：Carnegie Mellon University
    - **Main Content**：***This paper introduces PolygloToxicityPrompts (PTP), a large-scale multilingual benchmark comprising 425,000 real-world prompts across 17 languages, designed to evaluate neural toxic degeneration in large language models (LLMs)***. Through six targeted research questions, the study reveals systemic disparities in toxicity generation across languages, model sizes, alignment strategies, and input conditions. Key findings show that prompt language significantly influences toxicity, with low-resource languages leading to more harmful outputs. ***Larger models tend to amplify toxicity***, while instruction- and preference-tuning offer only modest mitigation, regardless of the specific alignment method used (e.g., DPO, IPO, PPO). In comparing AI- versus human-generated preference data, human feedback generalizes better to non-English prompts, whereas AI feedback is more effective in its training language. The authors also demonstrate that ***toxicity detection tools (Perspective API) and safety classifiers (Llama Guard)*** provide complementary but non-equivalent assessments, emphasizing the need for hybrid evaluation. Additionally, input toxicity correlates with output degeneration—particularly in unaligned models—indicating the need for robust filtering and safer prompt handling.

### Others

- 【2025-04】[FAIRE: Assessing Racial and Gender Bias in AI-Driven Resume Evaluations](https://arxiv.org/pdf/2504.01420) (arXiv:2504, Racial | Gender Bias)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Athena Wen
    - **Institution**：Algoverse AI Research
    - **Main Content**：This paper introduces FAIRE, _**a benchmark designed to assess racial and gender bias in AI-driven resume evaluation systems powered by Large Language Models (LLMs)**_. The authors employ two evaluation methods—direct scoring and ranking—to examine how AI models evaluate resumes that include different racial or gender cues. The study finds that all models exhibit some form of bias, with significant differences in scoring and ranking based on race and gender. For instance, _**GPT-4o showed a clear bias favoring Asian resumes, while Claude 3.5 Haiku showed more balanced results**_. The study underscores the persistence of bias in AI-based recruitment tools, revealing the need for better bias mitigation strategies to ensure fairness in hiring processes. The benchmark and dataset are open-sourced to help future research in improving AI fairness in recruitment. 





- 【2025-04】[The LLM Wears Prada: Analysing Gender Bias and Stereotypes through Online Shopping Data](https://arxiv.org/pdf/2504.01951) (arXiv:2504, Gender Bias)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Massimiliano Luca
    - **Institution**：University of Trento
    - **Main Content**：This paper proposes a novel empirical framework to examine gender bias and stereotypical reasoning in Large Language Models (LLMs) by leveraging real-world online shopping histories. The authors prompt five state-of-the-art LLMs—including Gemma 3, LLaMA 3, GPT-4o, Claude 3.5, and QwQ 32B—to _**predict a user’s gender based solely on their Amazon purchase records, under both standard and bias-aware prompting conditions.**_ Experimental results show that while LLMs can predict gender with moderate accuracy (F1 scores between 0.66–0.70), their predictions rely heavily on gender-stereotyped product associations (e.g., associating cosmetics with females and electronics with males). Furthermore,_ **instructing models to avoid bias only reduces confidence but fails to eliminate underlying associations**_. The study reveals inconsistencies in model justifications, including misclassification of female-associated items as male, and shows that LLMs align more with male behavioral data than female. These findings highlight the limits of prompt-based bias mitigation and advocate for structural interventions such as dataset diversification and adversarial debiasing to build more equitable and reliable LLM applications.


- 【2025-04】[Leaking LoRa: An Evaluation of Password Leaks and Knowledge Storage in Large Language Models](https://arxiv.org/pdf/2504.00031) (arXiv:2504, Privary)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Ryan Marinelli
    - **Institution**：University of Oslo
    - **Main Content**：This paper investigates the security risks of fine-tuning Large Language Models (LLMs) using LoRA, particularly the memorization and leakage of sensitive information such as passwords. Using Facebook’s OPT-1.3B model fine-tuned on a mix of customer support data and RockYou password lists, the study successfully recovered 37 out of 200 passwords. Through _**causal tracing**_, the authors locate the password information in specific model layers. They then apply _**Rank-One Model Editing (ROME)**_ to purge sensitive memory, reducing the recoverable passwords to zero. The paper highlights a key trade-off: _**while ROME can sanitize sensitive content, it degrades model utility, lowering WikiText benchmark accuracy from 40% to 10%.**_ The authors advocate for context-aware security prioritization in deployment, stressing that security, usability, and functionality cannot be optimized simultaneously in fine-tuned models.


- 【2025-04】[Detecting and Mitigating Bias in LLMs through Knowledge Graph-Augmented Training](https://arxiv.org/pdf/2504.00310) (arXiv:2504, Bias Detecting; Mitigating)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Rajeev Kumar
    - **Institution**：Gen AI Research, Althire AI
    - **Main Content**：This paper proposes a novel framework for detecting and mitigating bias in Large Language Models (LLMs) through Knowledge Graph-Augmented Training (KGAT). By integrating structured, domain-specific knowledge from knowledge graphs into the training of LLMs, the authors demonstrate significant reductions in _**demographic and fairness-related biases**_. The method combines Graph Neural Networks and multi-head attention to align unstructured text with structured semantics, enabling more context-aware and equitable model outputs. Evaluated on public datasets such as Bias in Bios, CelebA, and COMPAS, the approach shows measurable gains in metrics like demographic parity (+15%) and equal opportunity (+10%). This work highlights the dual benefit of KGAT: it enhances fairness while also improving overall model accuracy, offering a scalable and robust solution for ethical AI deployment in high-stakes domains such as healthcare, finance, and law.

- 【2025-03】[BEATS: Bias Evaluation and Assessment Test Suite for Large Language Models](https://arxiv.org/pdf/2503.24310) (arXiv:2503, Bias Evolution)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Alok Abhishek
    - **Institution**：San Francisco, USA
    - **Main Content**：***This paper introduces BEATS, a comprehensive framework for evaluating Bias, Ethics, Fairness, and Factuality (BEFF) in large language models (LLMs)***. The framework includes a benchmark of ***29 metrics*** spanning diverse social dimensions such as race, gender, age, religion, and more, aiming to quantify how LLMs might perpetuate systemic inequities. BEATS assesses LLM outputs using a curated dataset of ***901 bias-probing questions across 12 bias categories.*** The evaluation includes both model-generated responses and ***model-as-a-judge assessments***, using top-tier models (GPT-4o, Claude 3.5, Gemini 1.5). It applies formalized scoring functions to identify explicit/implicit, primary/secondary, and intersectional biases, while measuring fairness, ethical alignment, and factual reliability.


- 【2025-03】[Historical Ink: Exploring Large Language Models for Irony Detection in 19th-Century Spanish](https://arxiv.org/abs/2503.22585)(arXiv:2503, Irony Detection)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Kevin Cohen
    - **Institution**：Universidad de los Andes
    - **Main Content**：This paper investigates ***irony detection in 19th‑century Latin American newspapers*** using large language models. Two strategies are explored: (1) using GPT‑4o to expand texts with richer emotional and contextual cues, and (2) employing a semi‑automated annotation process—complemented by human verification—to augment a historical Spanish dataset. The enhanced data are then used to ***fine‑tune BERT‑based classifiers*** for both multi‑class and binary sentiment tasks. Experimental results reveal that while prompt‑based classification with GPT‑4o alone is insufficient, the BERT‑based pipeline significantly improves the detection of ironic expressions.


- 【2025-03】[FLEX: A Benchmark for Evaluating Robustness of Fairness in Large Language Models](https://arxiv.org/pdf/2503.19540)(NAACL'25-findings，Fairness Benchmark)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Dahyun Jung
    - **Institution**：Korea University
    - **Main Content**：This paper introduces FLEX (Fairness Benchmark in LLM under Extreme Scenarios), a new benchmark designed for the rigorous evaluation of fairness in LLMs. With the rapid development of LLMs, ***the issue of bias*** in models during user interaction has become increasingly apparent, potentially leading to societal impacts and potential harm. ***Existing evaluation benchmarks do not sufficiently reveal the bias vulnerabilities of models under extreme conditions. Therefore, FLEX tests whether models can maintain fairness in harsh environments by subjecting them to adversarial prompts aimed at eliciting bias.*** FLEX assesses the robustness of models through three types of extreme scenarios: Persona Injection, Competing Objectives, and Text Attack, revealing model risks that traditional benchmarks might underestimate. The construction process of the FLEX benchmark involves three steps: first, covering fair samples from existing benchmarks; second, selecting extreme scenarios that best expose model vulnerabilities; and finally, ensuring the diversity of adversarial prompts within the dataset to guarantee comprehensive and accurate evaluation. Experimental results demonstrate that FLEX is more effective than existing benchmarks in evaluating the fairness of LLMs, especially when facing bias-inducing extreme situations. This research emphasizes that while LLMs may appear relatively safe in regular contexts, they remain vulnerable in complex scenarios, necessitating a more rigorous safety evaluation system.


- 【2024-10】[Gender and content bias in Large Language Models: a case study on Google Gemini 2.0 Flash Experimental](https://arxiv.org/pdf/2503.16534)(arXiv:2503，Bias Analysis)
    
    <details>
    
    <summary> Click For Details ! </summary>
    
    - **Author**：Roberto Balestri
    - **Institution**：Università di Bologna, Bologna, Italy
    - **Main Content**：This paper systematically evaluates **gender and in-group bias** in Google's Gemini 2.0 Flash experimental version for content moderation. The study employs standardized prompts, analyzing prompt acceptance rates across two dimensions: gender (neutral, male, female) and content type (sex-related and violence/drug-related). Statistical models, including chi-square tests and logistic regression, were used for comparative analysis, and a cross-sectional comparison was conducted with ChatGPT-4o. The results indicate that while the ***Gemini 2.0 Flash experimental version has achieved some success in reducing bias against females, it has simultaneously become more lenient in moderating violent content***, potentially inadvertently contributing to the spread of harmful information.
