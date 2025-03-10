This project focuses on automatically grading short Arabic answers using advanced Natural Language Processing (NLP) techniques and sequence models such as LSTM.

# Dataset
This project uses The ARabic Dataset for Automatic Short Answer Grading Evaluation 
This dataset is intended for exploring research in the field of Automatic Short Answer Grading (ASAG).
[Dataset Link](https://github.com/leilaouahrani/AR-ASAG-Dataset)

# libraries used
- numpy  
- pandas  
- matplotlib  
- seaborn  
- nltk  
- scikit-learn  
- keras  
- tensorflow 

# Text Preprocessing
Arabic text is cleaned, normalized, and tokenized to handle linguistic variations such as diacritics, punctuation, and synonyms. Using `Tokenizer`, text is converted into sequences of tokens (integers), and then `pad_sequences` is applied to ensure all input sequences have a uniform length, which is essential for feeding data into model.

# texts_to_sequences & Word Embedding
After preprocessing the text, the `Tokenizer` is used to convert words into numerical sequences using the `texts_to_sequences` method. These sequences are then padded to ensure consistent input length. The resulting sequences are passed through a word embedding layer (`Word2Vec`) allowing the model to represent each word in a dense vector space that captures semantic and contextual relationships. This encoding forms the foundation for LSTM sequence model input.

# Model Architecture
| model  | optimizer | metrics |loss function  |accuracy score|
| -------- | -------- | -------- | -------- |-------- |
|  LSTM    | adam   |accuracy score    |categorical crossentropy    |85%

# testing sample
|answer| rate |
| -------- | -------- |
| 1    | B   |
|2    | A| 
| 3   | D   |
| a  | B   |
