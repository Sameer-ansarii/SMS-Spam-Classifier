# SMS-Spam-Classifier

# About Dataset
## Context

The SMS Spam Collection is a set of SMS tagged messages that have been collected for SMS Spam research. It contains one set of SMS messages in English of 5,574 messages, tagged acording being ham (legitimate) or spam.

## Content
The files contain one message per line. Each line is composed by two columns: v1 contains the label (ham or spam) and v2 contains the raw text.

This corpus has been collected from free or free for research sources at the Internet:

-> A collection of 425 SMS spam messages was manually extracted from the Grumbletext Web site. This is a UK forum in which cell phone users make public claims about SMS spam messages, most of them without reporting the very spam message received. The identification of the text of spam messages in the claims is a very hard and time-consuming task, and it involved carefully scanning hundreds of web pages. The Grumbletext Web site is: [Web Link].


-> A subset of 3,375 SMS randomly chosen ham messages of the NUS SMS Corpus (NSC), which is a dataset of about 10,000 legitimate messages collected for research at the Department of Computer Science at the National University of Singapore. The messages largely originate from Singaporeans and mostly from students attending the University. These messages were collected from volunteers who were made aware that their contributions were going to be made publicly available. The NUS SMS Corpus is avalaible at: [Web Link].


-> A list of 450 SMS ham messages collected from Caroline Tag's PhD Thesis available at [Web Link].


-> Finally, we have incorporated the SMS Spam Corpus v.0.1 Big. It has 1,002 SMS ham messages and 322 spam messages and it is public available at: [Web Link]. This corpus has been used in the following academic researches:

## Acknowledgements
The original dataset can be found here. The creators would like to note that in case you find the dataset useful, please make a reference to previous paper and the web page: http://www.dt.fee.unicamp.br/~tiago/smsspamcollection/ in your papers, research, etc.

We offer a comprehensive study of this corpus in the following paper. This work presents a number of statistics, studies and baseline results for several machine learning methods.

Almeida, T.A., GÃ³mez Hidalgo, J.M., Yamakami, A. Contributions to the Study of SMS Spam Filtering: New Collection and Results. Proceedings of the 2011 ACM Symposium on Document Engineering (DOCENG'11), Mountain View, CA, USA, 2011.

![dataset-cover](https://github.com/Sameer-ansarii/SMS-Spam-Classifier/assets/125865393/f28bd7a8-6be4-4a90-859d-a90ace7f7923)


--------------------------

# SMS Spam Classifier Project Report
## Introduction
This project aims to develop a spam classifier using Natural Language Processing (NLP) and Machine Learning techniques. The goal is to accurately differentiate between spam and ham (non-spam) messages in the SMS text data.

## Methodology
### 1. Data Acquisition and Preprocessing
* The SMS Spam Collection Dataset from Kaggle was used for this project.


* The dataset contains 5,572 messages with 5 columns.


* Irrelevant columns (Unnamed: 2, Unnamed: 3, Unnamed: 4) were removed.


* Duplicates (403) were dropped from the dataset.


#### 2. Data Exploration and Analysis
* The dataset contained no null values, ensuring data integrity.


* A new column 'message_length' was added to represent the length of each message.


* Statistical summaries revealed insights on message length distribution and other aspects of the data.


* The value counts of target categories ('ham' and 'spam') were calculated.


### 3. Data Visualization

* The distribution of target categories showed that 87.37% were 'ham' messages and 12.63% were 'spam' messages.


* Histograms and box plots revealed the skewness of message length in both categories.


### 4. Data Preprocessing
* Text preprocessing techniques such as lower casing, tokenization, and stemming (using Snowball Stemmer) were applied to the messages.


* Stop words, HTML tags, square brackets, and URLs were removed to clean the text.


### 5. Text Vectorization Using TF-IDF
* TF-IDF vectorization was performed on both the training and test sets to convert text data into numerical form.


* A total of 6012 features were generated using TF-IDF vectorization.



### 6. Train-Test Split
* The data was split into training and test sets in a 80:20 ratio.


* The dimensions of the resulting sets were displayed.
### 7. Model Building and Evaluation


* Nine different classifiers were trained and evaluated using performance metrics.


* Random Forest Classifier demonstrated excellent performance with high accuracy, precision, recall, F1-score, and balanced accuracy.


### 8. Model Evaluation
* Classification reports for both the training and test data were generated, providing insights into precision, recall, and F1-score.


* The confusion matrix in percentage form illustrated the distribution of false positives and false negatives.


### 9. Cross Validation
* Cross-validation was performed to assess model performance and variance.


* The mean accuracy score of the Random Forest Classifier was calculated.
### 10. Model Saving

* The trained Random Forest Classifier model was saved using the joblib library.


## Conclusion
In conclusion, the developed SMS spam classifier successfully differentiates between spam and ham messages with high accuracy and precision. The Random Forest Classifier emerged as the best-performing model, providing consistent results on both training and test data. This project showcases the effectiveness of NLP techniques and machine learning algorithms in tackling text classification tasks.

## Future Work
* Further hyperparameter tuning could be performed to optimize model performance.


* Ensemble methods or deep learning architectures could be explored for potential improvements.


* The model could be integrated into a messaging platform or email client for practical use.
