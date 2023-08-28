# Topic Modeling - Customer Complaints - BERTopic LSI LDA

Notebooks:
1. https://www.kaggle.com/code/shirshmall/topic-modeling-bertopic-customer-complaints/notebook
2. https://www.kaggle.com/code/shirshmall/topic-modelling-lda-lsi-custom-complaints/notebook

Dataset: https://www.kaggle.com/datasets/utkarshx27/consumer-complaint

# Topic Modelling on Customer Complaints

## Introduction
This project revolves around the concept of topic modeling applied to customer complaints using a dataset known as the Consumer Complaint Database of financial products and services. The dataset comprises consumer complaints about various financial products and services, which are published after companies respond or after a 15-day period, depending on the circumstances. The main objective of this project is to cluster these consumer complaints into topics using techniques like Latent Semantic Analysis (LSA), Latent Dirichlet Allocation (LDA), and BERTopic.

## Dataset
The Consumer Complaint Database contains a collection of complaints about consumer financial products and services. The complaints are associated with various financial aspects and products. The key column "issue" is utilized for topic modeling, as it describes the primary issue or problem mentioned in the consumer complaint.

## Techniques and Tasks
The project employs three distinct techniques for topic modeling: Latent Semantic Analysis (LSA), Latent Dirichlet Allocation (LDA), and BERTopic. The primary aim is to cluster consumer complaints based on the underlying topics present in the dataset.

### Implementation Steps for LDA and LSI
1. **Data Cleaning**: The initial step involves text preprocessing, including lowercase conversion, punctuation removal, elimination of words with two or more "x" letters, removal of numbers and words with numbers, removal of stopwords, tokenization, and lemmatization using the Spacy library.
2. **Creating Document Term Matrix**: Gensim is employed to create a Document Term Matrix, involving the creation of a dictionary and calculation of Term Document Frequency.
3. **LDA/LSI Implementation**: Gensim's LDA/LSI models are implemented on the cleaned and processed data.
4. **Evaluation**: The Coherence Score is computed to evaluate the quality of the generated topics.
5. **Result of LDA**: The obtained Coherence Score is 0.55.
6. **Hyperparameter Tuning**: A function is created for training the LDA model and computing the Coherence Score. Hyperparameters such as Topics range, Alpha parameter, and Beta parameter are tuned.

### Implementation Steps for BERTopic
1. **Data Cleaning and Preprocessing**: Similar preprocessing steps are applied, including data cleaning and text normalization.
2. **Extracting Embeddings**: Sentence Transformer is employed to extract embeddings from the preprocessed text.
3. **Dimensionality Reduction**: UMap is used to reduce the dimensionality of the extracted embeddings.
4. **Clustering**: The HDBSCAN model is utilized to cluster the reduced embeddings.
5. **Tokenization and Topic Representation**: Topics are tokenized, and a topic representation is created using CountVectorizer and ClassTfidfTransformer.
6. **Training**: Features are extracted from the BERTopic model, and evaluation is performed using u_mass and c_v scores.
7. **Result**: The obtained u_mass score is -0.266, and the cv_score is 0.856.
8. **Visualizing Topics**: Topics are visualized using bar charts and an Intertopic Distance Map.

## Conclusion
The project successfully applies LSA, LDA, and BERTopic techniques to cluster consumer complaints into topics based on the main issues described in the complaints. By employing various preprocessing steps and advanced text modeling techniques, the project provides insights into the underlying patterns in customer complaints, which can aid in better understanding customer feedback and improving financial products and services.
