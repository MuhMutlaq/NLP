# Lab 2: Text Pre-processing and Regular Expressions

## Student Information

**Name:** Muhannad Almutlaq  
**ID:** 2240006060

### Experimentation & Key Takeaways

* **Regular Expressions (Regex):** Utilized Python's `re` module to extract specific information from unstructured text. I experimented with functions like `search`, `match`, `findall`, and `sub` for pattern matching and text feature engineering. A practical application involved extracting and counting top hashtags from a dataset of tweets.
* **Tokenization Strategies:** Compared sentence and word tokenization using both NLTK and SpaCy pipelines. I learned that NLTK uses the unsupervised machine learning `punkt` tokenizer, while SpaCy relies on its pre-trained `en_core_web_sm` model.
* **Text Normalization:** Applied lowercasing to reduce the dimensionality of the vector space model (ensuring words like "Book" and "book" are treated identically).
* **Stemming vs. Lemmatization:** Experimented with reducing words to their root forms. I compared the PorterStemmer (older, faster) with the SnowballStemmer (better accuracy) in NLTK. I then applied Lemmatization, which unlike stemming, brings context to the words and links them based on part-of-speech (POS) tags to form meaningful root words.
* **Stop Words Optimization:** Analyzed the impact of removing low-level information (like "the", "a", "an") to reduce dataset size and training time. I also customized the stop words list by dynamically adding and removing specific tokens based on the context of the task.
