# **Resume Classification**

## Abstract
With the onset of the epidemic, everything has gone online, and individuals have been compelled to work from home. There is a need to automate the hiring process in order to enhance efficiency and decrease manual labour that may be done electronically. If resume categorization were done online, it would significantly reduce paperwork and human error. The recruiting process has several steps, but the first is resume categorization and verification. Automating the first stage would greatly assist the interview process in terms of speedy applicant selection. The classification of resumes will be performed using Machine Learning algorithms, which will aid in the extraction of skills and show diverse capabilities under appropriate job profile classes. While the abilities are being extracted, an appropriate job profile may be retrieved from the categorised and pre-processed data and shown on the interviewer's screen. During video interviews, this will aid the interviewer in the selection of candidates.

## Requirements
- Python - 3.6.7
- Beautiful Soup - 4.11.1
- Numpy - 1.16.4
- nltk - 3.2.5
- Matplotlib - 3.0.3
- Sklearn - 1.2.0

## Dataset
The dataset is scraped from online webpages named Resources for Employers. It contains 26 different job categories. "industry," "job_designation," "job_description," "responsibilities," "requirements," "skills," and "url_links" are the different categories of data scraped from the website. The dataset contains 1038 rows and 6 columns.

## Flow of the project
1. Scraped the required contents from the website and made them into a dataframe.
2. Corrected the target class's class imbalance.
3. Text pre-processing (removal of stop words, emojis, mentions, urls, and other noise, as well as a lemmatizing and stemming stage) and merging all the columns into a single column.
4. Use the TF-IDF vectorizer to convert the data into a model of numerical features that are ready to be used for classification.
5. Train five different ML classifiers using the training vectors with a splitting factor of 0.2.
6. Tune some of the parameters of the best classifier among the five to improve the model's accuracy.
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
