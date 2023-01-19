# bagOfWords-Tfidf-vectorizers
This repository has the implementation of traditional NLP techniques like Bag Of Words (BoW) and TF-IDF from scratch and then comparing the results with the scikit learn's respective libraries/modules vectorizers.<br>
<h1>Sample Corpus of documents</h1>
Below is the sample corpus of string documents used for both the models i.e. BoW and TF-IDF.<br>
corpus = [<br>
     'the cat sat on the tree',<br>
     'the cat and dog are the best friends',<br>
     'there is a scarcity of mango tree and the pug dog',<br>
     'few cat are missing',<br>
]
<h1>1. Bag of Words (BoW)</h1>
A bag of words is a representation of text that describes the occurrence/frequency of words within a document. This technique is used in Natual Language Processing (NLP). This technique does not take semantic meaning into consideration, it just counts the frequency of words within a document.<br><br>
In scratch implementation, unique words are found out from the collection of documents corpus. These unique words are treated as column values. Each document from the corpus is treated as the row value. And then the frequency of those words in the sentence/document are calculated and treated as values in the table. In this way, BoW is implemented from scratch.<br>
After computing BoW values for above corpus, both from scratch and using SKLearn's Count Vectorizer library, below are the results in a tabular format.<br><br>

![image](https://user-images.githubusercontent.com/86348193/213409102-794af92f-fd12-4f01-b92a-11e129ba8646.png)
<br>
<h1>2. Term Frequency - Inverse Document Frequency (TF-IDF)</h1>
TF-IDF reflects how important a word is to a document in a collection or corpus. TF tells you how frequent a particular word is in your document. On the contrary, IDF tells you how unique a particular word is in your whole documents corpus or documents collection. This technique is used in Natual Language Processing (NLP). This technique does not take semantic meaning into consideration.<br><br>
Formula for TF-IDF is <b>tf-idf(t, d) = tf(t, d) * log(N/(df + 1))</b>. Here, t is a term or a word, d is a document, N is a count of all documents in a corpus, df is a occurence of word/term t in N documents. Here log is used to dampen the exploding effect of IDF if there are large number of documents in a corpus. In few cases, we use a fixed vocabulary and few words of the vocabulary might be absent in the document, in such cases, the df will be 0. As we cannot divide by 0, we smoothen the value by adding 1 to the denominator.<br><br>
In scratch implementation, unique words are found out from the collection of documents corpus. These unique words are treated as column values. Each document from the corpus is treated as the row value. And then the TF-IDF of those words in the sentence/document are calculated and treated as values in the table. In this way, TF-IDF is implemented from scratch.<br>
After computing TF-IDF values for above corpus, both from scratch and using SKLearn's tfidf Vectorizer library, below are the results in a tabular format.<br><br>

![image](https://user-images.githubusercontent.com/86348193/213413659-194b2d8d-5cbf-414c-92c4-186583812dcd.png)
