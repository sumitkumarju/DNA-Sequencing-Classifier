# DNA-Sequencing-Classifier
It was a Kaggle competition problem in which we have to categorize DNA into  6 different categories.
A dataset of DNA sequence and label was provided. This problem was interesting because the sequence was not of uniform length which is a requirement for feeding data to a classification or regression algorithm.So I need to change it into uniform length sequence.
Recently I learned about a new technique K-mer counting. A very efficient technique for identifying DNA sequence.The method I use here is simple and easy. I first take the long biological sequence and break it down into k-mer length overlapping “words”. For example, if I use "words" of length 6 (hexamers), “ATGCATGCA” becomes: ‘ATGCAT’, ‘TGCATG’, ‘GCATGC’, ‘CATGCA’. Hence our example sequence is broken down into 4 hexamer words.
Then I applied the BAG of WORDS using CountVectorizer using NLP. A multinomial naive Bayes classifier was used. I did some parameter tuning and found the ngram size of 4 (reflected in the Countvectorizer() instance) and a model alpha of 0.1 did the best result.
I was lucky to get accuracy = 0.954 and precision = 0.955 on the test dataset.
