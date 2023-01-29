# **Resume Classification**

## Abstract
Since the pandemic began, everything has been done online, forcing many to work from home. The recruiting process has to be automated in order to increase efficiency and reduce manual labour that may be completed electronically. Online resume classification would drastically cut down on paperwork and human error. The first phase of the hiring process is the classification and verification of resumes. Automating the first step will substantially speed up the candidate selection part of the interview process. Using machine learning algorithms, resumes will be categorised, making it easier to extract talents and display a variety of capabilities under the proper job profile classes. An appropriate job profile may be derived from the classified and pre-processed data and shown on the interviewer's screen while the talents are being extracted. This will help the interviewer choose applicants during video interviews.

## Requirements
- Python - 3.6.7
- Beautiful Soup - 4.11.1
- Numpy - 1.16.4
- nltk - 3.2.5
- Matplotlib - 3.0.3
- Sklearn - 1.2.0

## Dataset
The dataset is scraped from online webpages named Resources for Employers. There are 26 distinct job categories in it. Many kinds of data collected from the website include "industry," "job designation," "job description," "responsibilities," "requirements," "skills," and "url links". The dataset has 6 columns and 1038 rows.

## Flow of the project
1. Gathered the required website content and converted it into a dataframe.
2. Redressed the class disparity in the target class.
3. Text pre-processing (including a lemmatizing and stemming stage, the elimination of stop words, emoticons, mentions, urls, and other noise), and combining all the columns into one column.
4. Used the TF-IDF vectorizer to convert the data into a model of numerical features that are ready to be used for classification.
5. Train five different ML classifiers using the training vectors with a splitting factor of 0.2.

6. Tune some of the parameters of the top classifier among the five to improve the model's accuracy.
7. Use the best estimator of the selected classifier to predict the test labels.


## Preprocessing Techniques:
- Letter casing
- Tokenizing
- Noise removal
- Stopword removal
- Normalization
- Vectorization


## Classifiers
- Logistic Regression
  + Accuracy = 98.88%
- K-nearest Neighbor Classifier
  + Accuracy = 88.78%
- Linear Support Vector Classifier
  + Accuracy = 98.56%
- Random Forest Classifier
  + Accuracy = 98.56%
- XGBoost Classifier
  + Accuracy = 99.36%
  
The best model is XGBoost with accuracy of 99.36%.

## Conclusion
Different machine learning models have different strengths that make some better than others for certain tasks, such as detecting hate speech. Some models are more accurate, while others are more efficient. It is important to use different models and compare their performances in order to find the best category. We had achieved 99.4% accuracy on the validation data.
