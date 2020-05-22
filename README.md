# TLInternship2020
## Module 1

Front_end - folder contains Django framework that contains a webpage that accepts the content and type of user mentioned classification. This information gets saved in SQLLite database of below format
![Database format](https://github.com/PreethiElango/TLInternship2020/blob/master/Img/db.jpeg)


Webpage looks like this if you open in  Pycharm and run the file.
![Front_end format](https://github.com/PreethiElango/TLInternship2020/blob/master/Img/Front%20page.jpeg)


## Module 2:
Scaling of data: We are storing the data in  SQL directly. So scaling would not be much issue. We are storing only the data and annotated input.

## Module 3:

### Overview
Building high quality ground truth - We process the input like removing stopwords, do stemming and tokenisation. Using the word in the text we vectorise the input and pass it to the model. May be at this step we can pass it to offensive word collection to get  the over all picutre of the sentence. we can also calculate the sentiment of the sentence as the additional parameter.

## Module 4:

### Overview
Data Preparation & cleaning.
-	In this we have collected the tweets and classified them into three categories.
-	Did the cleaning of tweets like removing links and punctuations.
-	removed the stopwords and later did the stemming.

Converting Tweets to TF-IDF
- we have converted all the tweets to the vectorizer form so that we can apply various machine 
Learning algorithms as model operates on numerical data and we had text data we have choosen to use TF-IDF form 
	
	
why we use SVM
- because we have larger feature i.e. 500 length vector for each sentence.
- capture much more complex relationships between your datapoints(sentence Vector form) without having to perform difficult transformations on your own
- it takes a longer time but in our case its was not an issue as data set is not that big and also this model will not be tranined again and again.

we have used linear kernel as it is faster and also we got desried accuracy also.
we have used default degree i.e. 3 as it worked correctly for me.
we set Probality as 1 as we need it later for choosing the label of lass.


We have created three SVM model out of it 
1  First for predicting whether sentence is hate speech or not 
2. Second for predicting whether sentence is offensive or not
3. Third for predicting whether sentence not hate and offensive.

we created three model so as to avoid the issues that comes because of imbalance data
so we have created three models with the proper balance data set.

We classfiy the sentence using these above created three model and class of a sentence is equal to the class which is predicted with the highest proability among the three classifiers.

## How to Run this File:
Front end
Please setup django environment and paste the front file into the python project and run.
You should be able to see the server running in the local.
You can hit the link and see that front page opens up.
Here, you can enter all the contents.

Data Analysis and Classification
Please open the Classifier.ipynb file in jupyter notebook and run the cells.
Description of each code is given in markdown cell.
You can change the input in last cell see the prediction of our classifier










