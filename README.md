# Lab 12: Transformers

## Student Information

**Name:** Muhannad Almutlaq  
**ID:** 2240006060

### Experimentation & Key Takeaways

- **Transformer Fundamentals:** Explored Transformer deep learning architectures that rely on self-attention mechanisms to process text sequences, serving as the foundation for modern NLP models (like BERT, GPT, and T5) and replacing earlier RNN/LSTM approaches.
- **Model Loading & Inspection:** Utilized the Hugging Face `transformers` library to load pretrained models (`distilbert-base-uncased-finetuned-sst-2-english` and `bert-base-uncased`), analyzing internal configurations such as the number of hidden layers, attention heads per layer, and total hidden dimensions.
- **Tokenization & Embeddings:** Processed raw text using `AutoTokenizer` to convert sequences into token IDs and contextual embeddings, identifying structural tokens like `[CLS]` (start) and `[SEP]` (end).
- **Self-Attention Mechanism:** Extracted and visualized attention matrices from specific layers and heads (e.g., the 3rd layer and 2nd head) to understand how rows (target query tokens) and columns (source key tokens) calculate weighted focus distributions that always sum to 1.0 score.
- **Classification & Inference:** Implemented an inference pipeline that passes tokenized inputs through the classification head to output logits, subsequently applying the `torch.softmax` function to convert these raw scores into final prediction probabilities and confidence percentages.
