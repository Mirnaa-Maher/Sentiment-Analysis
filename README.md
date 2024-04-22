EXPERIMENTAL RESULTS

We have made 6 main experiments on our project each of them is in an individual notebook in google colab:

1-	Remove emoji without stemming
2-	Remove emoji with stemming
3-	With emoji, with stemming
4-	With emoji, without stemming
5-	Replace emoji without stemming
6-	Replace emoji with stemming

all preprocessing steps have been fixed and we just start to deal with 2 steps only which are stemming and dealing with emojis

first experiment: 
we start with removing emoji from all rows and try to not use stemming with it which returns each word to its root, to follow up the results of lime “a method of XAI” and see their effects on the visualization of xai.
We use an accuracy measure to compare results and found the result of these steps is good with our ML models as a beginning and with lime.
The accuracy of SVM is 65
The accuracy of the ensemble model is 64
We try other experiments to improve these results


second experiment: 
we try removing the emoji as 1st one but with stemming to conclude the effect of stemming on results and we found that accuracy increases up to 3 % in each model we use and it is a good step.
The accuracy of SVM is 67
The accuracy of ensemble model is 67

third experiment:
we start to deal with emoji and leave it in data with stemming for text and see how the models will understand it, we found that the accuracy of the model with emoji is less than the accuracy of the same model without emoji.
so we conclude that models don’t correctly deal with emojis so we will try to replace them with a word that reflects their meaning.
The accuracy of SVM is 65
The accuracy of the ensemble model is 66

fourth experiment:
try to find if stemming has a  high effect on the accuracy or just emojis 
we try to leave emoji without doing any type of stemming on it and found that accuracy becomes less than leaving emoji with stemming 
there for: stemming is a good preprocessing step as it increases the accuracy of experiment 2 when we use it and decreases it in experiment 4 when we do not use it.
The accuracy of SVM is 64
The accuracy of the ensemble model is 64


fifth experiment:
as we say before we will replace each emoji in the dataset with its meaningful text but without stemming
We found the result of these steps is good with our ML models and with lime but not the best one so we try the last experiment.
The accuracy of SVM is 66
The accuracy of ensemble model is 65

Sixth experiment:
Replacing emojis with text and trying using stemming too at the same time, we found the best results in this experiment so we build the remaining of the project on it. 
The accuracy of SVM is 67% 
The accuracy of the ensemble model is also 67%


Discussion 
Comparing the common models with the previous work on the same dataset :
SVM  68, 67
Naive Bayes  62,60
Complement Naive Bayes  64,63
Logistic Regression  69,66
Decision Tree  57,56
Ensemble  69,67
