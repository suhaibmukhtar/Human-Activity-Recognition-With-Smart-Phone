# Human-Activity-Recognition-With-Smart-Phone
## Overview
Smart phones have become a most useful tool in our daily life for communication with advanced technology provided intelligent assistance to the user in their everyday activities. The portable working framework with computing ability and interconnectivity, application programming interfaces for executing outsiders’ tools and applications, mobile phones have highlights such as cameras, GPS, web browsers so on., and implanted sensors such as **accelerometers** and **gyroscope** which permits the improvement of applications in view of client’s specific area, movement and context.
![Project Framework](https://github.com/suhaibmukhtar/Human-Activity-Recognition-With-Smart-Phone/blob/main/images/Frame_Work.drawio.png
)


## Use of Feature Selection Techniques: 
The dataset used in this project is highly dimensional, with 563 features. Such high dimensionality can lead to issues like multicollinearity, increased computational cost, and reduced interpretability of the models. To mitigate these challenges and improve model performance, several feature selection techniques were applied.

## Techniques Used
<b>1. Variance Threshold:</b>
Purpose: Removes constant or quasi-constant features that do not add significant information.
Impact: Reduced the number of features by eliminating those with low variance, leading to a more concise and relevant feature set.

<b>2.Correlation Analysis:</b>
Purpose: Identifies and removes highly correlated features to reduce multicollinearity.
Impact: Improved model stability and interpretability by removing redundant features and focusing on independent predictors.

<b>3.ANOVA (Analysis of Variance):</b>
Purpose: Selects features based on F-statistics or F-ratio, especially useful for numeric features and categorical output.
Impact: Further refined the feature set, retaining features that have a significant impact on the target variable.
<b>Results After Applying Feature Selection</b>
Initial Feature Count: 563 features
Final Feature Count: Reduced to 100 features after applying feature selection techniques.
Accuracy Improvement: Model accuracy increased from 95% to 99% after feature selection.
These feature selection techniques were crucial in enhancing the performance, reducing computational complexity, and improving the interpretability of the models used in this project.

__Activity Recognition__ (AR) is monitoring the liveliness of a person by using smart phone. Smart phones are used in a wider manner and it becomes one of the ways to identify the human’s environmental changes by using the sensors in smart mobiles. *Smart phones are equipped in detecting sensors like gyroscope and accelerometer*. The contraption is demonstrated to examine the state of an individual. 

__Human Activity Recognition__ (HAR) framework *collects the raw data from sensors and observes the human movement using different deep learning approach*. Deep learning models are proposed to identify motions of humans with plausible high accuracy by using sensed data. 

__HAR Dataset from UCI dataset storehouse is utilized__. This dataset is collected from 30 persons (referred as subjects in this dataset), performing different activities with a smartphone to their waists. The data is recorded with the help of sensors (*accelerometer and Gyroscope*) in that smartphone. This experiment was video recorded to label the data manually.<p>

This project is to build a model that *predicts the human activities* such as __Walking, Walking_Upstairs, Walking_Downstairs, Sitting, Standing__ and __Laying__.

## Sources/Useful Links
- __Blog 1__ : https://www.ijrte.org/wp-content/uploads/papers/v8i1/A1385058119.pdf

- __Blog 2__ : https://machinelearningmastery.com/how-to-model-human-activity-from-smartphone-data/

- __For HAR Data_Set__ : https://archive.ics.uci.edu/ml/datasets/Smartphone+Dataset+for+Human+Activity+Recognition+%28HAR%29+in+Ambient+Assisted+Living+%28AAL%29

## Problem Statement
![#FF5733](https://via.placeholder.com/7x24/FF5733/000000?text=+) Given a new datapoint we have to predict the Human Activity, by using minimal set of features.

## Solution
We have a fairly small data set of Human Activity Recognition that has been labeled as “**Walking**”, “**Walking Upstairs**”, “**Walking Downstairs**”, “**Standing**”, “**Sitting**” and “**Lying**”.  We had downloaded HAR Dataset from UCI dataset storehouse .**Firstly** i used the blogs mentioned above as a reference to understand the domain Well. **Secondly**, After collection of dataset i.e. Data acquisition, with help of domain knowledge and EDA i carefully examined each feature,**Thirdly**,I used **feature selection techinques** so that to reduce the multicollinearity and remove the unwanted features which are not contributing in determining the output.**Then** we use pre-engineered dataset with classical machine learning (ML) to learn from the data, and predict the human Activity.
<div align='center'>
   ![Data Distribution](https://github.com/suhaibmukhtar/Human-Activity-Recognition-With-Smart-Phone/blob/main/images/download.png)
</div>

## Which type of ML Problem is this?
Human activity recognition, **is a challenging time series classification task.**
It involves predicting the movement of a person based on sensor data and traditionally involves deep domain expertise and methods from signal processing to correctly engineer features from the raw data in order to fit a machine learning model.

OR in other words you can call, it is a **multiclass classification problem**, for given a new datapoint we have to predict the Human Activity. And *Each datapoint corresponds one of the 6 Activities*.

## What is the best performance metric for this Problem?
- **Accuracy** : For any model we have printed the over all accuracy with this simple   “Accuracy” metric.

- **Confusion Matrix** : The very important thing that the confusion Matrix had told us what type of errors and what types of confusion are happening. 
    * Simply for understanding this metric for this project view, we know that we have 6 class label and often times it could so happen that our Model will be confused between sitting or standing, and walking upstairs or walking downstairs. 
    * So, the confusion Matrix is a very-very important way of understanding which class is your Algorithm or ML model is doing very well or for which classes your Algorithm or ML model is getting confused. 
