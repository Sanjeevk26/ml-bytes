# ML Bytes

**ML Bytes** is a collection of **bite-sized, story-driven explanations of core machine learning concepts**, backed by **runnable Python notebooks and scripts**.  
The goal is simple: **build intuition, not just formulas.**

This repository is designed for:
- Beginners learning ML fundamentals  
- Professionals preparing for interviews  
- Practitioners who want clear mental models for real-world ML decisions  

---

## What This Repo Focuses On

- Explaining **what ML concepts actually mean in practice**
- Using **real-world stories and analogies** (not abstract math)
- Demonstrating **trade-offs and pitfalls**
- Keeping everything **small, readable, and executable**

Each ML Byte is intentionally focused on **one concept at a time**.

---

## Repository Structure

This repo contains two kinds of learning assets:

### 1) Story-Driven Concept Notes (Markdown)
These files explain each concept using a single, coherent real-world story.

| File | Concept |
|------|--------|
| `classification-metrics-story.md` | Accuracy, Precision, Recall, F1 using an **Airport Security Scanner** |
| `roc_vs_precision_recall_story.md` | ROC vs Precision-Recall using real-world decision trade-offs |
| `model_calibration_story.md` | Why probability calibration matters |
| `class_imbalance_story_and_mitigation.md` | What class imbalance means and how to fix it |
| `data_leakage_story.md` | How data leakage silently breaks models |
| `underfitting_vs_overfitting_story.md` | Bias, variance, and generalization |

These are meant to be **read like short essays** to build intuition before touching any code.

---

### 2) Runnable Notebooks (Hands-On Demos)

These notebooks show the same concepts using **real datasets and real ML models**, but kept intentionally simple.

| Notebook | What it Demonstrates |
|--------|----------------------|
| `ml-bytes-classification-metrics.ipynb` | Confusion matrix, precision, recall, F1, thresholds |
| `ml_bytes_overfitting_underfitting.ipynb` | Training vs test performance, model complexity |
| `ml_bytes_data_leakage.ipynb` | How leakage inflates accuracy and breaks real-world performance |

Each notebook can be run locally or on Colab and mirrors the story-based explanations.

---

## Core Concepts Covered

### 1) Classification Metrics  
**Accuracy, Precision, Recall, F1 Score**

Using an **Airport Security Scanner** story, this module explains:
- Confusion Matrix (TP, FP, TN, FN)
- Why accuracy fails on imbalanced data
- Precision vs Recall trade-offs
- How thresholds change model behavior
- Why F1 score exists

Files:
- `classification-metrics-story.md`
- `ml-bytes-classification-metrics.ipynb`

---

### 2) Overfitting vs Underfitting  
**Training vs Real-World Performance**

Using an **exam preparation** analogy, this module explains:
- What underfitting and overfitting really mean
- Why high training accuracy can be misleading
- Why test data matters
- How model complexity affects generalization

Files:
- `underfitting_vs_overfitting_story.md`
- `ml_bytes_overfitting_underfitting.ipynb`

---

### 3) ROC vs Precision–Recall  
**Which curve to trust and when**

Using real decision trade-offs, this module explains:
- What ROC curves actually measure
- Why PR curves are better for rare events
- How thresholds interact with both

File:
- `roc_vs_precision_recall_story.md`

---

### 4) Model Calibration  
**When probabilities lie**

This module explains:
- Why 90% confidence doesn’t always mean 90% correct
- What calibration means in real-world systems
- Why ranking ≠ probability

File:
- `model_calibration_story.md`

---

### 5) Class Imbalance  
**When the data lies to you**

This module explains:
- Why rare events break accuracy
- What imbalance really means
- Practical mitigation strategies

File:
- `class_imbalance_story_and_mitigation.md`

---

### 6) Data Leakage  
**The most dangerous silent bug**

This module explains:
- What data leakage is
- How it sneaks into pipelines
- Why it produces fake high accuracy
- How to detect and prevent it

Files:
- `data_leakage_story.md`
- `ml_bytes_data_leakage.ipynb`

---

## How To Use This Repo

Recommended flow:

1. **Read a story file** (`*.md`)  
2. **Run the matching notebook** (`*.ipynb`)  
3. **Compare intuition vs numbers**

If you can explain the idea to someone else after that, the ML Byte has worked.

---

## Philosophy

ML Bytes focuses on **understanding behavior**, not memorizing formulas.

A model that looks good in training can still fail in the real world.  
A metric that looks high can still be misleading.  
A probability that looks confident can still be wrong.

This repo is about learning to **see those traps** before they hurt you.

---

## Roadmap (Coming Next)

- Learning curves  
- Bias–variance decomposition  
- Fairness and subgroup performance  
- Real-world threshold tuning  
- Monitoring and drift  

---

If you are learning machine learning for interviews, work, or real systems — this repo is designed to give you **mental models that actually stick**.