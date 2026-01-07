
# A Survey of User Lifelong Behavior Modeling: Perspectives on Efficiency and Effectiveness

## Overview
This is the official repository of the paper "A Survey of User Lifelong Behavior Modeling: Perspectives on Efficiency and Effectiveness"

This survey provides an in-depth examination of existing User Lifelong Behavior Modeling (ULBM) methods from an industrial perspective, with a particular focus on their performance under the efficiency–effectiveness balance, aiming to sustain a stable return on investment (ROI) as user lifelong behavior sequences continue to grow.

We will continue to track and summarize emerging ULBM research, with particular attention to approaches that have been validated in real-world industrial settings, in order to facilitate the continued advancement of this field.

## Table of Contents
- [Introduction](#introduction)
- [Survey Scope](#survey-scope)
- [Efficiency-Effectiveness Balance](#efficiency-effectiveness-balance)
  - [Efficiency Optimizations](#efficiency-optimizations)
    - [Algorithmic](#algorithmic)
    - [Infrastructure](#infrastructure)
  - [Effectiveness Optimizations](#effectiveness-optimizations)
- [Papers](#papers)
- [Datasets](#datasets)
- [Acknowledgement](#acknowledgement)
- [How to Contribute](#how-to-contribute)

## Introduction
User Lifelong Behavior Modeling (ULBM) aims to capture users’ long-term and continuously evolving preferences by leveraging their lifelong interaction histories. Owing to its defining characteristics, including ultra-long behavior sequences and heterogeneous user actions, deploying ULBM in industrial recommender systems poses substantial challenges in balancing efficiency and effectiveness, which is critical for sustaining a stable return on investment (ROI) as user behavior sequences continue to grow.

This survey examines ULBM approaches from two complementary perspectives: efficiency-aware designs, which emphasize algorithmic and engineering optimizations to improve scalability, and effectiveness-oriented modeling strategies, which focus on enhancing representation capacity through expressive interaction modeling, fine-grained interest mining, and the incorporation of external knowledge. In addition, we summarize representative datasets for ULBM evaluation to provide practical guidance and support future research.

Through this survey, we aim to provide researchers and practitioners with a comprehensive set of insights and practical references, and to stimulate further exploration of scalable and effective ULBM solutions under real-world constraints.

The shift of the ROI equilibrium point in industrial scenarios

![ROI](fig/ROI.png)


## Survey Scope
This survey covers a wide range of topics relevant to ULBM, including:
- Ultra-long sequence modeling.
- Heterogeneous behavior modeling.
- Industrial deployment under the efficiency–effectiveness balance (EEB).

## Efficiency-Effectiveness Balance

### Efficiency Optimizations

#### Algorithmic

ULBM commonly adopts a two-stage paradigm of *preprocess first, encode later* to reduce the scale of user behavior sequences and achieve a balance between efficiency and effectiveness. This paradigm can be further categorized into search-based methods and compression-based methods. In this context, the *General Search Unit* (GSU) and the *Interest Reduction Unit* (IRU) serve as key components for improving efficiency.

Trend chart of existing ULBM work on algorithmic optimizations:

![ALO](fig/alo.png)

#### Infrastructure
Industrial-scale ULBM faces strict latency and throughput requirements due to ultra-long sequences, persistent user states, and frequent online inference. Infrastructure optimizations aim to increase throughput, reduce GPU memory and storage, and shorten response time. These optimizations can be categorized into three main types: *custom kernels*, *precision optimization*, and *multi-level caching*.

The infrastructure optimizations of ULBM can be organized along three dimensions:

![INFRA](fig/infra.png)

### Effectiveness Optimizations
Effectiveness in ULBM refers to improving the quality of user representations by addressing key limitations: summarizing long-term interactions may lose critical dependencies, overlapping behaviors introduce noise, and relying solely on observed actions limits semantic understanding.  
To tackle these challenges, effectiveness optimizations focus on three main directions: *advancing interaction modeling*, *fine-grained user interest understanding*, and *incorporating external knowledge*.

The effectiveness optimizations of ULBM can be characterized along three dimensions:

![Effectiveness](fig/effectiveness.png)

## Papers
We provide a curated collection of references related to ULBM, including:
- short-sequence modeling,
- search-based methods,
- compression-based methods,
- Hybrid methods,
- End-to-End methods,
- Methods on heterogeneous user behaviors,
- Methods on incorporation of external knowledge.

- **Short-sequence Modeling:** Early and foundational methods that provide essential modeling principles for capturing user preferences through short-term interaction dynamics.

|  Method   |                                             Paper Title                                              |   Published At    |
| :-------: | :--------------------------------------------------------------------------------------------------: | :---------------: |
| *GwEN* |      [Deep Neural Networks for YouTube Recommendations](https://static.googleusercontent.com/media/research.google.com/zh-CN//pubs/archive/45530.pdf)      | RecSys'16 |
| *DIN* |      [Deep Interest Network for Click-Through Rate Prediction](https://arxiv.org/abs/1706.06978)      | KDD'18 |
| *DIEN* |      [Deep Interest Evolution Network for Click-Through Rate Prediction](https://arxiv.org/abs/1809.03672)      | AAAI'19 |
| *BST* |      [Behavior Sequence Transformer for E-commerce Recommendation in Alibaba](https://arxiv.org/abs/1905.06874)      | KDD'19 |


- **Search-based Methods:** Methods that enhance both efficiency and modeling effectiveness by searching behavior subsets most relevant to the current context from long user interaction histories.

|  Method   |                                             Paper Title                                              |   Published At    |
| :-------: | :--------------------------------------------------------------------------------------------------: | :---------------: |
| *SIM* |      [Search-based User Interest Modeling with Lifelong Sequential Behavior Data for Click-Through Rate Prediction](https://arxiv.org/abs/2006.05639)      | CIKM'20 |
| *TWIN* |      [TWIN: TWo-stage Interest Network for Lifelong User Behavior Modeling in CTR Prediction at Kuaishou](https://arxiv.org/abs/2302.02352)      | KDD'23 |
| *TransAct V2* |      [TransAct V2: Lifelong User Action Sequence Modeling on Pinterest Recommendation](https://arxiv.org/abs/2506.02267)      | CIKM'25 |
| *DARE* |      [Long-Sequence Recommendation Models Need Decoupled Embeddings](https://arxiv.org/abs/2410.02604)      | ICLR'25 |
| *MARM* |      [MARM: Unlocking the Future of Recommendation Systems through Memory Augmentation and Scalable Complexity](https://arxiv.org/abs/2411.09425)      | CIKM'25 |
| *GIST* |      [GIST: Cross-Domain Click-Through Rate Prediction via Guided Content-Behavior Distillation](https://arxiv.org/abs/2507.05142)      | arXiv'25 |
| *LCN* |      [Cross Domain LifeLong Sequential Modeling for Online Click-Through Rate Prediction](https://arxiv.org/abs/2312.06424)      | KDD'24 |
| *LIC* |      [Long-Term Interest Clock: Fine-Grained Time Perception in Streaming Recommendation System](https://arxiv.org/abs/2501.15817)      | WWW'25 |
| *MIRRN* |      [Multi-granularity interest retrieval and refinement network for long-term user behavior modeling in ctr prediction](https://arxiv.org/abs/2411.15005)      | KDD'25 |
| *LongRetriever* |      [LongRetriever: Towards Ultra-Long Sequence based Candidate Retrieval for Recommendation](https://arxiv.org/abs/2508.15486)      | arXiv'25 |
| *ETA* |      [End-to-End User Behavior Retrieval in Click-Through RatePrediction Model](https://arxiv.org/abs/2108.04468)      | arXiv'21 |
| *SDIM* |      [Sampling Is All You Need on Modeling Long-Term User Behaviors for CTR Prediction](https://arxiv.org/abs/2205.10249)      | CIKM'22 |
| *CoFARS* |      [Context-based Fast Recommendation Strategy for Long User Behavior Sequence in Meituan Waimai](https://arxiv.org/abs/2403.12566)      | WWW'24 |
| *UBR4CTR* |      [User Behavior Retrieval for Click-Through Rate Prediction](https://arxiv.org/abs/2005.14171)      | SIGIR'20 |
| *QIN* |      [Query-dominant User Interest Network for Large-Scale Search Ranking](https://arxiv.org/abs/2310.06444)      | CIKM'23 |
| *MUSE* |      [MUSE: A Simple Yet Effective Multimodal Search-Based Framework for Lifelong User Interest Modeling](https://arxiv.org/abs/2512.07216)      | arXiv'25 |


- **Compression-based Methods:** Methods that transform long behavior sequences into a limited number of compact representations to support scalable and effective user modeling.

|  Method   |                                             Paper Title                                              |   Published At    |
| :-------: | :--------------------------------------------------------------------------------------------------: | :---------------: |
| *DV365* |      [DV365: Extremely Long User History Modeling at Instagram](https://arxiv.org/abs/2506.00450)      | KDD'25 |
| *ULIM* |      [User Long-Term Multi-Interest Retrieval Model for Recommendation](https://arxiv.org/abs/2507.10097)      | RecSys'25 |
| *PinFM* |      [PinFM: Foundation Model for User Activity Sequences at a Billion-scale Visual Discovery Platform](https://arxiv.org/abs/2507.12704)      | RecSys'25 |
| *LREA* |      [LREA: Low-Rank Efficient Attention on Modeling Long-Term User Behaviors for CTR Prediction](https://arxiv.org/abs/2503.02542)      | SIGIR'25 |
| *HiT-LBM* |      [Hierarchical Tree Search-based User Lifelong Behavior Modeling on Large Language Model](https://arxiv.org/abs/2505.19505)      | SIGIR'25 |
| *Climber* |      [An Efficient Large Recommendation Model: Towards a Resource-Optimal Scaling Law](https://arxiv.org/abs/2502.09888)      | CIKM'25 |
| *VQL* |      [VQL: An End-to-End Context-Aware Vector Quantization Attention for Ultra-Long User Behavior Modeling](https://arxiv.org/abs/2508.17125)      | arXiv'25 |
| *ENCODE* |      [ENCODE: Breaking the Trade-Off Between Performance and Efficiency in Long-Term User Behavior Modeling](https://arxiv.org/abs/2508.13567)      | TKDE'25 |
| *Trinity* |      [Trinity: Syncretizing Multi-/Long-tail/Long-term Interests All in One](https://arxiv.org/abs/2402.02842)      | KDD'24 |
| *UUM* |      [Learning Universal User Representations Leveraging Cross-domain User Intent at Snapchat](https://arxiv.org/abs/2504.21838)      | SIGIR'25 |
| *DMQN* |      [Deep Multiple Quantization Network on Long Behavior Sequence for Click-Through Rate Prediction](https://arxiv.org/abs/2508.20865)      | SIGIR'25 |
| *DiffuMin* |      [Modeling Long-term User Behaviors with Diffusion-driven Multi-interest Network for CTR Prediction](https://arxiv.org/abs/2508.15311)      | RecSys'25 |
| *CHIME* |      [CHIME: A Compressive Framework for Holistic Interest Modeling](https://arxiv.org/abs/2504.06780)      | arXiv'25 |
| *MIMN* |      [Practice on Long Sequential User Behavior Modeling for Click-Through Rate Prediction](https://arxiv.org/abs/1905.09248)      | KDD'19 |
| *CAIN* |      [Context-Aware Lifelong Sequential Modeling for Online Click-Through Rate Prediction](https://arxiv.org/abs/2502.12634)      | arXiv'25 |
| *VISTA* |      [Massive Memorization with Hundreds of Trillions of Parameters for Sequential Transducer Generative Recommenders](https://arxiv.org/abs/2510.22049)      | arXiv'25 |
| *DGIN* |      [Deep Group Interest Modeling of Full Lifelong User Behaviors for CTR Prediction](https://arxiv.org/abs/2311.10764)      | arXiv'23 |


- **Hybrid Methods:** Approaches that combine retrieval-based and compression-based strategies to balance efficiency and effectiveness when modeling ultra-long user behavior sequences.

|  Method   |                                             Paper Title                                              |   Published At   | Paradigm       | 
| :-------: | :--------------------------------------------------------------------------------------------------: | :---------------:| :--------------|
| *ADFM* |      [Adversarial Filtering Modeling on Long-term User Behavior Sequences for Click-Through Rate Prediction](https://arxiv.org/abs/2204.11587)      | SIGIR'22 | Compression - Search ｜
| *HBM* |      [Hierarchical User Long-term Behavior Modeling forClick-Through Rate Prediction](https://dl.acm.org/doi/10.1145/3726302.3730207)      | SIGIR'25 | Compression - Search ｜
| *TWIN V2* |      [TWIN V2: Scaling Ultra-Long User Behavior Sequence Modeling for Enhanced CTR Prediction at Kuaishou](https://arxiv.org/abs/2407.16357)      | CIKM'24 | Compression - Search ｜
| *DMGIN* |      [DMGIN: How Multimodal LLMs Enhance Large Recommendation Models for Lifelong User Post-click Behaviors](https://arxiv.org/abs/2508.21801)      | arXiv'25 | Compression - Search ｜
| *DILN* |      [Interest Changes: Considering User Interest Life Cycle in Recommendation System](https://arxiv.org/abs/2505.08471)      | SIGIR'25 | Search - Compression |


- **End-to-End Methods:** Approaches that directly model ultra-long user behavior sequences in a unified framework without explicit preprocessing, enabling holistic preference learning.

|  Method   |                                             Paper Title                                              |   Published At    |
| :-------: | :--------------------------------------------------------------------------------------------------: | :---------------: |
| *STCA* |      [Make It Long, Keep It Fast: End-to-End 10k-Sequence Modeling at Billion Scale on Douyin](https://arxiv.org/abs/2511.06077)      | arXiv'25 |
| *LONGER* |      [LONGER: Scaling Up Long Sequence Modeling in Industrial Recommenders](https://arxiv.org/abs/2505.04421)      | RecSys'25 |
| *HSTU* |      [Actions Speak Louder than Words: Trillion-Parameter Sequential Transducers for Generative Recommendations](https://arxiv.org/abs/2402.17152)      | ICML'24 |
| *MTGR* |      [MTGR: Industrial-Scale Generative Recommendation Framework in Meituan](https://arxiv.org/abs/2505.18654)      | CIKM'25 |
| *GenRank* |      [Towards Large-scale Generative Ranking](https://arxiv.org/abs/2505.04180)      | arXiv'25 |
| *Fuxi-$\alpha$* |      [FuXi-α: Scaling Recommendation Model with Feature Interaction Enhanced Transformer](https://arxiv.org/abs/2502.03036)      | WWW'25 |



## Datasets

## Acknowledgement

## How to Contribute

