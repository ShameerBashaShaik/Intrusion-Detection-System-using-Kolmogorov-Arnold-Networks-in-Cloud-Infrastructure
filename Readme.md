# Intrusion Detection System for Cloud Infrastructure using DKD-KAN

## Overview

This repository contains the implementation and ongoing research work for a cloud-based Intrusion Detection System (IDS) using **DKD-KAN (Decoupled Knowledge Distillation based Kolmogorov-Arnold Network)**.

The project focuses on improving intrusion detection in modern cloud infrastructures by combining:

- Kolmogorov-Arnold Networks (KAN)
- Knowledge Distillation
- AI-based Feature Selection
- Explainable AI (XAI)
- SMOTE-based imbalance handling
- OpenStack cloud simulation

Traditional IDS approaches often face limitations in balancing:
- Detection accuracy
- Computational efficiency
- Model interpretability
- Scalability in distributed cloud environments

This work aims to address these challenges through a lightweight yet efficient hybrid framework capable of operating in dynamic cloud infrastructures.

---

# Research Motivation

Cloud infrastructures generate massive volumes of dynamic and heterogeneous network traffic. Existing Machine Learning and Deep Learning based IDS solutions often suffer from:

- High computational overhead
- Poor generalization
- Limited interpretability
- Difficulty handling class imbalance
- Inefficient feature representations

Recent advancements in **Kolmogorov-Arnold Networks (KANs)** have shown promising results in learning complex functional relationships with improved parameter efficiency.

However, KAN models can still be computationally intensive for deployment in practical cloud environments.

To overcome this limitation, this work introduces a hybrid framework based on:

## DKD-KAN
A combination of:
- KAN as the Teacher Model
- MLP as the Student Model
- Decoupled Knowledge Distillation (DKD)

This enables:
- Better feature representation
- Reduced inference cost
- Improved deployment feasibility
- Efficient cloud-scale intrusion detection

---

# Objectives

The primary objectives of this research are:

- Develop a cloud-oriented IDS using DKD-KAN
- Improve intrusion detection accuracy
- Reduce computational and inference overhead
- Enhance interpretability using SHAP and LIME
- Handle dataset imbalance using SMOTE
- Build a scalable and robust IDS framework
- Evaluate deployment feasibility in OpenStack environments

---

# Proposed Methodology

The workflow of the proposed IDS framework consists of the following stages:

## 1. Dataset Collection
Datasets currently explored:
- BCCC
- TestCloudIDS
- CAShift

---

## 2. Data Preprocessing
- Missing value handling
- Global mean imputation
- Min-Max normalization
- Standardization

---

## 3. Feature Selection

### AI-Based Feature Selection
Techniques explored:
- Genetic Algorithm (GA)
- Ant Colony Optimization (ACO)
- Particle Swarm Optimization (PSO)
- Grey Wolf Optimization (GWO)

Evaluation metrics:
- F1-Score
- MCC (Matthews Correlation Coefficient)

### Random Forest Feature Selection
- Feature importance ranking
- Noise reduction
- Dimensionality reduction

---

## 4. Ensemble Voting
Consensus-based feature selection for:
- Improved robustness
- Noise elimination
- Stable feature subsets

---

## 5. SMOTE Oversampling
Handling class imbalance through:
- Synthetic Minority Oversampling Technique (SMOTE)

Goals:
- Improved minority class detection
- Reduced model bias

---

## 6. DKD-KAN Framework

### Teacher Model
- Kolmogorov-Arnold Network (KAN)

### Student Model
- Multi-Layer Perceptron (MLP)

### Knowledge Distillation
Using Decoupled Knowledge Distillation:
- TCKD (Target Class KD Loss)
- NCKD (Non-Target Class KD Loss)

Benefits:
- Lower computation cost
- Faster inference
- Better deployment feasibility
- Accuracy retention

---

## 7. Explainable AI (XAI)

Interpretability modules:
- SHAP
- LIME

Purpose:
- Feature importance analysis
- Local and global interpretability
- Transparent decision-making

---

## 8. OpenStack-Based Simulation

The final deployment architecture is planned over OpenStack cloud infrastructure for:
- Real-world simulation
- Distributed testing
- Scalable evaluation

---

# Why KAN?

KANs were selected due to:

- Learnable activation functions
- Better symbolic representation
- Parameter efficiency
- Smooth spline-based learning
- Strong capability in modeling complex relationships

---

# Why DKD-KAN?

The DKD-KAN framework offers:

- Better feature representation
- Improved intrusion detection accuracy
- Reduced parameter count
- Improved interpretability
- Lower inference cost
- Better suitability for cloud IDS systems

---

# Current Progress

## Completed Work

### Research and Literature Review
- Studied multiple IDS research papers
- Analyzed KAN architectures
- Compared traditional ML/DL approaches

### Dataset Analysis
- Dataset detailing completed
- Initial preprocessing completed

### Feature Engineering
- AI-based feature selection completed
- Random Forest feature selection completed
- Ensemble voting completed

### Model Implementations
Implemented and analyzed:
- MLP
- Linear Regression
- KAN

### Data Balancing
- SMOTE analysis completed

### Documentation
- Paper summaries prepared
- Research conclusions documented

### Ongoing Work
- CAShift dataset generation from SCAP to CSV conversion
- DKD-KAN implementation refinement

---

# Future Work

The following research directions are currently planned:

- DKD-KAN evaluation on multiple datasets
- Comparative analysis with traditional IDS models
- SHAP and LIME interpretability implementation
- Hyperparameter tuning
- K-Fold Cross Validation
- OpenStack simulation
- Online learning integration
- Optimization of spline and grid orders
- Reduction of training and inference time

---

# Expected Contributions

This work aims to contribute:

- A lightweight cloud IDS framework
- Efficient hybrid KAN-distillation architecture
- Reduced computation and parameter cost
- Improved detection robustness
- Explainable and interpretable intrusion detection
- Scalable deployment capability for cloud environments

---

# Repository Structure

```bash
├── datasets/                 # Dataset files and preprocessing
├── preprocessing/            # Data cleaning and normalization
├── feature_selection/        # AI and RF based feature selection
├── models/
│   ├── mlp/
│   ├── kan/
│   └── dkd_kan/
├── explainability/           # SHAP and LIME implementations
├── openstack_simulation/     # OpenStack deployment setup
├── notebooks/                # Experimental notebooks
├── results/                  # Experimental outputs and metrics
├── docs/                     # Research notes and documentation
└── README.md