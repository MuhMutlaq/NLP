# Lab 13: Information Retrieval for RAG

## Student Information

**Name:** Muhannad Almutlaq  
**ID:** 2240006060

### Experimentation & Key Takeaways

- **Information Retrieval & RAG Foundations:** Built a sparse retrieval pipeline to search and rank relevant course note passages from user queries, supplying supporting context for Retrieval-Augmented Generation (RAG) workflows.
- **TF-IDF Vectorization:** Utilized `TfidfVectorizer` with English stop-word removal to transform raw document text into numerical sparse feature matrices based on Term Frequency (TF) and Inverse Document Frequency (IDF) scores.
- **Cosine Similarity & Ranking:** Calculated cosine similarity scores between transformed query vectors and document vectors to measure numerical alignment, sorting the results to extract top-$k$ relevant documents.
- **Search Filtering & Limitations:** Developed `search_filtered()` to discard zero-score results and demonstrated the exact-keyword matching limitation of sparse TF-IDF retrieval (e.g., failing on un-stemmed plural forms or non-overlapping synonyms).
- **Corpus Updating & Vocabulary Expansion:** Analyzed why appending new text requires re-executing `vectorizer.fit_transform(documents)` to update the vocabulary index, recalculate IDF weights across updated total documents ($N$), and maintain matrix dimensional alignment.
