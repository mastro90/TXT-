# Tweets Toxicity Analysis (TXA)

## Project Goal
The project aims to analyze a collection of tweets in order to:  
- Determine whether a tweet is toxic or non-toxic.  
- Identify the main categories of toxicity present in online language.  
- Extend the analysis to detect emotions expressed in tweets.

---

## General Workflow
1. Data Understanding & Preparation  
2. Topic Modeling  
3. Simple Classifiers  
4. Neural Network Classifiers  
5. BERT (Binary and Multiclass Classification)  
6. Emotion Detection  

---

## Data Understanding & Preparation
- Dataset analysis and definition of key variables.  
- Text cleaning: removal of emoticons, punctuation, links, mentions, numbers, and special characters.  
- Text normalization: lowercase conversion and expansion of contracted forms.  
- Stopwords removal.  
- Tokenization and lemmatization for further linguistic and machine learning analyses.

---

## Topic Modeling
- Application of unsupervised modeling techniques (LDA) to identify main types of toxicity.  
- Dataset preparation and document-term matrix construction.  
- Empirical interpretation of the resulting topics and semantic categorization of content.

---

## Simple Classifiers
- Implementation of a supervised classification pipeline including:
  - CountVectorizer  
  - SelectKBest (chi²)  
  - TfidfTransformer  
  - Multiple classifiers (Naive Bayes, KNN, Decision Tree, SVM)  
- Model optimization performed through GridSearchCV and RandomizedSearchCV.

---

## Neural Network Classifiers
- Development of sequential and recurrent neural networks (LSTM).  
- Use of embedding layers with:
  - Random weight matrices  
  - Pre-trained embedding matrices (GloVe)  
- Model training with binary cross-entropy loss and optimization through backpropagation.

---

## BERT – Binary Classification
- Use of a pre-trained BERT model for binary tweet classification.  
- Data preprocessing steps:
  - Tokenization and insertion of special tokens [CLS] and [SEP]  
  - Definition of maximum sequence length  
  - Creation of attention masks to distinguish real tokens from padding  
- Conversion of data into tensors and training using DataLoader.  
- Addition of a linear layer on top of BERT for final classification.

---

## Emotion Detection
- Application of transfer learning using the EmoRoBERTa model, based on RoBERTa and trained on emotion-labeled datasets (GoEmotions).  
- Association of one or more emotions to each tweet at sentence level.  
- Integration of emotion information into the dataset for subsequent analyses.

---

## BERT Multiclass
- Extension of BERT for multiclass classification based on detected emotions.  
- Reuse of the same preprocessing and training procedures from the binary BERT model.  
- Evaluation of performance across multiple emotional labels.


