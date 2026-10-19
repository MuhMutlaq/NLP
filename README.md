# Lab 9: Named Entity Recognition (NER)

## Student Information

**Name:** Muhannad Almutlaq  
**ID:** 2240006060

### Experimentation & Key Takeaways

- **Named Entity Recognition Fundamentals:** Explored NER as a core two-step NLP process that detects entities within unstructured text and classifies them into predefined categories such as people (`PERSON`), organizations (`ORG`), geopolitical locations (`GPE`), dates (`DATE`), and products (`PRODUCT`). Determined its critical role in downstream applications including information retrieval, question answering, and sentiment analysis.
- **Pre-Trained Entity Extraction with spaCy:** Utilized spaCy's `en_core_web_sm` pipeline to automatically parse text and extract named entities via `doc.ents`. Extracted token-level span attributes—including entity text (`ent.text`), category labels (`ent.label_`), and token start/end indices (`ent.start`, `ent.end`)—while leveraging `spacy.explain()` to translate shorthand labels into human-readable descriptions.
- **Manual Entity Span Modification & Alignment:** Addressed limitations in pre-trained models where domain-specific or unconventionally formatted entities (such as `'Bcd LLC'` enclosed in quotes) were overlooked. Used character-offset mapping and `offsets_to_biluo_tags` to verify token alignment across Begin, Inside, Last, Unit, and Outside (`BILUO`) tags, and programmatically appended missing entity spans to `doc.ents` to ensure accurate frequency counts for `PERSON` and `ORG` categories.
- **Custom NER Model Training & Persistence:** Built and trained a custom NER pipeline from a blank English model (`spacy.blank("en")`) to recognize specialized entity spans. Structured training data using character offsets and `Example.from_dict()`, optimized model weights over 20 training iterations using `nlp.update()` with dropout regularization, and serialized the trained pipeline to disk (`custom_ner_model`) for reloading and inference.
- **Entity Visualization with displaCy:** Rendered inline visual highlights of recognized entities within Jupyter notebooks using `displacy.render(doc, style="ent")`. Used color-coded span markers to visually validate both pre-trained and custom-trained NER model predictions directly against the source text.
