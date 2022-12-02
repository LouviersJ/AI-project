# AI Project Predicting Heart Disease
## Student Names: Lou Joseph,  Thaddaeus Lankford

(`pip install -r requirements.txt` will install all the required packages to run the code in the Analyzer.ipynb file)

## Project summary
The problem we will be addressing is the prediction of prevalence and severity of heart disease. This project is useful because predicting heart disease can aid in preventative treatment and cardiac rehabilitation after heart disease has been detected. For this project we will be using a random forest classifier and support vector classifier to predict heart disease.

Often times this dataset is split to have binary classification of having heart disease and not, but the same dataset I retrieved from UC Irvine had 0-4 as the classifications for differing degrees of heart disease. Some of the papers I skimmed analyzing this dataset (cleveland is the one that is most commonly used alone because it has least null values) have found that a naive decision tree classifier had a better specificity (true
negative rate) and accuracy rating than Naive Bayes and Bayesian Neural, and sensitivity (True
Positive rate) rating near and higher than some ensemble classifiers, so naturally I decided a random forest classifier would be pretty good. 
I also implimented an SVM because of the multivaried nature of the classifications in hopes it would more accurratly label the test set with 5 classifications.
I also used the data from the switzerland dataset because it was the only other set with all the labels intact. I dropped all the rows from this set with more than 1 entry as null and up with an extra ~40 data points. I filled the "ca" field with the mean rounded value because it was a discrete set of values that I believed at the time would not impact the data in a huge way (it did), and thal with the rounded mean for the same reasons (this only filled 2 values so it was no problem).

I got the feature importances of my random forest models and made point line graphs with the features most correlated with having heart disease.
*The models predicting 5 classifications will hardly ever predict a "4" because of the lack of entries in the dataset that are 4s, there is a high corelation with being older and having more severe heart disease, but at a certain severity the age dips slightly from what I assume is the mortality rate of people that age having that severity of heart disease not living long enough to be observed, or just the general thinning of any given population around older ages.
