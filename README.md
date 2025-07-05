# 🎓 College Feedback Classifier

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Watsonx.ai](https://img.shields.io/badge/IBM-Watsonx.ai-blueviolet)
![License: MIT](https://img.shields.io/badge/License-MIT-green)

> Automatically classify student feedback into **Academics**, **Facilities**, or **Administration** using IBM Watsonx.ai Foundation Models.

---

## 📚 Table of Contents

- [🧠 Project Overview](#-project-overview)
- [🎯 Objectives](#-objectives)
- [🛠️ Tools & Technologies](#-tools--technologies)
- [📈 Methodology](#-methodology)
- [📊 Visualizations](#-visualizations)
- [🚀 How to Run](#-how-to-run)
- [📂 Project Structure](#-project-structure)
- [✅ Sample Output](#-sample-output)
- [🐛 Challenges & Solutions](#-challenges--solutions)
- [📚 References](#-references)

---

## 🧠 Project Overview

This project uses **few-shot learning** and the **FLAN-T5-XXL** model from IBM Watsonx to transform unstructured student feedback into actionable categories, enabling better administrative decisions in educational institutions.

---

## 🎯 Objectives

- Classify student feedback into **Academics**, **Facilities**, or **Administration**
- Use **few-shot prompting** for zero-training text classification
- Visualize and export model results for evaluation

---

## 🛠️ Tools & Technologies

| Tool                  | Purpose                           |
|-----------------------|-----------------------------------|
| **Python**            | Programming Language              |
| **Watsonx.ai**        | Foundation Model Inference        |
| **FLAN-T5-XXL**       | Text-to-text classification       |
| **IBM COS**           | Cloud storage for datasets        |
| **Pandas / Sklearn**  | Data handling and evaluation      |
| **Matplotlib / Seaborn** | Data Visualization             |

---

## 📈 Methodology

```mermaid
graph TD
A[Load CSV Feedback Data] --> B[Preprocess & Split Data]
B --> C[Create Few-Shot Prompt Examples]
C --> D[Call FLAN-T5 Model for Prediction]
D --> E[Compare Actual vs Predicted]
E --> F[Export Results & Visualize Performance]

![image](https://github.com/user-attachments/assets/38549c1d-6aa2-44bd-984e-dcad4a684449)

![image](https://github.com/user-attachments/assets/fb67d9b0-169d-47d5-abda-98cea9d79e07)

![image](https://github.com/user-attachments/assets/6cebeb0e-cfa5-4812-84d1-86486353d965)
📚 References
🔗 IBM Watsonx.ai Docs

🔗 FLAN-T5 Research Paper

🔗 Scikit-learn Classification Metrics


