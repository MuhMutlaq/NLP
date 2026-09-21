# Lab 5: Text Representation

## Student Information

**Name:** Muhannad Almutlaq  
**ID:** 2240006060

### Experimentation & Key Takeaways

* **Numerical Text Conversion:** Explored fundamental text representation techniques to convert unstructured text into machine-readable numerical vectors that can be understood by machine learning models.
* **TF-IDF Vectorization:** Utilized `TfidfVectorizer` to quantify the importance of words across a document corpus, balancing Term Frequency (TF) with Inverse Document Frequency (IDF) to discount overly common words.
* **Document Similarity Mapping:** Applied Cosine Similarity metrics to measure the semantic closeness between different documents by calculating the dot product divided by the magnitudes of their vectors.
* **Word Embeddings (Word2Vec):** Investigated neural network-based embeddings using the `gensim` library, specifically utilizing the Skip-Gram architecture to capture deep inter-word semantics and contextual relationships.
* **Data Preprocessing Pipeline:** Implemented text cleaning procedures using Regular Expressions (`re`) to remove digits and punctuation, convert text to lowercase, and tokenize sentences using NLTK before feeding them into embedding models.
* **Semantic Word Analysis:** Leveraged a custom-trained Word2Vec model on the Simpsons dataset to perform semantic tasks, such as finding highly correlated words and characters using the `wv.most_similar()` method.
* **Contextual Outlier Detection:** Evaluated the spatial grouping capabilities of the learned embeddings by identifying semantic outliers in specific lists of words using the `wv.doesnt_match()` method.
