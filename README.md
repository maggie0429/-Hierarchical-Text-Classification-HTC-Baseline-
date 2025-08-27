# Hierarchical Text Classification (HTC) Baseline

This repository provides a baseline for **Hierarchical Text Classification (HTC)** tasks, focusing on library knowledge systems such as the Dewey Decimal Classification (DDC).  
The baseline demonstrates how traditional text classification methods can be adapted to respect **hierarchical label structures**.

## 🎯 Motivation
Many real-world text classification problems (e.g., **library science, scientific paper classification, smart building ontologies**) require predictions aligned with a **label hierarchy**.  
Flat classifiers often ignore parent-child dependencies, leading to inconsistent predictions.  
This project establishes a simple, reproducible **HTC baseline** for comparison with more advanced models.

## ⚙️ Methods
- **Dataset**: Example: OpenLibrary book titles mapped to DDC top-level classes (000–900)  
- **Preprocessing**:  
  - Tokenization + TF-IDF  
  - Train/test split by stratified sampling  
- **Models**:  
  - Logistic Regression (flat baseline)  
  - Hierarchical classifier (predict parent → child)  
- **Evaluation Metrics**:  
  - Accuracy, Macro-F1  
  - Hierarchical Precision/Recall (hP, hR)

## 📊 Results
Example (demo dataset, 10 classes):

| Model                       | Macro-F1 | hPrecision | hRecall |
|------------------------------|----------|------------|---------|
| Logistic Regression (flat)  | 0.612    | 0.650      | 0.603   |
| Hierarchical Classifier      | 0.641    | 0.672      | 0.629   |

👉 Even simple hierarchical decoding improves **consistency** over flat models.

## 📦 Repository Structure
