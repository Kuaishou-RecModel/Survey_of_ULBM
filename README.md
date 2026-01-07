
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
We provide a curated collection of references related to ULBM, including works on *short-sequence modeling*, *search-based ULBM methods*, *compression-based ULBM methods*, approaches that focus on *modeling heterogeneous user behaviors*, and methods that emphasize the *incorporation of external knowledge*.

- **short-sequence modeling:** Approaches that model user preferences based on short-term interaction histories, which are effective for capturing immediate intent but limited in representing long-term interests.

|  Method   |                                             Paper Title                                              |   Published At    |
| :-------: | :--------------------------------------------------------------------------------------------------: | :---------------: |
| *GwEN* |      [Deep Neural Networks for YouTube Recommendations](https://static.googleusercontent.com/media/research.google.com/zh-CN//pubs/archive/45530.pdf)      | RecSys'16 |
| *DIN* |      [Deep Interest Network for Click-Through Rate Prediction](https://arxiv.org/abs/1706.06978)      | KDD'18 |
| *DIEN* |      [Deep Interest Evolution Network for Click-Through Rate Prediction](https://arxiv.org/abs/1809.03672)      | AAAI'19 |
| *BST* |      [Behavior Sequence Transformer for E-commerce Recommendation in Alibaba](https://arxiv.org/abs/1905.06874)      | KDD'19 |

## Datasets

## Acknowledgement

## How to Contribute

