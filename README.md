Quora Question Answering Analysis
This repository contains an analysis and comparison of different models for the task of question answering using the Quora Question Answer Dataset (Quora-QuAD). We explore the performance of BERT, GPT-2, and T5 models on a subset of this dataset.

Dataset
The dataset used is the Quora Question Answer Dataset (Quora-QuAD). It consists of question-answer pairs extracted from Quora.

Preprocessing
  Text Cleaning
  Convert text to lowercase
  Remove newlines and non-word characters
  Remove extra spaces
Tokenization and Stopword Removal
  Tokenize the text into words
  Remove English stopwords
Stemming and Lemmatization
  Apply PorterStemmer for stemming
  Apply WordNetLemmatizer for lemmatization
Model Loading and Prediction
  Models Used
    BERT: bert-large-uncased-whole-word-masking-finetuned-squad
    GPT-2: gpt2
    T5: t5-small
Prediction Functions
  BERT: For question answering using context
  GPT-2: For text generation based on the question
  T5: For question answering using context
Evaluation Metrics
  Metrics Used
    ROUGE: Measures overlap between predicted and reference text
    BLEU: Measures n-gram precision with brevity penalty
    F1-Score: Measures token overlap with precision and recall
Results Summary
  BERT:
    ROUGE-1: 0.198, ROUGE-2: 0.107, ROUGE-L: 0.192
    BLEU: Very low due to brevity penalty
    F1: 0.197
  GPT-2:
    ROUGE-1: 0.160, ROUGE-2: 0.039, ROUGE-L: 0.110
    BLEU: Slightly better than BERT but still low
    F1: 0.156
  T5:
    ROUGE-1: 0.415, ROUGE-2: 0.233, ROUGE-L: 0.416
    BLEU: Very low due to brevity penalty
    F1: 0.416

Visualizations
  Data Distribution
    Distribution of question and answer lengths
  Feature Importance
    Top 20 important features for answer length prediction using a Random Forest classifier
  Model Performance
    ROUGE scores comparison
    F1 scores comparison



Improvements Based on Findings
1) Continuous Learning:

    Problem: Over time, models may become outdated and less effective.
    Solution: Introduce a feedback system where users can provide input and corrections. Use this feedback to regularly update and retrain the models, ensuring they stay current and improve continuously.

2) Explainability:

    Problem: It can be difficult to understand why a model made a particular decision.
    Solution: Use tools that show how the model's attention is focused on different parts of the input. This helps to make the model’s decision-making process clearer and more transparent.

3) Hybrid Models:

     Problem: Each model has unique strengths and drawbacks.
     Solution: Combine models to take advantage of their distinct characteristics. For example, utilize BERT to extract crucial information, T5 to polish and refine the responses, and GPT-2 to provide originality and variation.
