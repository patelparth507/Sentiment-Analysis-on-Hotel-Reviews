# Sentiment-Analysis-on-Hotel-Reviews

Research Questions:
1. How satisfied are customers with Hotel Monaco?
2. What do customers think of Hotel Monaco?
3. What amenities influence customer satisfaction?
4. What should Hotel Monaco improve to attract more visitors?

Data Pre-Processing (Cleaning) steps:
1. Any expression which is not a word, changed it into space
2. Converted any upper case into lower case
3. Performed Tokenization
4. Used wordnet lexical database for English language to perform lemmatization
5. Removed any word whose length is less than 2

Vectorization (TF-IDF): 
1. Created 7000 features by TF IDF vectorization
2. Used bigrams and trigrams to understand the relevance of 2 and 3 consecutive words in the model
3. Removed stop words

Modeling:
1. Multinomial Logistic Regression:
- Multiclass classification
- Ridge Regularization to get rid of overfitting
- “newton-cg” solver to handle multinomial loss and support l2 penalty
- Inverse Regularization Strength 0.6 (Identified using hyperparameter tuning)
- Accuracy : 82%
- Log Loss : 0.48

2. Naive Bayes Theorem:
- Naive Bayes is a classification technique based on Bayes Theorem
- Used Bernoulli and Gaussian method in building model
- Accuracy of Bernoulli 77.43% and Log Loss of 2.395
- Accuracy of Gaussian 67.11% and Log Loss of 11.24

3. Random Forest:
- Uses bootstrap sampling technique to fit multiple trees and then aggregates individual tree to fit the model
- Helps to get rid of overfitting
- Used default Gini criterion to evaluate purity in subnodes
- Accuracy: 81.4%
- Log Loss: 0.508

Conclusions:
1. On the basis of the descriptive statistics, the overall average rating of the hotel is 3.95 out of 5 which shows that customers are mostly satisfied with the hotel
2. Amenities influencing customer satisfaction : Room quality
                                                 Staff service
                                                 location
                                                 restaurant
                                                 food quality
                                                 cleanliness
3. Improvements to be done :  Customer service by staff
                              Room & Charges description 
4. Through our model, the hotel would be able to classify their reviews into three different emotions and improve their service accordingly

