# Few-shot named entity recognition with hybrid multi-prototype learning (The code and data are being collated and updated, and the official version will be released in this project later.)

This repository contains the open-sourced official implementation of the paper:

Few-shot named entity recognition with hybrid multi-prototype learning.

_Zenghua Liao, Junbo Fei, Weixin Zeng and Xiang Zhao_



For any questions/comments, please feel free to open GitHub issues.

## 🎥 Overview

Information extraction provides the basic technical support for knowledge graph construction and Web applications. Named entity recognition (NER) is one of the fundamental tasks of information extraction. Recognizing unseen entities from numerous contents with the support of only a few labeled samples, also termed as few-shot learning, is a crucial issue to be studied. Few-shot NER aims at identifying emerging named entities from the context with the support of a few labeled samples. Existing methods mainly use the same strategy to construct a single prototype for each entity or non-entity class, which has limited expressiveness power and even biased representation. In this work, we propose a novel hybrid multi-prototype class representation approach. Specifically, for entity classes, we first insert labels after entities in support sentences to enrich the learned token and label embeddings with more contextual information. Then, for each entity span, the contextual token embeddings are averaged to form its entity-level prototype, while the contextual label embedding is considered as its label-level prototype. The set of prototypes for all entities in a class constitutes the multi-prototype of this entity class. For non-entity class, we directly use the set of token embeddings to represent it, where multi-prototype refers to the multiple token embeddings. By treating the entity and non-entity classes differently, our hybrid strategy can extract more precise class representations from the support examples. Furthermore, we establish a harder and more reasonable experimental setting of few-shot NER by offering a rigorous sampling strategy. Extensive empirical results show that our proposal improves performance over prior models on popular benchmark Few-NERD under both loose and our proposed rigorous sampling constraints, achieving comparable performance to current state-of-the-arts.



## 🎯 Quick Start

### Requirements

- python 3.9
- pytorch 1.9.0+cu111
- Few-NERD dataset

Few-nerd is the HMP implementation.
The DecomposedMetaNER adds extra CRF.
