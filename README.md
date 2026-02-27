# NLP_projects

This repository contains two distinct projects focused on Natural Language Processing (NLP) and deep learning. **Project 1** explores medical document classification using Recurrent Neural Networks (RNNs) and domain-specific embeddings, while **Project 2** provides a comparative analysis of three major neural architectures for Natural Language Inference (NLI).

---

## Project 1: Medical Abstract Classification

This project implements an end-to-end pipeline for classifying medical abstracts into five distinct categories: neoplasms, digestive system diseases, nervous system diseases, cardiovascular diseases, and general pathological conditions.

### Key Features

* 
**Text Preprocessing:** Cleans medical text by handling URLs, HTML, and domain-specific numeric units (e.g., mg, mmHg).


* **Dual Embedding Approach:**
* 
**FastText:** Custom-trained on the dataset to capture subword information for rare medical terms.


* 
**BioWordVec:** Utilizes pre-trained biomedical embeddings for enhanced semantic understanding.




* 
**Architecture:** A 2-layer **Bidirectional LSTM (BiLSTM)** with masked mean and max pooling to handle variable-length sequences and class imbalance.


* 
**Visualization:** t-SNE projections comparing the semantic neighborhoods of trained vs. pre-trained medical embeddings.



### Performance Evaluation

| Model | Accuracy | F1-Score (Weighted) |
| --- | --- | --- |
| FastText BiLSTM | 0.6229 | 0.6079 |
| **BioWordVec BiLSTM** | **0.6517** | **0.6350** |

---

## Project 2: Comparative Analysis of NLI Models

This study investigates and compares three neural architectures on the Natural Language Inference (NLI) task to determine logical relationships (entailment, contradiction, or neutral) between sentence pairs.

### Core Architectures

* 
**Model A (BiLSTM):** A sequential baseline utilizing multiple attention mechanisms (Self, Dot, General, Additive) to align premise and hypothesis.


* 
**Model B (Encoder-Decoder):** Combines an LSTM encoder with a GRU decoder to explore cross-sequence representation learning.


* 
**Model C (Transformer):** A decoder-only Transformer stack utilizing **Disentangled Self-Attention** to separate token content from positional features.



### Experimental Results

The Transformer-based model achieved the highest performance, confirming its superior ability to model long-range dependencies.

| Model | Test Accuracy |
| --- | --- |
| BiLSTM (Baseline) | 0.69285 

 |
| BiLSTM-GRU | 0.7262 

 |
| **Transformer-based** | <br>**0.76783** 

 |

### Key Findings

* 
**Attention:** Additive (Bahdanau) attention performed best for the BiLSTM architecture (0.705).


* 
**Disentangled Attention:** Content-to-position () interactions were found to be more useful than position-to-content () for NLI reasoning.



---

## Authors & Contributions

* 
**Zihan Wu (24372276):** Project 2 Model A design and implementation; ablation studies.


* **Jianyun Yang (24181422):** Project 1 ; Project 2 Model C design, implementation, and qualitative study.


* 
**Haoran Yun (24180266):** Project 2 Model B design and implementation.



*These projects were developed as part of the CITS4012 curriculum at the University of Western Australia.*
