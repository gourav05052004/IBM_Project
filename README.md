🎓 College Feedback Classifier
A machine learning project using IBM Watsonx.ai Foundation Models to automatically classify open-ended student feedback into categories like Academics, Facilities, or Administration, enabling educational institutions to gain structured insights and improve decision-making.

📌 Features
✅ Classifies open-ended feedback using few-shot prompt engineering

✅ Utilizes IBM Foundation Models (FLAN-T5 XXL) for text classification

✅ Exports results to CSV and visualizes key performance metrics

✅ Generates comparison charts and a confusion matrix for analysis

🎯 Objectives
Categorize unstructured feedback into meaningful themes

Provide visual and statistical performance evaluation

Enable administrative teams to focus on targeted improvements

🛠️ Tools & Technologies
Component	Description
Language	Python
Platform	IBM Watsonx.ai + Watson Machine Learning SDK
Model	FLAN-T5-XXL (via Foundation Models)
Libraries	pandas, matplotlib, seaborn, scikit-learn, ibm-watson-machine-learning
Storage	IBM Cloud Object Storage (COS)

🧠 Methodology
Data Collection: Student feedback in CSV format

Data Preprocessing: Clean and split into train/test sets

Few-Shot Prompting: Select 2 examples per category as context

Model Selection: Use FLAN-T5-XXL for classification

Prediction: Run the model on test data using few-shot prompts

Evaluation: Visualize results, confusion matrix, and classification report

Export: Save predicted results as classified_feedback_results.csv to COS

📊 Visualizations
Category distribution before prediction

Actual vs. Predicted bar chart

Confusion matrix heatmap

Precision, recall, F1-score report

📂 Project Structure
kotlin
Copy
Edit
├── data/
│   └── college_feedback.csv
├── notebooks/
│   └── classification_notebook.ipynb
├── outputs/
│   └── classified_feedback_results.csv
├── README.md
🚀 How to Run
Upload your feedback CSV to IBM Cloud Object Storage

Set your Watsonx credentials and project ID

Run the classification notebook

View visualizations and download results

📈 Sample Output (CSV)
Feedback	Actual Category	Predicted Category
"The labs are well-equipped."	Facilities	Facilities
"Grievance handling takes too long."	Administration	Administration
"Faculty is always helpful."	Academics	Academics

🧩 Challenges Faced
Prompt formatting issues for consistent model output

Handling API latency and timeouts

Minor category confusion in predictions due to close semantics

✅ Solutions: Added exception handling, improved few-shot examples, and ensured balanced category sampling.

📚 References
IBM Watsonx.ai Documentation

FLAN-T5 Paper (Google Research)

Scikit-learn Metrics Guide
