# FIT5215 Deep Learning Portfolio (2025)

This repository contains my coursework solutions and experiment outputs for deep learning projects, including image classification robustness and NLP question classification.

## Repository Structure

- `3137807_assignment01_solution/`
  - `Assignment01_solution.ipynb`
  - `Assignment01_output.html`
- `31378307_assignment02_solution/`
  - `FIT5215_DeepLearning_Assignment2_Official[Main].ipynb`
  - `FIT5215_DeepLearning_Assignment2_Official[RNNs].ipynb`
  - `FIT5215_DeepLearning_Assignment2_Official[Transformers].ipynb`
  - `DeepLearning/*.html`

## What I Built

### 1) Assignment 1 (Deep Neural Networks + CNN + Robustness)

- Implemented and trained multiple models for image classification.
- Ran ablation-style comparisons for loss design and optimization strategy.
- Implemented adversarial evaluation/training with FGSM and PGD-20.

Key metrics from executed outputs:

- FFN baseline test accuracy: `87.30%`
- Entropy-regularized FFN (`lambda=0.1`) test accuracy: `87.13%`
- SAM model test accuracy: `87.18%`
- Another CNN setting test accuracy: `62.45%`
- Mixup test accuracy: `47.47%`
- CutMix test accuracy: `44.30%`
- Baseline robustness check:
  - Clean test accuracy: `53.59%`
  - Robust test accuracy: `0.84%`
- Adversarial training pipeline:
  - Pre-training validation accuracy: `53.91%`
  - Best robust validation accuracy: `22.20%`
  - Final clean accuracy: `14.14%`
  - PGD-20 robust accuracy: `15.82%`
  - FGSM robust accuracy: `30.17%`
  - PGD robustness gain vs baseline (`0.84%`): `+14.98%`

### 2) Assignment 2 (Sequential/NLP Models)

- Built end-to-end text classification pipeline on 6-class question classification.
- Implemented and compared:
  - Word2Vec + Logistic Regression baseline
  - TextCNN
  - SimpleRNN/LSTM/GRU (different output pooling strategies)
  - Attention-enhanced RNN
  - Transformer encoder classifier
  - Prefix-tuning on pretrained BERT (`bert-base-uncased`)

Key metrics from executed outputs:

- Word2Vec + Logistic Regression validation accuracy: `0.8990`
- TextCNN test accuracy: `95.5224%`

RNN family (test accuracy):

- Simple RNN (mean): `85.07%`
- Simple RNN (max): `96.52%`
- Simple RNN (last_state): `37.81%`
- LSTM (mean): `96.02%`
- LSTM (max): `96.02%`
- LSTM (last_state): `85.07%`
- GRU (mean): `95.52%`
- GRU (max): `97.01%`
- GRU (last_state): `96.02%`
- AttentionRNN (mean): `98.01%`

Embedding run mode comparison (test accuracy):

- `scratch`: `97.01%`
- `init-only`: `98.01%`
- `init-fine-tune`: `96.52%`

Transformer / Prompt tuning:

- Transformer classifier test accuracy: `97.0149%`
- Prefix-tuning (BERT) test accuracy: `97.51%`
- Best tuned prefix model test accuracy: `98.51%`
- Checkpoint reload consistency: `98.51%` (same as in-memory best model)

## Resume-Ready Highlights (CN)

- 独立完成 `FFN/CNN/RNN/LSTM/GRU/Attention/Transformer/BERT Prefix-Tuning` 的建模与训练，建立统一实验与评估流程。
- 在 6 类问题分类任务上实现系统化模型对比，最佳模型达到 `98.51%` 测试准确率，并完成 checkpoint 保存与重载一致性验证。
- 在鲁棒学习实验中实现 `FGSM/PGD-20` 攻击与对抗训练，PGD 鲁棒准确率由 `0.84%` 提升至 `15.82%`（`+14.98%`）。

## Resume-Ready Highlights (EN)

- Built and evaluated a full deep-learning model suite (`FFN/CNN/RNN/LSTM/GRU/Attention/Transformer/BERT Prefix-Tuning`) with a consistent training/evaluation pipeline.
- Achieved up to `98.51%` test accuracy on 6-class question classification, with reproducible checkpoint save/reload verification.
- Implemented adversarial robustness evaluation/training (FGSM, PGD-20), improving PGD robust accuracy from `0.84%` to `15.82%` (`+14.98%`).

## Reproducibility Notes

- This repo stores executed notebooks and exported HTML with training logs and final metrics.
- Main evidence files:
  - `3137807_assignment01_solution/Assignment01_output.html`
  - `31378307_assignment02_solution/FIT5215_DeepLearning_Assignment2_Official[Main].ipynb`
  - `31378307_assignment02_solution/FIT5215_DeepLearning_Assignment2_Official[RNNs].ipynb`
  - `31378307_assignment02_solution/FIT5215_DeepLearning_Assignment2_Official[Transformers].ipynb`
