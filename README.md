# Text_generation
We implemneted several methods to generate text automatically. The size of the datasets these methods can handle varies. All these methods use the same way to deal with the sampling during new text generation. That is, a parameter 'temperature' is used to control the randomness. Without this parameter, the same input always lead to the generation of same text. A large value of this parameter leads to more randomness.  

# 1. One-hot encoding and LSTM
This is a char RNN. Each char of the input is one-hot encoding, which leads to a large sparse input matrix. Thus, it can only deal with small dataset.

