# Lab 4: Text Classification and Evaluation

## Student Information

**Name:** Muhannad Almutlaq  
**ID:** 2240006060

### Experimentation & Key Takeaways

* **Sentiment Categorization:** Framed the problem as a multi-class classification task by transforming raw 1-5 star Amazon reviews into discrete sentiment classes (Positive, Neutral, Negative).
* **Text Preprocessing Pipeline:** Engineered a comprehensive 5-step data cleaning function using regular expressions. Removed URLs, punctuation, and numbers, converted text to lowercase, and filtered out standard English stopwords using NLTK to eliminate noise before vectorization.
* **Feature Extraction (TF-IDF):** Transformed unstructured review texts into structured numerical matrices using `TfidfVectorizer`. Capped the vocabulary to the top 5,000 most informative features to optimize memory usage and training speed without sacrificing model performance.
* **Classification Models:** Trained and deployed a Multinomial Naive Bayes classifier for sentiment prediction. (Also explored the application of Support Vector Machines (SVM) with linear kernels for textual data separation).
* **Model Evaluation Metrics:** Quantified model performance using comprehensive metrics beyond simple accuracy. Utilized `classification_report` to analyze Precision, Recall, and F1-scores across all three sentiment classes to get a true picture of the model's predictive power.
* **Confusion Matrix Analysis:** Constructed and explicitly ordered Confusion Matrices (Negative, Neutral, Positive) to visually diagnose misclassification patterns and understand where the model struggles (such as the common difficulty of distinguishing ambiguous "neutral" reviews from positive or negative ones).
