# DEEP_LEARNING_PROJECT
# DEEP LEARNING PROJECT  
## Abstractive Text Summarization using Seq2Seq with Attention


##  Objective
The objective of this project is to build an **abstractive text summarization system** using **deep learning**. The model automatically generates a concise summary from a long news article while preserving the important information and overall meaning of the text.


##  Dataset
The project uses a **news article dataset** consisting of:
- `article` : Full news text  
- `highlights` : Human-written summary  

The dataset is divided into:
- Training set  
- Validation set  
- Test set  

The data is loaded from Google Drive and processed using Pandas.


##  Methodology

### 1. Data Preprocessing
- Converted text to lowercase  
- Removed special characters, punctuation, and extra spaces  
- Tokenized the text  
- Added special start (`sostok`) and end (`eostok`) tokens to summaries  
- Applied padding to ensure fixed-length sequences  


### 2. Model Architecture
The project uses a **Sequence-to-Sequence (Seq2Seq)** architecture with **LSTM** networks.

#### Encoder
- Embedding layer  
- LSTM layer to encode the input article into context vectors  

#### Decoder
- Embedding layer  
- LSTM layer to generate summaries  
- Attention mechanism to focus on relevant parts of the input  


### 3. Attention Mechanisms Used
Two attention techniques are implemented and compared:

- **Bahdanau Attention** (Additive Attention)  
- **Luong Attention** (Multiplicative Attention)  

Both models are trained separately to analyze performance differences.


### 4. Model Training
- Optimizer: Adam  
- Loss function: Sparse Categorical Crossentropy  
- Batch size: 32  
- Epochs: 5  
- Training and validation loss are plotted for analysis  


##  Evaluation

The models are evaluated using:
- **ROUGE-1**
- **ROUGE-2**
- **ROUGE-L**

A **heatmap visualization** is used to compare ROUGE scores for Bahdanau and Luong attention models.


## 📈 Results
- Training and validation loss decrease gradually, showing proper learning  
- Both attention mechanisms generate abstractive summaries  
- ROUGE scores are calculated and compared visually  
- Bahdanau and Luong attention show similar performance on the given dataset  

---

##  Technologies Used
- Python  
- TensorFlow / Keras  
- NumPy  
- Pandas  
- Matplotlib  
- Seaborn  
- Jupyter Notebook  
- Google Colab  



##  Conclusion
This project demonstrates the practical implementation of **abstractive text summarization** using **deep learning and attention mechanisms**. It highlights how attention improves the quality of generated summaries by allowing the model to focus on important parts of the input text.


##  Future Scope
- Increase training epochs for better accuracy  
- Use pretrained embeddings (GloVe, Word2Vec)  
- Apply Transformer-based models (BERT, T5)  
- Improve evaluation scores with larger datasets  



