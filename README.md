# ABEX-RAT: Synergizing Abstractive Augmentation and Adversarial Training for Classification of Occupational Accident Reports


## 📖 About

This repository contains the implementation of **ABEX-RAT**, a novel framework designed for the efficient and accurate classification of occupational accident reports. This project addresses the significant challenge of severe class imbalance in real-world datasets, which often compromises the performance of analytical models, particularly for rare but severe incident types.

ABEX-RAT synergizes generative data augmentation with robust adversarial training to boost classification performance, establishing a highly effective and efficient alternative to resource-intensive fine-tuning of large models.

## 🚀 Framework

The ABEX-RAT architecture is a three-stage pipeline as illustrated in the paper.
<img width="2470" height="1366" alt="frame" src="https://github.com/user-attachments/assets/f41d9269-88b9-4556-9ca4-5d42e4d2cf5a" />

1.  **Stage 1: Abstractive-Expansive (ABEX) Data Augmentation**:
    * A large language model (LLM), such as Qwen3, is used to distill raw accident reports into concise abstracts that capture the core semantics.
    * A BART-based generative model then expands these abstracts into multiple diverse, high-quality synthetic samples, particularly for underrepresented classes, to balance the dataset.

2.  **Stage 2: Feature Extraction**:
    * A pre-trained text embedding model (e.g., Qwen3-Embedding) converts all text samples (both original and augmented) into dense semantic vectors. This allows for an efficient feature representation for the classifier.

3.  **Stage 3: Random Adversarial Training (RAT) & Classification**:
    * A lightweight Multi-Layer Perceptron (MLP) classifier is trained on the semantic vectors.
    * It uses a computationally efficient Random Adversarial Training (RAT) protocol. This protocol stochastically applies perturbations to the inputs, enhancing model generalization and robustness without significant computational overhead.
    * A focal loss function is used to further address class imbalance during training.


## 💻 Code

The code is being organized and will be available soon. **Coming soon!**

## 📝 Citation

If you use our work in your research, please cite our paper:

```bibtex
@inproceedings{chen2026abexrat,
  title={ABEX-RAT: SYNERGIZING ABSTRACTIVE AUGMENTATION AND ADVERSARIAL TRAINING FOR CLASSIFICATION OF OCCUPATIONAL ACCIDENT REPORTS},
  author={Chen, Jian and Li, Zhou},
  booktitle={},
  year={2026},
  organization={IEEE}
}
```
