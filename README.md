# Lab 7: Large Language Models (LLMs)

## Student Information

**Name:** Muhannad Almutlaq  
**ID:** 2240006060

### Experimentation & Key Takeaways

- **Transformer Architecture Mapping:** Categorized core NLP tasks into their ideal architectures, matching sentiment classification and Named Entity Recognition to Encoder-only models, translation and summarization to Encoder-decoder models, and open-ended text generation to Decoder-only models.
- **Encoder-Only Sentiment Classification:** Evaluated the `distilbert-base-uncased-finetuned-sst-2-english` pipeline to classify the sentiment of multiple test sentences, successfully capturing both positive and negative contextual meanings.
- **Encoder-Decoder Text Processing:** Leveraged the `google/flan-t5-small` sequence-to-sequence model to process instructions, specifically utilizing its text-to-text generation capabilities to translate English to French and summarize short text paragraphs.
- **Decoder-Only Next-Token Generation:** Used the `distilgpt2` pipeline to demonstrate autoregressive text generation. Concluded that decoder-only models are perfectly suited for conversational agents like ChatGPT because they continuously predict subsequent sequence tokens based on preceding conversational context.
- **Temperature and Sampling Variance:** Explored the removal of `set_seed(42)` to observe generation stochasticity. Confirmed that probability-based sampling introduces non-deterministic token selection, causing the exact same prompt to yield completely diverse outputs compared to deterministic seed-locked generation.
