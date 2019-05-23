# Text_generation
We implemneted several methods to generate text automatically. The size of the datasets these methods can handle varies. All these methods use the same way to deal with the sampling during new text generation. That is, a parameter 'temperature' is used to control the randomness. Without this parameter, the same input always lead to the generation of same text. A large value of this parameter leads to more randomness.  

# 1. One-hot encoding and LSTM
This is a char RNN. Each char of the input is one-hot encoding, which leads to a large sparse input matrix. Thus, it can only deal with small dataset.

# 2. Word embedding and bidirectional GRU
This is based on the word. For chinese, we use the jieba library to get the word. The input for a sentence is just a list of indices which indicates the position of each word. Then an embedding layer, and two layers of bidirectional GRU are added. Compared with method 1, this can handle large dataset.

# 3. Embedding and GRU and Conv1D
Often, Convolution has been a popluar way to handle text if the word has been transformed to embeddings. Here, we combine both GRU and Conv1D. Another thing to mention is that motivated by bidirectional GRU, we also use the context after target word to help predict.
