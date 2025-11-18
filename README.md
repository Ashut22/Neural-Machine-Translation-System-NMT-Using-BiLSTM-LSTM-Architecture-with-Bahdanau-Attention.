# Neural Machine Translation: English→Hindi & English→Bengali

This project implements a Seq2Seq Neural Machine Translation system using a Bidirectional LSTM encoder, LSTM decoder, and Bahdanau Attention. It supports both English–Hindi and English–Bengali translation tasks.

## Overview
The system trains on parallel corpora and performs end-to-end translation through preprocessing, vocabulary building, sequence padding, encoder–decoder modeling, and greedy decoding at inference time.

## Key Features
- Text preprocessing: lowercasing, digit/punctuation removal, NLTK tokenization  
- Vocabulary creation with `<PAD>`, `<SOS>`, `<EOS>` tokens  
- Encoder: 3-layer BiLSTM with 128-dimensional embeddings  
- Decoder: 3-layer LSTM with Bahdanau Attention  
- Teacher forcing training strategy with gradient clipping  
- Greedy decoding for translation generation  
- Support for both English–Hindi and English–Bengali datasets

## Training Configuration
- Sequence length: 75  
- Hidden size: 128  
- Learning rate: 1e-3 (Adam optimizer)  
- Loss function: Negative Log-Likelihood  
- Teacher Forcing Ratio: 1.0  

## Results
- CHRF++: 0.30  
- ROUGE: 0.358  
- BLEU: 0.102  
These scores were obtained on the final evaluation set after training on both language pairs.

## Files
- `train_data1.json` – Training dataset  
- `test_data1_final.json` – Test dataset  
- Model training and inference code inside the notebook  
- Generated translations exported as CSV files

## How to Run
1. Place the training and test JSON files in the expected directory.  
2. Execute the notebook cell-by-cell to preprocess data, train models, and generate outputs.  
3. Final translations are saved as CSV files for submission or further evaluation.
