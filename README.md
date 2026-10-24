# Awesome Data Selection for LLM Alignment  

[![PR Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen)](https://github.com/yimutianyang/Awesome-Data-Selection-for-LLM-Alignment)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)  
---

## 📚 Paper Taxonomy  

### 1. 🔍 Data Quality Filtering  
| Title | Method | Dataset | Key Findings | Resources |  
|-------|--------|---------|--------------|-----------|  
| [Entropy Law: The Story Behind Data Compression and LLM Performance](https://arxiv.org/pdf/2407.06645) | Data compression rate (entropy) as quality proxy | C4, Pile | High-compression data boosts performance (+12%) | [PDF](https://arxiv.org/pdf/2407.06645) [Code](https://github.com/USTC-StarTeam/ZIP)|  
| [Less is More: Improving LLM Alignment via Preference Data Selection](https://arxiv.org/abs/2502.14560) | Reward model confidence filtering | Anthropic HH | 30% high-quality data achieves full-data performance | [PDF](https://arxiv.org/abs/2502.14560)|  
| [Principled Data Selection: The Hidden Risks of Difficult Examples](https://arxiv.org/abs/2502.09650) | Hard example distribution shift analysis | Reddit, StackExchange | Hard examples may harm OOD generalization | [PDF](https://arxiv.org/abs/2502.09650) [Code](https://github.com/glorgao/SelectiveDPO)|  
| [Larger or Smaller Reward Margins to Select Preferences for Alignment?](https://arxiv.org/abs/2503.01864)| Compute the gap between explicit reward and implicit reward | AlpacaEval 2, Arena-Hard | Align potential is important | [PDF](https://arxiv.org/pdf/2503.01864) [Code](https://github.com/Hesse73/Alignment-Potential-Metric)|  

### 2. 🌈 Data Diversity Optimization  
| Title | Method | Dataset | Key Findings | Resources |  
|-------|--------|---------|--------------|-----------|  
| [Harnessing Diversity for Important Data Selection](https://openreview.net/forum?id=bMC1t7eLRc) | Embedding similarity-based sampling | Slimpajama | Improves cross-domain generalization (+8%) | [PDF](https://openreview.net/forum?id=bMC1t7eLRc)|  
| [Adapt-∞: Dynamic Data Selection for Continual Learning](https://arxiv.org/pdf/2410.10636) | Dynamic selection in continual learning | COCO, LAION | Reduces catastrophic forgetting (↓15%) | [PDF](https://arxiv.org/pdf/2410.10636) [Code](https://github.com/adymaharana/adapt-inf) |  

### 3. ⚖️ Alignment-Specific Selection  
| Title | Method | Dataset | Key Findings | Resources |  
|-------|--------|---------|--------------|-----------|  
| [SEAL: Safety-enhanced Aligned LLM Fine-tuning](https://openreview.net/forum?id=VHguhvcoM5) | Toxicity scoring + safe data augmentation | ToxiGen | Reduces harmful outputs by 35% | [PDF](https://openreview.net/forum?id=VHguhvcoM5) [Code](https://github.com/hanshen95/SEAL) |  
| [InCo-DPO: Balancing Distribution Shift and Data Quality](https://arxiv.org/abs/2503.15880) | Distributionally robust preference selection | UltraFeedback | Improves OOD robustness (+7%) | [PDF](https://arxiv.org/abs/2503.15880) |  

### 4. ⚡ Efficiency-Driven Methods  
| Title | Method | Dataset | Key Findings | Resources |  
|-------|--------|---------|--------------|-----------|  
| [EDGE: Efficient Data Selection via Guideline Effectiveness](https://arxiv.org/abs/2502.12494) | Rule-based efficient filtering | Safe RLHF | 50% less data with 90% performance retained | [PDF](https://arxiv.org/abs/2502.12494) |  
| [Dataset Decomposition: Variable-Length Curriculum Learning](https://arxiv.org/abs/2405.13226) | Sequence-length curriculum | C4 | 2x faster training | [Paper](https://arxiv.org/abs/2405.13226) [Code](https://github.com/apple/ml-dataset-decomposition) |  

### 5. 📐 Theoretical Insights  
| Title | Key Contribution | Resources |  
|-------|------------------|-----------|  
| [What Makes Good Data for Alignment?](https://openreview.net/forum?id=BTKAeLqLMw) | Defines "Informativeness-Diversity-Safety" triad | [PDF](https://openreview.net/forum?id=BTKAeLqLMw) [Code](https://github.com/hkust-nlp/deita)|  
| [Rethinking Data Shapley for Data Selection](https://proceedings.mlr.press/v235/wang24cg.html) | Improved Shapley value computation | [PDF](https://proceedings.mlr.press/v235/wang24cg.html) |  

---

### 6. 🧹 Data Filter  
#### 6.1 📊 **Metric Innovation**  
| Title | Method | Dataset | Key Findings | Resources |  
|-------|--------|---------|--------------|-----------|    
| [GE-EDGE: Gradient Estimation for Effective Data Filtering](https://arxiv.org/pdf/2502.12494) | Gradient-based importance scoring | C4, BooksCorpus | Identifies high-impact samples via gradients | [PDF](https://arxiv.org/pdf/2502.12494) |  
| [WHAT MAKES GOOD DATA FOR ALIGNMENTA COMPREHENSIVE STUDY OF AUTOMATIC DATA SELECTION IN INSTRUCTION TUNING](https://arxiv.org/pdf/2312.15685) | Joint optimization of three metrics | Reddit, WikiText | Balances utility and diversity | [PDF](https://arxiv.org/pdf/2312.15685) [Code](https://github.com/hkust-nlp/deita) |  

#### 6.2 🛠️ **Method Innovation**  
| Title | Method | Dataset | Key Findings | Resources |  
|-------|--------|---------|--------------|-----------|
| [OI-Theory: Get More for Less](https://arxiv.org/pdf/2405.02774) | Influence function augmentation | Slimpajama | 20% data expansion with guarantees | [PDF](https://arxiv.org/pdf/2405.02774) [Code](https://anonymous.4open.science/r/DV4LLM-D761/) |   
| [Take the Essence and Discard the Dross](https://openreview.net/forum?id=erqoeO6lFu) | Feature extraction & criterion design | Multi-Domain Text | Filters 40% redundant data | [PDF](https://openreview.net/pdf?id=erqoeO6lFu) |  
| [Harnessing Diversity for Important Data Selection](https://openreview.net/forum?id=bMC1t7eLRc) | Embedding similarity sampling | Slimpajama | Enhances cross-domain generalization | [PDF](https://openreview.net/forum?id=bMC1t7eLRc) |  
| [Adapt-∞: Dynamic Data Selection for Continual Learning](https://arxiv.org/pdf/2410.10636) | Dynamic task-specific selection | COCO, LAION | Mitigates catastrophic forgetting | [PDF](https://arxiv.org/pdf/2410.10636) [Code](https://github.com/adymaharana/adapt-inf) |
| [Entropy Law: The Story Behind Data Compression and LLM Performance](https://arxiv.org/pdf/2407.06645) | Entropy-based compression rate | C4, Pile | High-entropy data correlates with model performance | [PDF](https://arxiv.org/pdf/2407.06645) |  

### 7. 🚀 Data Enhance  
| Title | Method | Dataset | Key Findings | Resources |  
|-------|--------|---------|--------------|-----------|  
| [Reward-Augmented Data Enhances Direct Preference](https://openreview.net/forum?id=bpSD3IOgyS) | Reward-guided synthetic generation | Anthropic HH, UltraFeedback | +14% alignment improvement | [PDF](https://arxiv.org/pdf/2410.08067) [Code](https://github.com/shenao-zhang/reward-augmented-preference) |  
| [Chunks as Arms: Multi-Armed Bandit-Guided Sampling for Long-Context LLM Preference Optimization](https://arxiv.org/abs/2508.13993) | Multi-armed bandit chunk sampling to generate high-quality, diverse DPO pairs | LongBench, InfiniteBench | >4% gain on long-context reasoning (Llama, Qwen) | [PDF](https://arxiv.org/pdf/2508.13993) [Code](https://github.com/NEUIR/LongMab-PO) |  
 


---  
*持续更新中，欢迎贡献！*  
