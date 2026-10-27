# Lab 10: Introduction to Machine Translation (MT)

## Student Information

**Name:** Muhannad Almutlaq  
**ID:** 2240006060

### Experimentation & Key Takeaways

- **Neural Machine Translation (NMT) Fundamentals:** Explored NMT as a data-driven subfield of AI that maps source languages to target languages using large neural networks, eliminating the need for manual rule definitions. Examined primary MT challenges, including semantic ambiguity, idiomatic expressions, and constraints of low-resource languages, alongside real-world applications in global e-commerce and cross-cultural communication.
- **Text Tokenization & Sequence Padding:** Utilized TensorFlow's `Tokenizer` to preprocess bilingual datasets (English and French). Converted raw text into integer arrays using `texts_to_sequences()` and extracted vocabulary mappings via `word_index`. Standardized input dimensions for the neural network by appending zeros to sequence structures using `pad_sequences()`.
- **Encoder-Decoder LSTM Architecture:** Constructed a Sequence-to-Sequence (Seq2Seq) model leveraging Long Short-Term Memory (`LSTM`) networks. Implemented an `Embedding` layer to transform tokenized integers into dense continuous vectors, an Encoder LSTM to encapsulate the source text's context, and a `RepeatVector` layer to bridge the contextual state to the target sentence length for the Decoder LSTM.
- **Model Compilation & Training:** Optimized the neural network using the `adam` optimizer and `sparse_categorical_crossentropy` loss function. Executed training iterations (`model.fit()`) while formatting the final layer with `TimeDistributed(Dense(vocab_size, activation='softmax'))` to generate a probability distribution over the target vocabulary at each individual timestep.
- **Inference Pipeline & Sequence Decoding:** Developed a custom function for translating unseen sentences. Processed incoming strings through the English tokenizer and padding mechanism, passed them to `model.predict()` to retrieve multi-dimensional probability arrays, and extracted the highest-probability word indices using `np.argmax(..., axis= -1)`. Finally, reconstructed the translated text utilizing the French tokenizer's `sequences_to_texts()` method.
