# Lab 3: N-Grams and Language Modeling

## Student Information

**Name:** Muhannad Almutlaq  
**ID:** 2240006060

### Experimentation & Key Takeaways

* **N-Gram Architecture:** Built probabilistic models by extracting unigrams, bigrams, and trigrams from sequential text data. This process is foundational for understanding predictive text, auto-completion, and modern LLM architectures.
* **Sequence Padding:** Applied `n-1` padding (using `<s>` and `</s>` symbols) to ensure sequence data fits a standard length for contiguous batching. I experimented with NLTK's `pad_both_ends` and `padded_everygram_pipeline` to streamline this preprocessing step.
* **Maximum Likelihood Estimation (MLE):** Trained an MLE model to estimate parameters and maximize probabilities based on frequency counts derived from a corpus. I practically applied this by generating synthetic tweets using a Bigram model.
* **Data Cleaning in the Wild:** Encountered real-world dataset challenges. I wrote custom cleaning functions using regex and the `emoji` library to strip URLs, mentions, and emojis before passing the data into the language model.
* **Model Evaluation (Perplexity):** Evaluated the performance of the generated bigram model using Perplexity. I observed that a lower perplexity indicates the model is less "perplexed" by the data, meaning it assigns higher probabilities to the actual words in the test set, resulting in better predictive performance.
* **Troubleshooting & Debugging:** Gained hands-on experience resolving Python dependency clashes (specifically resolving a `numpy.dtype` binary incompatibility), managing Pandas `DtypeWarnings` using `low_memory= False`, and handling `UnicodeDecodeError` by specifying alternative encoding strategies for messy CSV files.

