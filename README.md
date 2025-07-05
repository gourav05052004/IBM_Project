# 🎓 College Feedback Classifier

A project that uses **few-shot prompt engineering** and **foundation models** like FLAN-T5 (via IBM Watsonx.ai) to classify student feedback into categories like **Academics**, **Facilities**, and **Administration**. This helps educational institutions analyze feedback and take actionable steps for improvement.

---

## 📌 Project Overview

This project demonstrates how to:
- Automatically classify open-ended student feedback.
- Use few-shot learning with prompt templates.
- Apply IBM Watsonx Foundation Models (FLAN-T5) for multi-class classification.
- Export structured results and visualize category-wise distribution.

---

## 🎯 Objectives

- Classify free-form student feedback into predefined themes.
- Generate synthetic feedback data for testing.
- Enable easy analysis of student sentiments.
- Provide a foundation for integration into college feedback systems.

---

## 🧰 Tools & Technologies Used

| Tool / Tech                   | Purpose                                 |
|-------------------------------|------------------------------------------|
| Python                        | Main programming language                |
| IBM Watsonx.ai (FLAN-T5)      | Foundation model for inference           |
| IBM Cloud Object Storage      | Store & retrieve datasets/output         |
| Pandas, Seaborn, Matplotlib   | Data manipulation & visualization        |
| Scikit-learn                  | Evaluation metrics and splitting         |
| Jupyter / Watson Studio Runtimes | Notebook execution environment      |
| CSV                           | Feedback input/output format             |

---

## 🗂️ Dataset

The dataset used is a **synthetic collection of 150+ student feedback entries**, manually categorized into:
- **Academics**
- **Facilities**
- **Administration**

**Filename**: `college_feedback.csv`  
Sample structure:

| Feedback                                             | Category        |
|------------------------------------------------------|------------------|
| The water coolers don't work most of the time.       | Facilities       |
| Professors are excellent in explaining the subject.  | Academics        |

---

## 🧠 Methodology

1. **Data Upload**  
   Upload `college_feedback.csv` to IBM Cloud Object Storage.

2. **Few-Shot Prompt Construction**  
   - Sample 2 feedbacks per category as context.
   - Format prompt with label examples.

3. **Model Setup**  
   - Load `FLAN-T5-XXL` model using IBM Watson Machine Learning SDK.
   - Set decoding parameters for consistent output.

4. **Prediction**  
   - Run model over all test feedback using prompt + input.
   - Store results and append predicted category.

5. **Evaluation & Visualization**  
   - Generate bar chart of actual vs predicted.
   - Display confusion matrix and classification report.
   - Export final results to CSV.

---

## 📈 Visualizations

- 📊 Feedback Category Distribution (before prediction)
- 📊 Actual vs Predicted Counts
- 🔥 Confusion Matrix
- 📝 Classification Report (Precision, Recall, F1)

---

## 💻 How to Run

1. Upload your dataset (`college_feedback.csv`) to IBM Cloud Object Storage.
2. Open the classification notebook in IBM Watson Studio or Watsonx.ai Runtime.
3. Set your:
   - API key (securely using `getpass`)
   - Project ID
4. Run cells for:
   - Data loading
   - Prompt generation
   - Model inference
   - Export and visualizations
5. Download `classified_feedback_results.csv` from COS.

---

## ✅ Output Example

| Feedback                                        | Actual Category | Predicted Category |
|-------------------------------------------------|------------------|---------------------|
| "Faculty is responsive to student queries."     | Academics        | Academics           |
| "Cleanliness is not maintained in washrooms."   | Facilities       | Facilities          |
| "Fees processing takes too long."               | Administration   | Administration      |

---

## 🐛 Challenges Faced

| Problem                        | Solution                                  |
|-------------------------------|--------------------------------------------|
| API timeout with long inputs  | Batched requests and exception handling   |
| Model misclassification       | Improved prompt quality and clarity       |
| COS file read errors          | Used `ibm_boto3` with correct region/key   |

---

## 📚 References

- [IBM Watsonx.ai Documentation](https://www.ibm.com/docs/en/watsonx)
- [FLAN-T5 Paper (Google Research)](https://arxiv.org/abs/2210.11416)
- [Scikit-learn Metrics](https://scikit-learn.org/stable/modules/classes.html#module-sklearn.metrics)

---

> 💡 *This project demonstrates how modern foundation models can bring automation to educational sentiment analysis.*
