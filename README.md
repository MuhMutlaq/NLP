# Lab 11: Attention Mechanisms

## Student Information

**Name:** Muhannad Almutlaq  
**ID:** 2240006060

### Experimentation & Key Takeaways

- **Attention Fundamentals:** Explored Attention mechanisms to allow the neural network to dynamically focus more on relevant information within an input sequence when making a prediction.
- **Data Processing & Preparation:** Preprocessed the `Lab_11_QnA_Dataset.csv` dataset by converting question text to lowercase and mapping words to numeric tokens using `Tokenizer`. Standardized the sequence lengths using `pad_sequences(padding="post")` and converted both the input sequences and target answer IDs into PyTorch tensors.
- **Model Architecture & Implementation:** Constructed a custom PyTorch model featuring an `nn.Embedding` layer to transform tokenized integers into vectors and an `nn.RNN` to process the sequence. Implemented an Attention mechanism using `nn.Linear` and `torch.softmax` to calculate weight distributions across the words, passing the weighted context to a fully connected output layer to choose the correct answer.
- **Compilation, Training & Optimization:** Optimized the network using the `Adam` optimizer with a learning rate of 0.01. Executed a training loop for 50 epochs, utilizing PyTorch's `cross_entropy` loss function to update parameters via backpropagation.
- **Inference Pipeline & Evaluation:** Extracted attention weights using `torch.no_grad()` and visualized them with bar charts to identify the highest-weighted words for given questions. Observed that lightweight RNN architectures with attention on limited datasets do not always map to abstract human logic; they often rely on syntactical anchors or dataset-specific artifacts (like stop-words) as shortcuts to minimize classification loss.
