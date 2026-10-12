# Lab 8: Part-of-Speech (POS) Tagging

## Student Information

**Name:** Muhannad Almutlaq  
**ID:** 2240006060

### Experimentation & Key Takeaways

- **Part-of-Speech Tagging Fundamentals:** Explored POS tagging as a foundational NLP technique that categorizes words based on their definition and sentence context. Determined that POS tagging is critical for downstream applications including Named Entity Recognition (NER), relation extraction, grammar correction, and sentiment analysis.
- **NLTK Word-Level POS Tagging:** Implemented NLTK's `pos_tag` method in conjunction with `word_tokenize` to automatically assign morphological tags to individual words within parsed sentences. Demonstrated how this allows for targeted information retrieval, such as extracting adjectives (`JJ`) to analyze sentiment.
- **spaCy Linguistic Analysis (Coarse vs. Fine-Grained):** Processed textual data utilizing the `en_core_web_sm` pipeline to extract both coarse-grained generic grammatical categories (e.g., `VERB`, `PROPN`, `NOUN`) and fine-grained, morphology-specific tags (e.g., `VBP`, `NNP`, `NNS`). Used `spacy.explain()` to translate abstract tags into readable morphological descriptions.
- **Contextual & Morphological Disambiguation:** Validated spaCy's machine learning capability to dynamically determine POS based on surrounding sentence context rather than static definitions. Correctly differentiated identical vocabulary such as "google" acting as a proper noun (`PROPN`) versus a base action verb (`VERB`), and "table" acting as a physical object noun (`NOUN`) versus a motion submission verb (`VERB`).
- **Syntactic Dependency & POS Visualization:** Rendered complex grammatical relationships visually within Jupyter notebooks using `displacy.render`, mapping token dependencies, directional arcs, and POS tags to analyze syntax structures visually.
