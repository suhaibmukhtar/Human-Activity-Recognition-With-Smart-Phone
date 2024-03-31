# Human-Activity-Recognition-With-Smart-Phone
## Overview
Smart phones and Smart Watches have become a most useful tool in our daily life for communication with advanced technology provided intelligent assistance to the user in their everyday activities. The portable working framework with computing ability and interconnectivity, application programming interfaces for executing outsiders’ tools and applications, mobile phones have highlights such as cameras, GPS, web browsers so on., and implanted sensors such as **accelerometers** and **gyroscope** which permits the improvement of applications in view of client’s specific area, movement and context.<p>
  As these algorithms are used in devices like Smart Watches and Smart Phones with low computation power, it would be the good practice to reduce the Multicollinearity, and select only the best features which are contributing in determing the Activity recognition</p>
## Objectives
__Activity Recognition__ (AR) is monitoring the liveliness of a person by using smart phone. Smart phones are used in a wider manner and it becomes one of the ways to identify the human’s environmental changes by using the sensors in smart mobiles. *Smart phones are equipped in detecting sensors like gyroscope and accelerometer*. The contraption is demonstrated to examine the state of an individual.<br> 
                This project is to build a model that *predicts the human activities* such as __Walking, Walking_Upstairs, Walking_Downstairs, Sitting, Standing__ and __Laying__ as done in Smart-Watches.

__Feature Selection__ (FS) selecting the features that are contributing in determining the output variable. Selecting the subset of features from the features of dataset, using only subset of features without letting drop in the accuracy of the model. As these algorithms are executed on the devices with low computational power.

__Human Activity Recognition__ (HAR) framework *collects the raw data from sensors and observes the human movement using different deep learning approach*. Deep learning models are proposed to identify motions of humans with plausible high accuracy by using sensed data. 

## Scope of Project: Activity Recognition in Smartphones and Smartwatches

The scope of this project revolves around developing a system for activity recognition in both smartphones and smartwatches. The goal is to leverage machine learning algorithms to accurately identify and classify different activities performed by users, such as walking, running, sitting, standing, etc. The project focuses on real-time analysis, meaning that the recognition process should be efficient and effective for immediate use.
<h1 align='center'>Methodology Followed</h1>

