# DS-Sparkify
Capstone Project for the Data Scientist Nanodegree @ Udacity

### Table of Contents

1. [Project Motivation](#project)

2. [File Descriptions](#file)

3. [Results](#results)

4. [Acknowledgements](#licensing)

   

## Project Motivation <a name="project"></a>

Customer churn has become one of the biggest concerns for digital companies out there, since any customer that drops out from the service is a direct loss in the stream of revenue. For that reason, there has been a growing interest in applying statistical methodologies to try to predict which are the customers at risk of churning, and enable these companies to take preemptive actions.

The project presented here resulted from my enrollment in the Data Scientist Nanodegree at Udacity. In this project, we have been provided with customer behavior data for a fictional company named Sparkify, which pretends to be an emulation of actual companies like Spotify or Pandora. The data is comprised of observations on user interactions with the music streaming application; songs listened to, likes, downgrades, thumbs up, thumbs down, metadata like gender, location, etc, and with all this, we have been asked to create a model to predict churn.

The following has been my attempt at this. Since the data is relatively big we've used Spark to analyze it, making use of a cloud service such as IBM Watson, which already provided us with en environment in which run Jupyter notebooks and a installation of both Python and Spark. From a statistical perspective we will train several models on these data, but finally use Gradient Booting Machines since it's the one we found to perform the best on this specific dataset.
    

## File Descriptions <a name="file"></a>

The file with the data is not included in the repository given its realtively big size. 
  
## Results <a name="results"></a>

The main findings of the code, and some technical deep-dive, can be found at the post available [here](https://medium.com/@ortiz.fernandez.alvaro/sparkify-137817f1dde4).


## Acknowledgements <a name="licensing"></a>

I would like to thanks the udacity nanodegree in Data Science's team; they have provided me with an excellent set of tools to deal with this project and actually the idea to tackle this is theirs, which has proven to be an excelent way to learn to use Spark. Also a huge clap to those parties collaborating with them which have provided the data we've used.
