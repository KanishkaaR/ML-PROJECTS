## **TEXT SUMMARIZATION USING ML**:-
### INTRODUCTION:-
    In this project, text summarization is implemented using Natural Language Processing(NLP). The aim is to generate a concise and meaningful summary of given text. We used TextRank algorithm for text summarization.
### TextRank Algorithm:-
    TextRank is an extractive and unsupervised text summarization technique. 
    How TextRank algo works?
        1) The first step would be to concatenate all the text contained in the articles
        2) Then split the text into individual sentences
        3) In the next step, we will find vector representation (word embeddings) for each and every sentence
                For word vector representation we use 'GloVe(Global Vectors for Word Representation)'. GloVe is an unsupervised learning algorithm for obtaining vector representations for words.  We could have also used the Bag-of-Words or TF-IDF approaches to create features for our sentences, but these methods ignore the order of the words.
                Link to download GloVe:- https://www.kaggle.com/rtatman/glove-global-vectors-for-word-representation?select=glove.6B.100d.txt
        4) Similarities between sentence vectors are then calculated and stored in a matrix
        5) The similarity matrix is then converted into a graph, with sentences as vertices and similarity scores as edges, for sentence rank calculation
                Here rank is calculated using PageRank Algorithm. It is is used primarily for ranking web pages in online search results. Here inplace of web pages we use sentences. 
        6) Finally, a certain number of top-ranked sentences form the final summary.