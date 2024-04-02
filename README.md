# Evolution-of-criminal-language
Analysis of the QANON dataset to be able to understand how criminal language has evolved

## Introduction
In analyzing the QANON dataset, several tasks were undertaken to extract meaningful insights and build a machine learning model. The dataset comprised both structured and textual data, requiring distinct processing strategies.

### Technologies Used
- Natural Language Toolkit (NLTK)
- SpaCy
- Gensim
- Scikit-learn
- TensorFlow

### Structured Data Analysis
- Analyzed columns such as author, source, date, link, and image reference.
- Feature engineering was applied to columns like date and source to extract valuable information about language evolution on web platforms.
- Uninformative columns like link and author were eliminated.

### Textual Data Processing
- Text cleaning involved removing HTML tags, punctuation, and links.
- NLP techniques such as part-of-speech tagging, lemmatization, stemming, and stopword removal were applied using NLTK and SpaCy to create meaningful text representations.
- Integration of commonly used terms, slang, and proper names could enhance the NLP pipeline further.

### Topic Modeling
- Leveraged Latent Dirichlet Allocation (LDA) to automatically discover the 5 most relevant topics in the entire corpus.
- Each record was automatically labeled using the 20 most recurrent words for each topic.
- Adjustments to the number of topics and words allowed for flexibility in text fragmentation.
- Word embedding and tf-idf were used to represent text for LDA.
- Significant words for each topic were extracted and used to label records into classes.

### Machine Learning Approach
- Utilized SVC, Random Forest, and LSTM models for classification.
- SVC with linear kernel demonstrated efficiency with word embeddings, yielding around 0.8 AUC.
- LSTM model showed poor results, suggesting potential for improvement with better preprocessing and layer selection.

## Conclusion
The comprehensive analysis and machine learning approach provided insights into the QANON dataset, offering opportunities for further refinement and exploration.
