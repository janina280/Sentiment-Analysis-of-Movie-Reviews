# Sentiment-Analysis-of-Movie-Reviews

## 📌 Project Overview
This project implements a **Sentiment Analysis system for movie reviews** using **Deep Learning** techniques.  
The goal is to classify IMDB movie reviews as **positive** or **negative** by applying and comparing multiple **Recurrent Neural Network (RNN)** architectures.

---

## 🎯 Objectives
- Build a sentiment analysis model for movie reviews
- Apply text preprocessing techniques for NLP
- Compare the performance of Simple RNN, LSTM, GRU, and Bidirectional LSTM
- Evaluate models using Accuracy and F1-score
- Demonstrate predictions on unseen reviews

---

## 📂 Dataset
- **Dataset name:** IMDB Dataset of 50K Movie Reviews  
- **Source:** Kaggle  
  https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews  
- **Number of samples:** 50,000  
- **Classes:** Positive / Negative (balanced dataset)

---

## 🧠 Models Used
- **Simple RNN** – baseline recurrent model
- **LSTM (Long Short-Term Memory)** – captures long-term dependencies
- **GRU (Gated Recurrent Unit)** – efficient alternative to LSTM
- **Bidirectional LSTM** – captures context from both directions

---

## 🔄 Data Preprocessing
The following preprocessing steps were applied:
- Conversion to lowercase
- Removal of HTML tags
- Removal of special characters
- Tokenization using Keras Tokenizer
- Padding sequences to a fixed length

**Key parameters:**
- Vocabulary size: **20,000**
- Maximum sequence length: **200**

---

## ⚙️ Training Configuration
- Batch size: **64**
- Epochs: **up to 7**
- Optimizer: **Adam**
- Loss function: **Binary Cross-Entropy**
- Regularization techniques:
  - EarlyStopping (patience = 2)
  - Dropout layers

---

## 📊 Evaluation Metrics
The models were evaluated using:
- **Accuracy**
- **F1-score**
- **Confusion Matrix**
- Training and validation curves (accuracy & loss)

---

## 📈 Results

| Model | Accuracy | F1-score |
|------|----------|----------|
| Simple RNN | 0.5108 | 0.5956 |
| LSTM | 0.8674 | 0.8704 |
| GRU | 0.8724 | 0.8698 |
| Bidirectional LSTM | 0.8612 | 0.8615 |

---

## 🧪 Observations
Simple RNN performs poorly due to the vanishing gradient problem.
LSTM and GRU achieve the best balance between performance and complexity.
GRU slightly outperforms LSTM while being computationally more efficient.
Bidirectional LSTM tends to overfit without additional regularization.
Early stopping significantly improves model generalization.

##🚀 Future Improvements
Use pre-trained word embeddings (GloVe, Word2Vec)
Experiment with Transformer-based models (e.g., BERT)
Apply text data augmentation techniques
Perform cross-validation for more robust evaluation

## 🛠 Technologies Used
Python
TensorFlow 
Scikit-learn
Pandas, NumPy

## 🔮 Sample Predictions
After training, the best-performing model was used to predict sentiment on manually written reviews.

Example:
```text
"This movie was absolutely fantastic! Great acting and amazing plot."
→ Predicted sentiment: Positive (high confidence)
