
# CSR Classification: Detecting Greenwashing in Corporate Statements

## Introduction

This project aims to **classify corporate social responsibility (CSR) statements** to evaluate their authenticity, helping consumers and investors distinguish genuine sustainability efforts from greenwashing. The system uses machine learning and NLP, leveraging BERT fine-tuning to categorize statements as either **genuine, mixed, or pure greenwashing**.

---

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Data Sources](#data-sources)
- [Label Categories](#label-categories)
- [Installation](#installation)
- [Usage](#usage)
- [Model Performance](#model-performance)
- [Examples](#examples)

---

## Features

- **Automated classification** of CSR statements as genuine, mixed, or greenwashing.
- **BERT-based fine-tuned model** with high test accuracy.
- **Insightful language analysis** highlighting important linguistic markers.
- Addresses **dataset imbalance** and provides guidelines for annotation.

---

## Data Sources

Publicly available, non-proprietary, and non-copyrighted:
- Corporate social responsibility reports
- Public corporate press releases
- Sustainability blogs
- Company websites

---

## Label Categories

CSR statements are classified into three categories:

- **L1: Genuine Impact-Driven**
  - Action-oriented, quantified, externally verified, accountable, minimal self-promotion.
- **L2: Mixed (Real Impact but PR-heavy)**
  - Some real action, but diluted by promotional language, vague context, or missing metrics.
- **L3: Pure Greenwashing**
  - Vague, unverified, or symbolic statements serving mainly as image-enhancing tools with no substantial evidence.
  
---

## Installation

1. **Clone the repository** (or copy project files).

2. **Install required dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
   > **Dependencies:**  
   > - Python 3.8+  
   > - `transformers`  
   > - `torch`  
   > - `scikit-learn`  
   > - `pandas`, `numpy`

---

## Usage

1. **Load and preprocess data**: Loads CSR statement data, cleans and preprocesses text, and filters relevant columns.
2. **Data annotation**: Applies manual or provided labels (Genuine, Mixed, Greenwashing) to statements for supervised learning.
3. **Model training**: Fine-tunes a BERT-based classifier on annotated CSR statements.
4. **Evaluation and analysis**: Evaluates the classifier's performance (accuracy, confidence intervals), analyzes language features, and discusses model strengths and weaknesses.

To run the main workflow, execute:

run all cells in `csr_classifiction.ipynb`.

---

## Model Performance

- **Best Model:** BERT Fine-Tuning
- **Test Accuracy:** 99%
- **95% Confidence Interval:** (0.9703, 1.0097)
  > *Note: Theoretical accuracy cannot exceed 100%; statistical error included.*

#### Key Findings

- Sentences with **verified results** and **specific numbers** are classified as genuine.
- **Abstract or aspirational language** (e.g., "journey", "aspirations", “planet”) is often classified as greenwashing.
- **Imbalanced dataset**: Greenwashing statements are less frequent.
- BERT model **generalizes well** to subtle language differences.

---

## Examples

**Label 1: Genuine Impact-Driven**
```
“In 2023, we installed 15,000 solar panels at our manufacturing facility, reducing annual CO₂ emissions by 30%, as verified by EnergyTrust.”
```

**Label 2: Mixed (Real Impact but PR-heavy)**
```
“Our packaging is now made from recycled materials, and we are continuously striving to lead the industry in eco-innovation.”
```

**Label 3: Pure Greenwashing**
```
“We care about the Earth and are always looking for ways to go green.”
```

---

## Contributors

- Collin Lee
- Kavin Vasudevan
- Xinyun Liu
- Arhaan Aggarwal

---