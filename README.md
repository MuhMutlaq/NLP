# Lab 6: Deep Learning for NLP

## Student Information

**Name:** Muhannad Almutlaq  
**ID:** 2240006060

### Experimentation & Key Takeaways

* **Binary Sentiment Classification:** Built deep learning models to classify 1,000 Yelp restaurant reviews into Negative (`0`) and Positive (`1`) sentiment categories.
* **Text Preprocessing & Data Splitting:** Cleaned raw review text using Regular Expressions (`re`) to convert text to lowercase, remove punctuation and special characters, and strip extra whitespace, followed by splitting the dataset into 80% training and 20% testing sets.
* **TF-IDF vs. Word2Vec Representation:** Converted unstructured reviews into numerical features first using `TfidfVectorizer` (`max_features= 1000`) and subsequently by training a Skip-Gram (`sg= 1`) Word2Vec model (`vector_size= 200`, `window= 5`, `min_count= 1`) to represent each review as a single vector.
* **PyTorch Tensor Conversion:** Transformed the extracted numerical feature vectors and sentiment labels into PyTorch `FloatTensor` objects for neural network compatibility.
* **Feedforward Neural Network Architectures:** Designed multi-layer neural networks using `torch.nn.Sequential`, `nn.Linear`, and `nn.ReLU` activation functions, experimenting with both a two-hidden-layer baseline (`64 → 32 → 1`) and a deeper three-hidden-layer architecture (`128 → 64 → 32 → 1`).
* **Loss Calculation & Backpropagation:** Trained the neural networks across multiple epochs using `BCEWithLogitsLoss` for numerically stable binary cross-entropy computation and the `Adam` optimizer to update model weights via backpropagation.
* **Model Evaluation & Metrics:** Applied `torch.sigmoid` to map raw output logits to probabilities with a `0.5` decision threshold, assessing model performance using Test Accuracy, Confusion Matrices, and Classification Reports (Precision, Recall, and F1-score).
