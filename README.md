# Predict_Churn_with_PySpark

## Project Motivation

The motivation for this project is to show the capabilties of using PySpark for data exploration and machine learning and practice using simulated log data from the fictional company Sparkify to attempt to predict customer churn.

The data analysis was done in two forms. 
1. 12GB of data were analyzed using distributed computing with an AWS Elastic MapReduce Cluster, EMR Notebook and PySpark.
2. A 120MB subset of the data was analyzed locally using PySpark, Pandas/Scikit-Learn, and a Jupyter Notebook.

## File Descriptions

- Sparkify.ipynb (Jupyter Notebook containing data analysis and modelling done locally on 120MB dataset)
- mini_sparkify_event_data.json (120 MB subset of full 12 GB used for local analysis)

## Dependencies

- pyspark
- numpy
- pandas
- matplotlib
- sklearn

## Summary of Results

After exploring the log data the 3 best features correlated to Churn were found to be: 

- Avg pageviews for Thumbs Down (0.27) 
- Avg pageviews for NextSong (-0.25)
- Avg pageviews for Roll Advert (0.18) 

This is not surprising. The higher percentage of time the user spends seeing advertisements or disliking music the more likely they are to cancel their service. The higher percentage of time the user spends listening to music the more likely they are to stay.

After this, 10 classification algorithms were compared using 5-fold cross validation.

The best performing model in terms of weighted f1 score was a Gradient Boosted Classifier.

![Alt text](https://github.com/tylerwatkins101/Predict_Churn_with_PySpark/blob/master/Classification%20Report.jpg)

## Acknowledgements

- Udacity PySpark Course (part of Data Scientists Nanodegree)
- stackoverflow.com