![Project Framework](https://github.com/suhaibmukhtar/Human-Activity-Recognition-With-Smart-Phone/blob/main/images/Frame_Work.drawio.png)
## 1. Download the Dataset from Kaggle/UCI ML repository
###  Data Directory
   ![npic03](https://user-images.githubusercontent.com/49862149/91126397-7c7f1000-e6c1-11ea-94e9-c909b34df502.jpg)

-  ![#FF5733](https://via.placeholder.com/8x24/FF5733/000000?text=+) __Important Note__: When I am applying Machine learning algorithm, I use these experts created feature data. When we are applying Deep learning algorithm, I use RAW sensors DATA for predicting Human Activity.
   ![npic4](https://user-images.githubusercontent.com/49862149/91137130-25326d00-e6cc-11ea-99a0-1cee55d314c0.jpg)
 
-  ![#FF5733](https://via.placeholder.com/8x24/FF5733/000000?text=+) The data is provided as a single zip file that is about **58 megabytes** in size. The direct link for this download is: [**UCI HAR Dataset.zip**](https://archive.ics.uci.edu/ml/machine-learning-databases/00364/dataset_uci.zip)

## 2. Perform the Data-Preprocessing and EDA:
1) Perform the feature scaling so that to restric all the feature under the same scale.
2) Check for distribution of data.
<div align="center">
  <img src="https://github.com/suhaibmukhtar/Human-Activity-Recognition-With-Smart-Phone/raw/main/images/download.png" alt="Data Distribution">
</div>
<div align="center">
  <img src="https://github.com/suhaibmukhtar/Human-Activity-Recognition-With-Smart-Phone/blob/main/images/pie.png" alt="Pie Distribution">
</div>
3) Check for missing values, if exist then replace them with mean/medain for numerical featues and replace with mode for categorical features.


   
## 2.1. Check and Display Duplicate Features in the Dataset
<div align="center">
  <img src="https://github.com/suhaibmukhtar/Human-Activity-Recognition-With-Smart-Phone/blob/main/images/duplicated_cols.png" alt="Duplicated Features">
</div>

## 3) Feature Engineering
### Use of Feature Selection Techniques for Selecting Optimal features: 
The dataset used in this project is highly dimensional, with 563 features. Such high dimensionality can lead to issues like multicollinearity, increased computational cost, and reduced interpretability of the models. To mitigate these challenges and improve model performance, several feature selection techniques were applied.
### Techniques Used
### a) Variance Threshold:
Purpose: Removes constant or quasi-constant features that do not add significant information.
Impact: Reduced the number of features by eliminating those with low variance, leading to a more concise and relevant feature set.

### b) Correlation Analysis:
Purpose: Identifies and removes highly correlated features to reduce multicollinearity.
Impact: Improved model stability and interpretability by removing redundant features and focusing on independent predictors.

### c) ANOVA (Analysis of Variance):
Purpose: Selects features based on F-statistics or F-ratio, especially useful for numeric features and categorical output.
Impact: Further refined the feature set, retaining features that have a significant impact on the target variable.

## Results After Applying Feature Selection</b>
### Initial Feature Count: 563 features
### Final Feature Count: Reduced to 100 features after applying feature selection techniques.
<div align="center">
  <img src="https://github.com/suhaibmukhtar/Human-Activity-Recognition-With-Smart-Phone/blob/main/images/features_after_feature_selection.png" alt="Duplicated Features">
</div>

### Accuracy Improvement: Model accuracy increased from 95% to 99% after feature selection .
These feature selection techniques were crucial in enhancing the performance, reducing computational complexity, and improving the interpretability of the models used in this project.
<div style="display: flex;">
    <img src="https://github.com/suhaibmukhtar/Human-Activity-Recognition-With-Smart-Phone/blob/main/images/conf_before.png" alt="Confusion-matrix of LR Before" style="width: 45%;">
    <img src="https://github.com/suhaibmukhtar/Human-Activity-Recognition-With-Smart-Phone/blob/main/images/confusion_matrix.png" alt="Confusion-matrix of LR After" style="width: 45%;">
</div>




## DataSet Description
__HAR Dataset from UCI dataset storehouse is utilized__. This dataset is collected from 30 persons (referred as subjects in this dataset), performing different activities with a smartphone to their waists. The data is recorded with the help of sensors (*accelerometer and Gyroscope*) in that smartphone. This experiment was video recorded to label the data manually.<p>



## Sources/Useful Links
- __Blog 1__ : https://www.ijrte.org/wp-content/uploads/papers/v8i1/A1385058119.pdf

- __Blog 2__ : https://machinelearningmastery.com/how-to-model-human-activity-from-smartphone-data/

- __For HAR Data_Set__ : https://archive.ics.uci.edu/ml/datasets/Smartphone+Dataset+for+Human+Activity+Recognition+%28HAR%29+in+Ambient+Assisted+Living+%28AAL%29

## Problem Statement
![#FF5733](https://via.placeholder.com/7x24/FF5733/000000?text=+) Given a new datapoint we have to predict the Human Activity, by using minimal set of features.

## Solution
We have a fairly small data set of Human Activity Recognition that has been labeled as “**Walking**”, “**Walking Upstairs**”, “**Walking Downstairs**”, “**Standing**”, “**Sitting**” and “**Lying**”.  We had downloaded HAR Dataset from UCI dataset storehouse .**Firstly** i used the blogs mentioned above as a reference to understand the domain Well. **Secondly**, After collection of dataset i.e. Data acquisition, with help of domain knowledge and EDA i carefully examined each feature,**Thirdly**,I used **feature selection techinques** so that to reduce the multicollinearity and remove the unwanted features which are not contributing in determining the output.**Then** we use pre-engineered dataset with classical machine learning (ML) to learn from the data, and predict the human Activity.**At End**, we evaluated all the models using performance measures such as Accuracy-Score, Confusion Matrix and Classification report, 


## Which type of ML Problem is this?
Human activity recognition, **is a challenging time series classification task.**
It involves predicting the movement of a person based on sensor data and traditionally involves deep domain expertise and methods from signal processing to correctly engineer features from the raw data in order to fit a machine learning model. In Addition it is a supervised Machine Learning Problem.

OR in other words you can call, it is a **multiclass classification problem**, for given a new datapoint we have to predict the Human Activity. And *Each datapoint corresponds one of the 6 Activities*.

## What is the best performance metric for this Problem?
- **Accuracy** : For any model we have printed the over all accuracy with this simple   “Accuracy” metric.

- **Confusion Matrix** : The very important thing that the confusion Matrix had told us what type of errors and what types of confusion are happening. 
    * Simply for understanding this metric for this project view, we know that we have 6 class label and often times it could so happen that our Model will be confused between sitting or standing, and walking upstairs or walking downstairs. 
    * So, the confusion Matrix is a very-very important way of understanding which class is your Algorithm or ML model is doing very well or for which classes your Algorithm or ML model is getting confused.
<div align="center">
  <img src="https://github.com/suhaibmukhtar/Human-Activity-Recognition-With-Smart-Phone/blob/main/images/confusion_matrix.png" alt="Confusion Matrix">
</div>

<div align="center">
  <img src="https://github.com/suhaibmukhtar/Human-Activity-Recognition-With-Smart-Phone/blob/main/images/download%20(1).png" alt="Classification Report">
</div>
  We can see clearly in this confusion matrix plot our model is doing very well for class Laying and Walking and good for Standing, Walking_Downstairs and Walking_Upstairs but our model getting confused with Sitting Class. 

- **Multi-class log-loss**: We know that Multi-class log-loss is very important metric for multiclass ML problem. 

## Business Objectives and Constraints
- These days, in addition to Smartphones, we are also using **Smart-Watches** like Fitbit or Apple-Watch, which help us to track our health. They monitor our each activity throughout the day check how many calories we have burnt. How many hours have we slept. However, in addition to Accelerometer and Gyroscope, they also use Heart-Rate data to monitor our activity. Since, we only have Smartphone data so just by using Accelerometer and Gyroscope data we will monitor the activity of a person. This software can then be converted into an App which can be downloaded in Smartphone. Hence, a person who has Smartphone can monitor his/her health using this App.

- **The cost of a mis-classification can be very high**.

- **No strict latency concerns**.


   


## Train and Test ratio
30 subjects(*volunteers*) data is randomly split to __80%__ of the volunteers were taken as __training data__ and remaining __20%__ subjects’ recordings were taken for __test data__.  _e.g_. 21 subjects for train and nine for test.

