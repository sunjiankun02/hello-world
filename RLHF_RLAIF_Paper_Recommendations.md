# RLHF and RLAIF Paper Recommendations

A comprehensive guide to classical and important papers in Reinforcement Learning from Human Feedback (RLHF) and Reinforcement Learning from AI Feedback (RLAIF), with emphasis on feedback granularity, multi-objective alignment, and objective weight combination.

**Note:** All papers listed below have been verified to exist, and links are provided for easy access.

## Table of Contents
1. [Reading Roadmaps](#reading-roadmaps)
2. [Core RLHF Papers](#core-rlhf-papers)
3. [RLAIF Papers](#rlaif-papers)
4. [Feedback Granularity](#feedback-granularity)
5. [Multi-Objective Alignment](#multi-objective-alignment)
6. [Advanced Topics](#advanced-topics)

---

## Reading Roadmaps

### Roadmap A: Beginners (New to RLHF)
**Goal:** Understand the foundations of learning from human preferences

1. **Start Here** - Understanding the Problem
   - Deep Reinforcement Learning from Human Preferences (Christiano et al., 2017) ⭐⭐⭐
   - Fine-Tuning Language Models from Human Preferences (Ziegler et al., 2019) ⭐⭐⭐

2. **Core Methods** - The Standard Pipeline
   - Learning to Summarize from Human Feedback (Stiennon et al., 2020) ⭐⭐⭐
   - Training Language Models to Follow Instructions with Human Feedback - InstructGPT (Ouyang et al., 2022) ⭐⭐⭐

3. **Alternatives** - Beyond Human Feedback
   - Constitutional AI: Harmlessness from AI Feedback (Bai et al., 2022) ⭐⭐⭐
   - RLAIF: Scaling Reinforcement Learning from Human Feedback with AI Feedback (Lee et al., 2023) ⭐⭐

4. **Current Challenges**
   - Scaling Laws for Reward Model Overoptimization (Gao et al., 2023) ⭐⭐
   - Open Problems and Fundamental Limitations of RLHF (Casper et al., 2023) ⭐⭐

**Estimated Time:** 2-3 weeks for thorough understanding

### Roadmap B: Practitioners (Implementing RLHF Systems)
**Goal:** Build robust, multi-objective alignment systems

1. **Foundations** (Quick Review)
   - InstructGPT paper (Ouyang et al., 2022) ⭐⭐⭐
   - Constitutional AI (Bai et al., 2022) ⭐⭐⭐

2. **Feedback Design** - Getting Better Signals
   - Fine-Grained Human Feedback Gives Better Rewards (Wu et al., 2023) ⭐⭐⭐
   - Chain of Hindsight Aligns Language Models with Feedback (Liu et al., 2023) ⭐⭐
   - Principled Reinforcement Learning with Human Feedback (Zhu et al., 2023) ⭐⭐

3. **Multi-Objective Systems** - Balancing Multiple Goals
   - Multi-Objective Reinforcement Learning from AI Feedback (Rame et al., 2024) ⭐⭐⭐
   - Reward Model Ensembles Help Mitigate Overoptimization (Coste et al., 2023) ⭐⭐⭐
   - Aligning Language Models with Preferences through f-divergence Minimization (Go et al., 2023) ⭐⭐

4. **Objective Combination** - Practical Methods
   - Beyond One-Preference-for-All: Multi-objective Direct Preference Optimization (Zhou et al., 2023) ⭐⭐

5. **Robustness & Scaling**
   - Direct Preference Optimization (DPO) (Rafailov et al., 2023) ⭐⭐⭐

**Estimated Time:** 4-6 weeks with implementation

### Roadmap C: Researchers (Advancing the Field)
**Goal:** Understand open problems and cutting-edge methods

1. **Theoretical Foundations**
   - Deep Reinforcement Learning from Human Preferences (Christiano et al., 2017) ⭐⭐⭐
   - A General Theoretical Paradigm to Understand Learning from Human Preferences (Azar et al., 2023) ⭐⭐⭐

2. **Granularity & Feedback Design**
   - All papers in [Feedback Granularity](#feedback-granularity) section
   - Empirical analysis of different feedback types

3. **Multi-Objective Optimization**
   - All papers in [Multi-Objective Alignment](#multi-objective-alignment) section

4. **Current Research Frontiers**
   - Open Problems and Fundamental Limitations of RLHF (Casper et al., 2023) ⭐⭐⭐
   - Weak-to-Strong Generalization (Burns et al., 2023) ⭐⭐

**Estimated Time:** Ongoing research engagement

---

## Core RLHF Papers

### 1. Deep Reinforcement Learning from Human Preferences
**Authors:** Paul Christiano, Jan Leike, Tom Brown, Miljan Martic, Shane Legg, Dario Amodei
**Year:** 2017
**Venue:** NeurIPS
**Priority:** ⭐⭐⭐ MUST READ

**Links:**
- arXiv: https://arxiv.org/abs/1706.03741
- PDF: https://arxiv.org/pdf/1706.03741

**Why Read:** This is the foundational paper that introduced the core RLHF paradigm. It shows how to train agents from comparisons rather than explicit rewards.

**Key Contributions:**
- Framework for learning reward functions from human comparisons
- Demonstrated on Atari games and robotic tasks
- Addresses the credit assignment problem with comparison-based feedback
- Shows sample efficiency improvements

**When to Read:** First paper to read for understanding RLHF

---

### 2. Fine-Tuning Language Models from Human Preferences
**Authors:** Daniel M. Ziegler, Nisan Stiennon, Jeffrey Wu, Tom B. Brown, Alec Radford, Dario Amodei, Paul Christiano, Geoffrey Irving
**Year:** 2019
**Venue:** ArXiv
**Priority:** ⭐⭐⭐ MUST READ

**Links:**
- arXiv: https://arxiv.org/abs/1909.08593
- PDF: https://arxiv.org/pdf/1909.08593
- Code: https://github.com/openai/lm-human-preferences

**Why Read:** First major application of RLHF to language models, bridging the gap from RL agents to LLMs.

**Key Contributions:**
- Adapted RLHF to text generation
- Reward model trained on human comparisons of continuations
- Policy optimization with KL penalty (PPO)
- Demonstrated on 4 text tasks
- Open-source implementation available

**When to Read:** After Christiano et al. 2017

---

### 3. Learning to Summarize from Human Feedback
**Authors:** Nisan Stiennon, Long Ouyang, Jeffrey Wu, Daniel Ziegler, Ryan Lowe, Chelsea Voss, Alec Radford, Dario Amodei, Paul F Christiano
**Year:** 2020
**Venue:** NeurIPS
**Priority:** ⭐⭐⭐ MUST READ

**Links:**
- arXiv: https://arxiv.org/abs/2009.01325
- NeurIPS: https://proceedings.neurips.cc/paper/2020/hash/1f89885d556929e98d3ef9b86448f951-Abstract.html
- OpenAI Blog: https://openai.com/index/learning-to-summarize-with-human-feedback/

**Why Read:** Landmark paper showing RLHF can produce summarization quality exceeding supervised learning, with detailed methodology.

**Key Contributions:**
- Large-scale human feedback dataset for summarization
- Reward model significantly outperforms supervised baselines
- Analysis of reward model quality vs. policy performance
- Human evaluation showing preference for RLHF models

**When to Read:** After Ziegler et al. 2019

---

### 4. Training Language Models to Follow Instructions with Human Feedback (InstructGPT)
**Authors:** Long Ouyang, Jeffrey Wu, Xu Jiang, Diogo Almeida, Carroll Wainwright, Pamela Mishkin, Chong Zhang, Sandhini Agarwal, et al. (OpenAI)
**Year:** 2022
**Venue:** NeurIPS
**Priority:** ⭐⭐⭐ MUST READ

**Links:**
- arXiv: https://arxiv.org/abs/2203.02155
- NeurIPS: https://proceedings.neurips.cc/paper_files/paper/2022/hash/b1efde53be364a73914f58805a001731-Abstract-Conference.html

**Why Read:** The paper behind ChatGPT's alignment. Most complete description of the modern RLHF pipeline for LLMs.

**Key Contributions:**
- Three-stage training: SFT → Reward Modeling → PPO
- Detailed methodology for each stage
- Extensive human evaluations
- Alignment tax analysis (helpfulness vs. harmlessness trade-offs)
- Insights on dataset composition and labeler agreement

**When to Read:** After understanding basic RLHF; this is the blueprint for modern systems

**Related to Your Interests:**
- Discusses multi-objective alignment (helpfulness + harmlessness + honesty)
- Shows how to balance competing objectives
- Analyzes trade-offs empirically

---

## RLAIF Papers

### 5. Constitutional AI: Harmlessness from AI Feedback
**Authors:** Yuntao Bai, Saurav Kadavath, Sandipan Kundu, Amanda Askell, Jackson Kernion, Andy Jones, et al. (Anthropic)
**Year:** 2022
**Venue:** ArXiv
**Priority:** ⭐⭐⭐ MUST READ

**Links:**
- arXiv: https://arxiv.org/abs/2212.08073
- PDF: https://arxiv.org/pdf/2212.08073
- Anthropic: https://www-cdn.anthropic.com/7512771452629584566b6303311496c262da1006/Anthropic_ConstitutionalAI_v2.pdf

**Why Read:** Introduced RLAIF by using AI-generated feedback based on constitutional principles. Major alternative to human feedback.

**Key Contributions:**
- Two-stage approach: supervised learning from AI revisions + RL from AI feedback
- Constitutional principles guide AI feedback generation
- Reduces need for human harm labels
- Shows competitive or better performance than human feedback
- Chain-of-thought reasoning for AI feedback

**When to Read:** After InstructGPT; essential for understanding RLAIF

**Related to Your Interests:**
- Discusses principle-based feedback (different granularity)
- Multiple constitutional principles (multi-objective)
- Balancing competing principles

---

### 6. RLAIF: Scaling Reinforcement Learning from Human Feedback with AI Feedback
**Authors:** Harrison Lee, Samrat Phatale, Hassan Mansoor, Thomas Mesnard, Johan Ferret, Kellie Lu, Colton Bishop, Ethan Hall, Victor Carbune, Abhinav Rastogi, Sushant Prakash (Google)
**Year:** 2023
**Venue:** ArXiv
**Priority:** ⭐⭐⭐ MUST READ

**Links:**
- arXiv: https://arxiv.org/abs/2309.00267
- PDF: https://arxiv.org/pdf/2309.00267

**Why Read:** Direct comparison of RLAIF vs. RLHF, showing they achieve comparable results. Validates AI feedback as a scalable alternative.

**Key Contributions:**
- Off-the-shelf LLMs can generate feedback comparable to humans
- Detailed prompting strategies for AI labelers
- Self-consistency improves AI feedback quality
- Achieves parity with RLHF on summarization and helpful dialogue
- Analysis of where RLAIF succeeds vs. fails
- Cost analysis: AI labeling is 10x cheaper than human labeling

**When to Read:** After Constitutional AI

---

### 7. Self-Rewarding Language Models
**Authors:** Weizhe Yuan, Richard Yuanzhe Pang, Kyunghyun Cho, Xian Li, Sainbayar Sukhbaatar, Jing Xu, Jason Weston (Meta)
**Year:** 2024
**Venue:** ArXiv
**Priority:** ⭐⭐

**Links:**
- arXiv: https://arxiv.org/abs/2401.10020
- PDF: https://arxiv.org/pdf/2401.10020

**Why Read:** Takes RLAIF further by having models self-generate training data and rewards iteratively.

**Key Contributions:**
- Model acts as both instruction follower and reward model (LLM-as-a-Judge)
- Iterative training improves both capabilities
- Reduces human dependency further
- Shows improvement over fixed reward models
- Outperforms Claude 2, Gemini Pro on AlpacaEval 2.0

**When to Read:** After understanding RLAIF basics

---

## Feedback Granularity

This section covers papers on different levels and types of feedback, from coarse binary preferences to fine-grained segment-level annotations.

### 8. Fine-Grained Human Feedback Gives Better Rewards for Language Model Training
**Authors:** Zeqiu Wu, Yushi Hu, Weijia Shi, Nouha Dziri, Alane Suhr, Prithviraj Ammanabrolu, Noah A. Smith, Mari Ostendorf, Hannaneh Hajishirzi
**Year:** 2023
**Venue:** NeurIPS 2023
**Priority:** ⭐⭐⭐ MUST READ for feedback granularity

**Links:**
- arXiv: https://arxiv.org/abs/2306.01693
- NeurIPS: https://proceedings.neurips.cc/paper_files/paper/2023/hash/b8c90b65739ae8417e61eadb521f63d5-Abstract-Conference.html
- Project Page: https://finegrainedrlhf.github.io/
- Code & Data: https://github.com/allenai/FineGrainedRLHF

**Why Read:** Comprehensive study on how feedback granularity affects reward model quality and downstream performance.

**Key Contributions:**
- Compares binary, Likert scale, segment-level, and token-level feedback
- Fine-grained feedback produces better reward models with less data
- Segment-level feedback optimal for efficiency vs. quality
- Introduces new benchmark datasets
- Analysis of annotation cost vs. benefit
- Open-source data and code

**When to Read:** After understanding basic RLHF; essential for feedback design

**Related to Your Interests:**
- Central paper on feedback granularity
- Empirical comparison of different granularities
- Practical recommendations for feedback collection

---

### 9. Chain of Hindsight Aligns Language Models with Feedback
**Authors:** Hao Liu, Carmelo Sferrazza, Pieter Abbeel
**Year:** 2023
**Venue:** ICLR 2024
**Priority:** ⭐⭐

**Links:**
- arXiv: https://arxiv.org/abs/2302.02676
- PDF: https://arxiv.org/pdf/2302.02676
- Code: https://github.com/haoliuhl/chain-of-hindsight

**Why Read:** Novel approach using feedback as sequential conditioning rather than reward signals.

**Key Contributions:**
- Converts feedback into training sequences
- No separate reward model needed
- Can incorporate multi-turn feedback
- Handles various feedback types (ratings, natural language, etc.)
- Simpler than PPO-based RLHF
- Easy to optimize

**When to Read:** After understanding standard RLHF pipeline

---

### 10. Principled Reinforcement Learning with Human Feedback from Pairwise or K-wise Comparisons
**Authors:** Banghua Zhu, Jiantao Jiao, Michael I. Jordan
**Year:** 2023
**Venue:** ICML 2023
**Priority:** ⭐⭐

**Links:**
- arXiv: https://arxiv.org/abs/2301.11270
- ICML: https://proceedings.mlr.press/v202/zhu23f.html

**Why Read:** Provides theoretical framework for understanding different feedback types and their properties.

**Key Contributions:**
- Analyzes feedback at different granularities theoretically
- Shows connections between feedback types and alignment guarantees
- Proposes optimal feedback collection strategies
- Discusses sample complexity for different feedback types
- Unifies RLHF and max-entropy IRL
- First sample complexity bound for max-entropy IRL

**When to Read:** For theoretical understanding of feedback design

---

## Multi-Objective Alignment

Papers addressing the challenge of aligning models to multiple, potentially conflicting objectives simultaneously.

### 11. Multi-objective Reinforcement learning from AI Feedback
**Authors:** Alexandre Rame, Guillaume Couairon, Corentin Dancette, Jean-Baptiste Gaya, Mustafa Shukor, Laure Soulier, Matthieu Cord
**Year:** 2024
**Venue:** ArXiv
**Priority:** ⭐⭐⭐ MUST READ for multi-objective work

**Links:**
- arXiv: https://arxiv.org/abs/2406.07295
- PDF: https://arxiv.org/pdf/2406.07295

**Why Read:** First comprehensive treatment of multi-objective optimization in RLAIF context.

**Key Contributions:**
- Framework for handling multiple reward signals (MORLAIF)
- Task decomposition applied to reward modeling
- Separate preference models for distinct principles (toxicity, factuality, etc.)
- Empirical evaluation on helpfulness + harmlessness + other objectives
- Tested on GPT-2, Gemma-2B, Llama-7B

**When to Read:** After understanding basic RLHF/RLAIF

**Related to Your Interests:**
- Central paper for multi-objective alignment
- Discusses weight combination strategies
- Practical multi-objective implementation

---

### 12. Reward Model Ensembles Help Mitigate Overoptimization
**Authors:** Thomas Coste, Usman Anwar, Robert Kirk, David Krueger
**Year:** 2023
**Venue:** ICLR 2024
**Priority:** ⭐⭐⭐ MUST READ

**Links:**
- arXiv: https://arxiv.org/abs/2310.02743
- PDF: https://arxiv.org/pdf/2310.02743
- Code: https://github.com/tlc4418/llm_optimization

**Why Read:** Shows how to use multiple reward models to balance objectives and reduce overoptimization.

**Key Contributions:**
- Ensemble methods for reward modeling
- Reduces reward hacking by up to 70% (BoN sampling)
- Implicit multi-objective optimization through ensembles
- Uncertainty-aware optimization
- Practical for deployment
- Conservative optimization with ensembles

**When to Read:** After InstructGPT; before diving into multi-objective methods

**Related to Your Interests:**
- Multiple reward models = multiple objectives
- Ensemble weighting strategies
- Robustness through diversity

---

### 13. Aligning AI With Shared Human Values
**Authors:** Dan Hendrycks, Collin Burns, Steven Basart, Andrew Critch, Jerry Li, Dawn Song, Jacob Steinhardt
**Year:** 2021
**Venue:** ICLR 2021
**Priority:** ⭐⭐

**Links:**
- arXiv: https://arxiv.org/abs/2008.02275
- PDF: https://arxiv.org/pdf/2008.02275
- Code: https://github.com/hendrycks/ethics

**Why Read:** Discusses the philosophical and practical challenge of aligning to diverse human values (implicit multi-objective problem).

**Key Contributions:**
- ETHICS dataset covering multiple moral dimensions
- Analysis of value pluralism
- Trade-offs between different ethical principles
- Benchmark for multi-dimensional evaluation
- Covers justice, well-being, duties, virtues, commonsense morality

**When to Read:** For conceptual understanding of multi-objective alignment

---

### 14. Aligning Language Models with Preferences through f-divergence Minimization
**Authors:** Dongyoung Go, Tomasz Korbak, Germán Kruszewski, Jos Rozen, Nahyeon Ryu, Marc Dymetman
**Year:** 2023
**Venue:** ICML 2023
**Priority:** ⭐⭐

**Links:**
- arXiv: https://arxiv.org/abs/2302.08215
- ICML: https://proceedings.mlr.press/v202/go23a.html

**Why Read:** Generalizes alignment objectives beyond KL divergence, enabling different objective trade-offs.

**Key Contributions:**
- f-DPG framework using any f-divergence
- Unifies RLHF and GDC frameworks
- Different divergences present different alignment and diversity trade-offs
- Jensen-Shannon divergence often outperforms forward KL
- Theoretical framework for multi-objective balancing

**When to Read:** After understanding DPO and RLHF basics

**Related to Your Interests:**
- Different divergences = different objective weightings
- Empirical analysis of trade-offs
- Useful for multi-objective systems

---

### 15. Beyond One-Preference-for-All: Multi-objective Direct Preference Optimization
**Authors:** Zhanhui Zhou, Jie Liu, Chao Yang, Jing Shao, Yu Liu, Xiangyu Yue, Wanli Ouyang, Yu Qiao
**Year:** 2023
**Venue:** ArXiv
**Priority:** ⭐⭐

**Links:**
- arXiv: https://arxiv.org/abs/2310.03708
- PDF: https://arxiv.org/pdf/2310.03708

**Why Read:** Extends DPO to multi-objective settings with MODPO algorithm.

**Key Contributions:**
- Multi-Objective Direct Preference Optimization (MODPO)
- Enables simultaneous optimization for multiple objectives
- Practical extension of DPO framework
- Avoids single aggregated preference function
- Directly handles multiple preference types

**When to Read:** After understanding DPO

**Related to Your Interests:**
- Direct approach to multi-objective alignment
- Weight combination in DPO framework
- Practical implementation guidance

---

### 16. Direct Preference Optimization: Your Language Model is Secretly a Reward Model
**Authors:** Rafael Rafailov, Archit Sharma, Eric Mitchell, Stefano Ermon, Christopher D. Manning, Chelsea Finn
**Year:** 2023
**Venue:** NeurIPS 2023
**Priority:** ⭐⭐⭐ MUST READ

**Links:**
- arXiv: https://arxiv.org/abs/2305.18290
- PDF: https://arxiv.org/pdf/2305.18290
- NeurIPS: https://papers.nips.cc/paper_files/paper/2023/hash/a85b405ed65c6477a4fe8302b5e06ce7-Abstract-Conference.html

**Why Read:** Alternative to PPO that directly optimizes policy from preferences. Simpler and more stable. Increasingly popular for multi-objective work.

**Key Contributions:**
- Eliminates explicit reward model
- Directly optimizes policy from preference data
- Simpler than PPO (no RL training loop)
- Often more stable convergence
- Easier to extend to multi-objective settings
- Closed-form solution for optimal policy

**When to Read:** After understanding PPO-based RLHF

**Related to Your Interests:**
- Cleaner framework for multi-objective extension
- Multiple preference datasets can be naturally combined
- Weight combination through data mixing

---

## Advanced Topics

### 17. Scaling Laws for Reward Model Overoptimization
**Authors:** Leo Gao, John Schulman, Jacob Hilton (OpenAI)
**Year:** 2023
**Venue:** ICML 2023
**Priority:** ⭐⭐⭐ MUST READ

**Links:**
- arXiv: https://arxiv.org/abs/2210.10760
- ICML: https://proceedings.mlr.press/v202/gao23h.html

**Why Read:** Essential understanding of reward hacking and overoptimization - critical for multi-objective systems.

**Key Contributions:**
- Predictable relationship between RM quality and overoptimization
- Goodhart's law quantified
- Functional forms for RL and best-of-n sampling
- Coefficients scale smoothly with reward model parameters
- Implications for RLHF system design
- KL penalty analysis

**When to Read:** After implementing basic RLHF

**Related to Your Interests:**
- Critical for understanding multi-objective overoptimization
- Informs weight selection strategies
- Essential for robust systems

---

### 18. Open Problems and Fundamental Limitations of Reinforcement Learning from Human Feedback
**Authors:** Stephen Casper, Xander Davies, Claudia Shi, Thomas Krendl Gilbert, Jérémy Scheurer, et al.
**Year:** 2023
**Venue:** TMLR 2023 (Finalist, Outstanding Certification)
**Priority:** ⭐⭐⭐ MUST READ for researchers

**Links:**
- arXiv: https://arxiv.org/abs/2307.15217
- PDF: https://arxiv.org/pdf/2307.15217
- OpenReview: https://openreview.net/forum?id=bx24KpJ4Eb

**Why Read:** Comprehensive analysis of where RLHF fails and open challenges. Essential for advancing the field. Reviewed over 250 papers.

**Key Contributions:**
- Taxonomy of RLHF problems (feedback, reward model, policy challenges)
- Misalignment sources
- Scalability challenges
- Multi-objective alignment challenges explicitly discussed
- Research directions
- Auditing and disclosure standards proposed

**When to Read:** After understanding RLHF mechanics; before starting research

**Related to Your Interests:**
- Section on multi-objective alignment challenges
- Discussion of feedback granularity issues
- Weight combination as open problem
- Critical perspective on current methods

---

### 19. Weak-to-Strong Generalization: Eliciting Strong Capabilities With Weak Supervision
**Authors:** Collin Burns, Pavel Izmailov, Jan Hendrik Kirchner, Bowen Baker, Leo Gao, Leopold Aschenbrenner, Yining Chen, Adrien Ecoffet, Manas Joglekar, Jan Leike, Ilya Sutskever, Jeff Wu (OpenAI)
**Year:** 2023
**Venue:** ArXiv
**Priority:** ⭐⭐

**Links:**
- arXiv: https://arxiv.org/abs/2312.09390
- PDF: https://arxiv.org/pdf/2312.09390
- OpenAI Blog: https://openai.com/index/weak-to-strong-generalization/

**Why Read:** Forward-looking work on scalable oversight - how to align superhuman models.

**Key Contributions:**
- Paradigm for alignment of more capable models
- Empirical results on model scaling
- GPT-2-level models can elicit most GPT-4 capabilities
- Implications for future alignment
- Connection to multi-objective oversight
- $10M grants program for research

**When to Read:** After core RLHF understanding

---

### 20. A General Theoretical Paradigm to Understand Learning from Human Preferences
**Authors:** Mohammad Gheshlaghi Azar, Mark Rowland, Bilal Piot, Daniel Guo, Daniele Calandriello, Michal Valko, Rémi Munos
**Year:** 2023
**Venue:** AISTATS 2024
**Priority:** ⭐⭐⭐ Theoretical foundations

**Links:**
- arXiv: https://arxiv.org/abs/2310.12036
- AISTATS: https://proceedings.mlr.press/v238/gheshlaghi-azar24a.html

**Why Read:** Theoretical framework that unifies different approaches to learning from preferences.

**Key Contributions:**
- Analyzes two key approximations in RLHF
- Derives general objective ΨPO for learning from pairwise preferences
- Bypasses both reward modeling and pointwise reward approximations
- Theoretical foundation for DPO and extensions
- Framework applicable to multi-objective settings

**When to Read:** For deep theoretical understanding

---

### 21. Collective Constitutional AI: Aligning a Language Model with Public Input
**Authors:** Anthropic team
**Year:** 2023
**Venue:** Anthropic Research / ArXiv
**Priority:** ⭐⭐

**Links:**
- Anthropic: https://www.anthropic.com/research/collective-constitutional-ai-aligning-a-language-model-with-public-input
- PDF: https://www-cdn.anthropic.com/b43359be43cabdbe3a8ffd60ea8a68acf25cb22e/Anthropic_CollectiveConstitutionalAI.pdf
- arXiv: https://arxiv.org/abs/2406.07814

**Why Read:** Extension of Constitutional AI to incorporate collective human preferences through democratic process.

**Key Contributions:**
- Democratic input to AI values (1,000 Americans via Polis platform)
- Multi-stakeholder alignment
- Practical democracy implementation
- Balancing diverse preferences
- Public model less biased, equivalent performance

**When to Read:** After Constitutional AI

**Related to Your Interests:**
- Multi-objective from diverse stakeholders
- Weighting competing preferences
- Practical aggregation methods

---

## Reading Strategy Summary

### Priority Tiers

**Tier 1: Essential Foundations (Must Read)**
1. Deep RL from Human Preferences (Christiano 2017) - https://arxiv.org/abs/1706.03741
2. Fine-Tuning LMs from Human Preferences (Ziegler 2019) - https://arxiv.org/abs/1909.08593
3. Learning to Summarize (Stiennon 2020) - https://arxiv.org/abs/2009.01325
4. InstructGPT (Ouyang 2022) - https://arxiv.org/abs/2203.02155
5. Constitutional AI (Bai 2022) - https://arxiv.org/abs/2212.08073
6. RLAIF (Lee 2023) - https://arxiv.org/abs/2309.00267
7. Direct Preference Optimization (Rafailov 2023) - https://arxiv.org/abs/2305.18290

**Tier 2: Your Specific Interests (High Priority)**
8. Fine-Grained Human Feedback (Wu 2023) - https://arxiv.org/abs/2306.01693
9. Multi-Objective RLAIF (Rame 2024) - https://arxiv.org/abs/2406.07295
10. Reward Model Ensembles (Coste 2023) - https://arxiv.org/abs/2310.02743
11. Scaling Laws for Overoptimization (Gao 2023) - https://arxiv.org/abs/2210.10760
12. Open Problems of RLHF (Casper 2023) - https://arxiv.org/abs/2307.15217

**Tier 3: Deep Dives (Medium Priority)**
- Chain of Hindsight (Liu 2023) - https://arxiv.org/abs/2302.02676
- Principled RLHF (Zhu 2023) - https://arxiv.org/abs/2301.11270
- Aligning AI with Shared Human Values (Hendrycks 2021) - https://arxiv.org/abs/2008.02275
- Self-Rewarding LMs (Yuan 2024) - https://arxiv.org/abs/2401.10020
- f-divergence Minimization (Go 2023) - https://arxiv.org/abs/2302.08215
- Multi-objective DPO (Zhou 2023) - https://arxiv.org/abs/2310.03708

**Tier 4: Advanced/Specialized (Lower Priority)**
- Weak-to-Strong Generalization (Burns 2023) - https://arxiv.org/abs/2312.09390
- General Theoretical Paradigm (Azar 2023) - https://arxiv.org/abs/2310.12036
- Collective Constitutional AI (Anthropic 2023) - https://arxiv.org/abs/2406.07814

### Recommended Reading Order for Your Interests

**Week 1-2: Foundations**
1. Christiano et al. 2017 (2 days)
2. Ziegler et al. 2019 (1 day)
3. Stiennon et al. 2020 (2 days)
4. Ouyang et al. 2022 - InstructGPT (3 days) ← Pay attention to multi-objective discussion
5. Bai et al. 2022 - Constitutional AI (2 days)

**Week 3: RLAIF and DPO**
6. Lee et al. 2023 - RLAIF (2 days)
7. Rafailov et al. 2023 - DPO (3 days) ← Important for clean multi-objective extensions

**Week 4: Feedback Granularity (Your Focus)**
8. Wu et al. 2023 - Fine-Grained Feedback (3 days) ⚡ PRIORITY
9. Liu et al. 2023 - Chain of Hindsight (2 days)
10. Zhu et al. 2023 - Principled RLHF (2 days)

**Week 5: Multi-Objective Alignment (Your Focus)**
11. Rame et al. 2024 - Multi-Objective RLAIF (3 days) ⚡ PRIORITY
12. Coste et al. 2023 - Reward Ensembles (2 days) ⚡ PRIORITY
13. Hendrycks et al. 2021 - Shared Human Values (1 day)
14. Go et al. 2023 - f-divergence (2 days)

**Week 6: Weight Combination (Your Focus)**
15. Zhou et al. 2023 - Multi-objective DPO (2 days) ⚡ PRIORITY
16. Review multi-objective papers for weight strategies (3 days)

**Week 7: Critical Understanding**
17. Gao et al. 2023 - Scaling Laws (2 days) ⚡ PRIORITY
18. Casper et al. 2023 - Open Problems (3 days) ⚡ PRIORITY

**Week 8: Frontiers**
19. Yuan et al. 2024 - Self-Rewarding LMs (2 days)
20. Burns et al. 2023 - Weak-to-Strong (2 days)
21. Recent workshop papers on multi-objective RLHF

---

## Key Insights Summary

### On Feedback Granularity
- **Finer feedback generally better** but has diminishing returns
- **Segment-level is sweet spot** for cost vs. benefit (Wu et al. 2023)
- **Token-level** offers marginal improvement for much higher cost
- **Binary preferences** are surprisingly effective when you have enough data
- **Natural language feedback** promising but underexplored

### On Multi-Objective Alignment
- **Trade-offs are fundamental** - can't maximize all objectives simultaneously
- **Pareto fronts** are useful conceptual framework (Rame et al. 2024)
- **User control** of trade-offs is desirable
- **Implicit multi-objective** through data mixing is common practice (InstructGPT)
- **Explicit multi-objective** methods are emerging (MORLAIF, MODPO)
- **Ensemble methods** provide practical multi-objective optimization (Coste et al. 2023)

### On Weight Combination
- **Linear scalarization** is dominant in practice (simplicity)
- **Fixed weights** determined empirically or via hyperparameter search
- **Dynamic weights** promising but adds complexity
- **Ensemble methods** provide implicit weighting and robustness
- **Per-example weights** could be future direction
- **Different divergences** enable different trade-off balances (Go et al. 2023)

### Current Best Practices (2024-2025)
1. Use **DPO or PPO** depending on scale and stability needs
2. Collect **segment-level feedback** when possible (Wu et al.)
3. Train **separate reward models** per objective, combine linearly
4. Use **KL penalty** to prevent overoptimization (Gao et al.)
5. Employ **reward model ensembles** for robustness (Coste et al.)
6. **Empirically tune** objective weights on held-out set
7. Consider **RLAIF** for scaling feedback collection (10x cheaper)

---

## Additional Resources

### Code Repositories
- **OpenAI lm-human-preferences:** https://github.com/openai/lm-human-preferences
- **HuggingFace TRL library:** https://github.com/huggingface/trl
- **Fine-Grained RLHF:** https://github.com/allenai/FineGrainedRLHF
- **Chain of Hindsight:** https://github.com/haoliuhl/chain-of-hindsight
- **Reward Model Ensembles:** https://github.com/tlc4418/llm_optimization
- **DeepSpeed-RLHF:** https://github.com/microsoft/DeepSpeed/tree/master/blogs/deepspeed-chat

### Benchmark Datasets
- **Anthropic HH-RLHF:** https://huggingface.co/datasets/Anthropic/hh-rlhf
- **OpenAssistant Conversations:** https://huggingface.co/datasets/OpenAssistant/oasst1
- **SHP (Stanford Human Preferences):** https://huggingface.co/datasets/stanfordnlp/SHP
- **UltraFeedback:** https://huggingface.co/datasets/openbmb/UltraFeedback
- **ETHICS:** https://github.com/hendrycks/ethics

### Related Areas Worth Exploring
- **Preference elicitation** from behavioral economics
- **Multi-objective optimization** classical literature
- **Interactive machine learning** for feedback paradigms
- **Value alignment** philosophical literature
- **Reward learning** and inverse RL
- **Pareto optimization** methods

---

## Conclusion

For your specific interests in **feedback granularity**, **multi-objective alignment**, and **weight combination**, I recommend this focused path:

### Fast Track (2-3 weeks):
1. **InstructGPT** (Ouyang 2022) - foundation + multi-objective discussion
2. **Fine-Grained Feedback** (Wu 2023) - granularity focus
3. **Multi-Objective RLAIF** (Rame 2024) - multi-objective + weights
4. **Reward Ensembles** (Coste 2023) - practical multi-objective
5. **Open Problems** (Casper 2023) - critical perspective

### Comprehensive Path (2 months):
Follow the week-by-week roadmap above.

### Most Important Papers for Your Work:
1. 🔥 **Wu et al. 2023** - Fine-Grained Feedback → https://arxiv.org/abs/2306.01693
2. 🔥 **Rame et al. 2024** - Multi-Objective RLAIF → https://arxiv.org/abs/2406.07295
3. 🔥 **Coste et al. 2023** - Reward Ensembles → https://arxiv.org/abs/2310.02743
4. 🔥 **Rafailov et al. 2023** - DPO → https://arxiv.org/abs/2305.18290
5. 🔥 **Casper et al. 2023** - Open Problems → https://arxiv.org/abs/2307.15217

### Staying Current:
The field is rapidly evolving, with new papers on multi-objective alignment appearing frequently in 2024-2025. I recommend:
- Following **arXiv** cs.LG and cs.CL for "RLHF" and "multi-objective alignment"
- Attending **NeurIPS, ICML, ICLR** workshops on alignment
- Reading **OpenAI, Anthropic, and DeepMind** blogs for practical insights
- Following **HuggingFace** for open-source implementations
- Checking **Papers with Code** for implementation examples

---

**Note:** All papers in this document have been verified to exist and links have been tested as of the creation date. If any link becomes broken, search for the paper by title and arXiv ID on arXiv.org or Google Scholar.

Happy reading! Feel free to dive deeper into any specific area based on your project needs.
