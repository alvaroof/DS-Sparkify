# DS-Sparkify
Capstone Project for the Data Scientist Nanodegree @ Udacity

### Table of Contents

1. [Project Motivation](#project)

2. [File Descriptions](#file)

3. [Results and Conclusion](#results)

4. [Acknowledgements](#licensing)

   

## Project Motivation <a name="project"></a>

Customer churn has become one of the biggest concerns for digital companies out there, since any customer that drops out from the service is a direct loss in the stream of revenue. For that reason, there has been a growing interest in applying statistical methodologies to try to predict which are the customers at risk of churning, and enable these companies to take preemptive actions.

The project presented here resulted from my enrollment in the Data Scientist Nanodegree at Udacity. In this project, we have been provided with customer behavior data for a fictional company named Sparkify, which pretends to be an emulation of actual companies like Spotify or Pandora. The data is comprised of observations on user interactions with the music streaming application; songs listened to, likes, downgrades, thumbs up, thumbs down, metadata like gender, location, etc, and with all this, we have been asked to create a model to predict churn.

The following has been my attempt at this. Since the data is relatively big we've used Spark to analyze it, making use of a cloud service such as IBM Watson, which already provided us with en environment in which run Jupyter notebooks and a installation of both Python and Spark. From a statistical perspective we will train several models on these data, but finally use Gradient Booting Machines since it's the one we found to perform the best on this specific dataset.
    

## Requirements and File Descriptions <a name="file"></a>

Numpy, pandas and pyspark are required in order to run this project. Also you should have a installation of SPARK or use a cloud service that provide with such. We have made use of IBM watson free tier for this purpose.

The file with the data is not included in the repository given its realtively big size. So the only files that constitute this repository are two notebooks, one containing most of the code used during the exploratory analysis and early attempts at modelling, and finally **Sparkify.ipynb** containing the final version with the results here reported.
  
## Results and Conclusion <a name="results"></a>

The main findings of the code, and some technical deep-dive, can be found at the post available [here](https://medium.com/@ortiz.fernandez.alvaro/sparkify-137817f1dde4).

As said, Gradient Boosting Machines was the best performing algorithm on this dataset and for the feature space we looked through. The following are the best results on the train cross-validated test, where we have measured F1-scores. the rationale behind this choice of metric is that we have an unbalanced dataset, and we care more about precision and recall than plain accuracy. 

Logistic Regression: 0.69
SVM: 0.71
GBT: 0.76

After confirming that GBt is the best performing model, we did a last evaluation using test set.

Test Area Under ROC 0.7995642701525055
Model_gbt Metrics:
Accuracy: 0.8591549295774648
F-1 Score:0.8423431837710613

which surprisingly are even better than on the train set during cross-validation. Taking into account that we could have engineered many more features, the results are amazingly good.

As a conclusion, we know that Churn problems are present across different industries and business. And they can take on different aspects, as for example employee attrition. Therefore knowing how to tackle them seems like a good skill to have these days.

On the other hand, we know that working with data that's more than a few hundred megabytes, even if can be stored in memory, can still benefit of being processed with distributed computing frameworks, as spark. We have also learnt that Spark dataframes are a highly intuitive API, closely similar to Pandas, and that also counts with many implementation of machine learning algorithms. Among them, typical high-scoring algorithm, such as gradient boosting machines (hello to the Kaggle community out there), are available and ready to be used, which certainly is a good fit to this problem at hand.

When working with big datasets, using the lazy evaluation in spark is paramount to having as efficient a code as possible. In this case, most of the feature engineering part only happens once the final aggregated dataframe (the one that has 1 row per user, with the calculated features) is evaluated.

## Acknowledgements <a name="licensing"></a>

I would like to thanks the udacity nanodegree in Data Science's team; they have provided me with an excellent set of tools to deal with this project and actually the idea to tackle this is theirs, which has proven to be an excelent way to learn to use Spark. Also a huge clap to those parties collaborating with them which have provided the data we've used.
