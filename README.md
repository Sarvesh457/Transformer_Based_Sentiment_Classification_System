# Transformer_Based_Sentiment_Classification_System
Transformer-Based Sentiment Analysis Using TensorFlow
Project Overview

This project demonstrates the implementation of a Transformer-based Sentiment Analysis Model using TensorFlow and Keras. The model classifies textual sentences as Positive or Negative by leveraging key Transformer concepts such as Token Embedding, Positional Encoding, Multi-Head Self-Attention, and Transformer Encoder Blocks.

The project is designed as an educational implementation that explains the internal working of Transformers step-by-step while building a complete sentiment classification pipeline.

Features
Custom text preprocessing using TensorFlow TextVectorization
Tokenization and sequence padding
Learnable Token Embeddings
Learnable Positional Embeddings
Multi-Head Self-Attention Mechanism
Custom Transformer Encoder Layer
Residual Connections and Layer Normalization
Binary Sentiment Classification
End-to-End Training and Prediction Pipeline
Educational visualization of attention scores and embeddings

# Project Architecture
Input Sentences
        │
        ▼
Text Vectorization
(Tokenization + Padding)
        │
        ▼
Token Embedding
        │
        ▼
Positional Embedding
        │
        ▼
Combined Embedding
        │
        ▼
Multi-Head Self Attention
        │
        ▼
Feed Forward Network
        │
        ▼
Layer Normalization
        │
        ▼
Global Average Pooling
        │
        ▼
Dense Layer
        │
        ▼
Sigmoid Output Layer
        │
        ▼
Positive / Negative Prediction
Technologies Used
Python 3.x
TensorFlow 2.x
Keras
NumPy
Dataset

The project uses a manually created dataset consisting of:

Positive Sentences
Negative Sentences

Example Positive Sentences :

this course is very good
i like this session
teaching is very clear
teacher explained very well

Example Negative Sentences 
:
this course is boring
session was confusing
teacher did not explain well
i am confused

Labels
1 → Positive
0 → Negative

# Transformer Components Implemented

1. Text Vectorization
Converts text into numerical token IDs.

Example:

this course is very good
↓
[2, 5, 3, 9, 15]

2. Token Embedding
Converts token IDs into dense vector representations.

Token ID
   ↓
Embedding Vector

3. Positional Embedding
Provides position information to the Transformer since Transformers process all words simultaneously.

Word Position
   ↓
Position Vector

4. Multi-Head Self-Attention
Allows each word to attend to other words within the same sentence.

Example:
teacher explained very well
The word "explained" can focus on:

teacher
very
well

to understand context.

5. Transformer Encoder Block
The encoder block contains:

Multi-Head Attention
MultiHeadAttention()
Feed Forward Neural Network
Dense(ReLU)
Dense()
Residual Connections
Output = Input + Attention
Layer Normalization
LayerNormalization()
Dropout
Dropout(0.1)
Model Configuration
Parameter	Value
Vocabulary Size	1000
Sequence Length	8
Embedding Dimension	16
Number of Attention Heads	2
Feed Forward Dimension	32
Dropout Rate	0.1
Output Activation	Sigmoid
Loss Function	Binary Crossentropy
Optimizer	Adam
Installation

Clone Repository : 
git clone https://github.com/your-username/transformer-sentiment-analysis.git

cd transformer-sentiment-analysis
Install Dependencies
pip install tensorflow numpy
Running the Project

Execute the Python script:
python transformer_sentiment_analysis.py
Training

The model is trained using:

model.fit(
    x_data,
    labels,
    epochs=80,
    batch_size=2
)

During training, the model learns patterns associated with positive and negative sentiments.

Evaluation

The model evaluates performance using:

loss, accuracy = model.evaluate(
    x_data,
    labels
)

Metrics:

Training Loss
Training Accuracy
Sample Predictions

Input:

this session is good

Output:

Positive
Score: 0.95

Input:

i am confused

Output:
Negative
Score: 0.08
Learning Outcomes

This project helps understand:

Natural Language Processing (NLP)
Transformer Architecture
Self-Attention Mechanism
Multi-Head Attention
Positional Encoding
Deep Learning for Text Classification
TensorFlow Custom Layers
Sentiment Analysis
Future Enhancements
Larger real-world datasets
Pre-trained Transformer models (BERT, RoBERTa, DistilBERT)
Attention visualization dashboard
Multi-class sentiment classification
Real-time sentiment prediction web application
Integration with social media sentiment analysis
Author

Sarvesh Mahajan

Computer Science Student

Project Title: Transformer-Based Sentiment Analysis Using TensorFlow

License

This project is developed for educational and academic purposes. Feel free to use and modify it for learning and research activities.
