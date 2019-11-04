# Decision_Trees-on-Amazon_Fine_Food_Reviews
Given a review, Using a decision tree model determine whether the review is positive (rating of 4 or 5) or negative (rating of 1 or 2). [Q] How to determine if a review is positive or negative? [Ans] We could use Score/Rating. A rating of 4 or 5 can be cosnidered as a positive review. A rating of 1 or 2 can be considered as negative one. A review of rating 3 is considered nuetral and such reviews are ignored from our analysis. This is an approximate and proxy way of determining the polarity (positivity/negativity) of a review.


Models used: Sklearn DecisionTreeClassifier, Vectorizers used : Bow (sklearn-CountVectorizer),Tfidf(sklearn-TfidfVectorizer),Avg-W2v(trained a gensim model),Tfidf-W2v Metrics used: auc(sklearn's roc_auc) and Accurcy

Ipynb notebook also consits of feature importance represented in the form of wordcloud

Obtained results:

+------------+---------------+-------+------------------+----------+------+
| Vectorizer |     Model     | depth | min sample split | Accuracy | AUC  |
+------------+---------------+-------+------------------+----------+------+
|    Bow     | Decision Tree |   50  |       500        |  86.698  | 0.89 |
|   Tfidf    | Decision Tree |   50  |       500        |  87.154  | 0.89 |
|  Avg-W2v   | Decision Tree |   10  |       500        |  86.304  | 0.88 |
| Tfidf-W2v  | Decision Tree |   10  |       500        |  85.451  | 0.85 |
+------------+---------------+-------+------------------+----------+------+
