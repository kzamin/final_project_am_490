# News Document Topic Classifier

# Abstract - in a paragraph or two, summarize the project

Built a topic classifier for news articles using the BBC News Dataset and the Huffington Post 1 Million News Articles Dataset. Utilizes bag of words and TF-idf featurization techniques and Multinomial Naive Bayes, Decision Tree, RNN, K Neighbors, and Random Forest Classifiers.

# Problem statement - what are you trying to solve/do

The ability to analyze and discover the topic of a news article from the article itself or the headline and a short description. 

# Related work - what papers/ideas inspired you, what datasets did you use, etc

Related Work: 
http://cs229.stanford.edu/proj2013/ChaseGenainKarniolTambour-LearningMulti-LabelTopicClassificationofNewsArticles.pdf

Datasets: 
https://www.kaggle.com/datasets/shivamkushwaha/bbc-full-text-document-classification
https://www.kaggle.com/datasets/therohk/million-headlines

Ideas: 
https://www.analyticsvidhya.com/blog/2021/12/text-classification-of-news-articles/
https://machinelearningmastery.com/gentle-introduction-bag-words-model/
https://www.datacamp.com/tutorial/naive-bayes-scikit-learn

# Methodology - what is your approach/solution/what did you do?

I originally attempted solving this with Multinomial Naive Bayes classifier and a Bag of Words vectorization scheme. Then, I proceeded to try out other classifiers used for these types of problems alongside the Tf-Idf vectorization scheme in order to see if I could match or even beat my original performance. 

I split up the original datasets by designating 20% of the data as test data and the rest as training data. I also made sure to shuffle the traininig data for every run.

For the million news articles dataset, the articles were not included in the dataset so I merged the headline + a short description of the article as the input data to see how the classifers fared on limited data. 

# Experiments/evaluation - how are you evaluating your results
I calculated the accuracy percentage by using sklearn metrics and comparing the classifer prediction to the original labels. 

Dataset: BBC News, Vectorizer: Bag of Words

K Nearest Neighbors Classifier
Accuracy: 0.7544642857142857

Multinomial Naive Bayes Classifier
Accuracy: 0.9799107142857143

Random Forest Classifier
Accuracy: 0.27232142857142855

RNN Classifier
Accuracy: 0.9799107142857143

Decision Tree Classifer
Accuracy: 0.8125


Dataset: BBC News, Vectorizer: Tf-idf

K Nearest Neighbors Classifier
Accuracy: 0.9441964285714286

Multinomial Naive Bayes Classifier
Accuracy: 0.9375

Random Forest Classifier
Accuracy: 0.2611607142857143

RNN Classifier
Accuracy: 0.984375

Decision Tree Classifer
Accuracy: 0.828125

# Results - How well did you do

For the BBC dataset, Multinomial Naive Bayes (MNB) and RNNs out performed all other schemes in the BoW model. However, MNB struggled in the Tf-idf scheme while K-nearest neighbors did significantly better and RNN came out in top. Random Forest struggled in all and was only slightly better than random guesses. 

# Examples - images/text/live demo, anything to show off your work (note, demos get some extra credit in the rubric)

# Video - a 2-3 minute long video where you explain your project and the above information

