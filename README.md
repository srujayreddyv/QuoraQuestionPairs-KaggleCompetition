# Quora Question Pairs- Kaggle Competition
This repository contains code for a project aimed at determining the similarity between questions from the Quora dataset using Natural Language Processing (NLP) and deep learning techniques. The project involves data preprocessing, text normalization, vector representation, and building a neural network model.

## Dataset
The dataset used in this project is the Quora Question Pairs dataset, which contains pairs of questions and a binary label indicating whether they are duplicate questions.

## Data Preprocessing
The data preprocessing pipeline includes several steps to clean and normalize the text data:
1. Lower Casing Questions: All text is converted to lowercase to ensure consistency.
2. Replacing Symbols and Short Forms: Various symbols, currency signs, and short forms are replaced with their full word equivalents.
3. Converting Numbers to Words: Numeric values are converted to their word representations. For example, "5" becomes "five."
4. Stemming: Text is processed using the Snowball Stemmer, which reduces words to their base form.
5. Removing Stopwords: Common stopwords are removed from the text, as they do not contribute significantly to determining question similarity.

## Vector Representation
The text data is transformed into vector representations using pre-trained GloVe embeddings. These embeddings capture semantic and syntactic meaning, which is essential for our similarity classification task.

## Neural Architecture
The Siamese neural network architecture is used for this task. The model uses shared embedding layers for both input questions and employs Bidirectional LSTMs to capture contextual information. Attention mechanisms are applied to identify the most relevant parts of the text. The model is trained to predict question similarity.

## Testing
The model is trained and tested on the Quora Question Pairs dataset, and its performance is evaluated using evaluation metrics such as accuracy, precision, recall, and F1-score. The project aims to provide an accurate measure of question similarity, which can be useful in various natural language processing applications.
