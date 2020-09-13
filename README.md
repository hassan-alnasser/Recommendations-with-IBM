# Data Scientist Nanodegree

## Project: Recommendations with IBM

## Table of Contents

- [Project Overview](#overview)
- [Project Components](#components)
  - [ETL Pipeline](#etl_pipeline)
  - [ML Pipeline](#ml_pipeline)
  - [Flask Web App](#flask)
- [Running](#run)
  - [Data Cleaning](#cleaning)
  - [Training Classifier](#training)
  - [Starting the Web App](#starting)
- [Conclusion](#conclusion)
- [Files](#files)
- [Software Requirements](#sw)
- [Credits and Acknowledgements](#credits)

***

<a id='overview'></a>

## 1. Project Overview

In this project, I'll apply a data science approach to analyze disaster data from <a href="https://www.figure-eight.com/" target="_blank">Figure Eight</a> to build a model for an API that classifies disaster messages.

_data_ directory contains a data set which are real messages that were sent during disaster events. I will be creating a machine learning pipeline to categorize these events so that appropriate disaster relief agency can be reached out for help.

This project will include a web app where an emergency worker can input a new message and get classification results in several categories. The web app will also display visualizations of the data.

[Here](#eg) are a few screenshots of the web app.

<a id='components'></a>

## 2. Project Components

There are three components of this project:

<a id='etl_pipeline'></a>

### 2.1. ETL Pipeline

File _data/process_data.py_ contains data cleaning pipeline that:

- Loads the `messages` and `categories` dataset
- Merges the two datasets
- Cleans the data
- Stores it in a **SQLite database**

<a id='ml_pipeline'></a>

### 2.2. ML Pipeline

File _models/train_classifier.py_ contains machine learning pipeline that:

- Loads data from the **SQLite database**
- Splits the data into training and testing sets
- Builds a text processing and machine learning pipeline
- Trains and tunes a model using GridSearchCV
- Outputs result on the test set
- Exports the final model as a pickle file

<a id='flask'></a>

### 2.3. Flask Web App

<a id='eg'></a>

Running [this command](#com) **from app directory** will start the web app where users can enter their query, i.e., a request message sent during a natural disaster.

**_Screenshot 1_**

![master](img/main.png)

What the app will do is that it will classify the text message into categories so that appropriate relief agency can be reached out for help.

<a id='run'></a>

<a id='files'></a>

## 5. Files

<pre>
.
├── app
│   ├── run.py------------------------# FLASK FILE THAT RUNS APP│   
│   └── templates
│       ├── go.html-------------------# CLASSIFICATION RESULT PAGE OF WEB APP
│       └── master.html---------------# MAIN PAGE OF WEB APP
├── data
│   ├── DisasterResponse.db-----------# DATABASE TO SAVE CLEANED DATA TO
│   ├── disaster_categories.csv-------# DATA TO PROCESS
│   ├── disaster_messages.csv---------# DATA TO PROCESS
│   └── process_data.py---------------# PERFORMS ETL PROCESS
├── img-------------------------------# PLOTS FOR USE IN README AND THE WEB APP
├── models
│   └── train_classifier.py-----------# PERFORMS CLASSIFICATION TASK

</pre>

<a id='sw'></a>

## 6. Software Requirements

This project uses **Python 3.6.3** and the necessary libraries are mentioned in _requirements.txt_.
The standard libraries which are not mentioned in _requirements.txt_ are _json_, _operator_, _pickle_, _pprint_, _re_, and _sys_.

<a id='credits'></a>

## 7. Credits and Acknowledgements <a name='licensing'></a>

Must give credit to [Figure-eight](https://www.figure-eight.com/) for the data and [Udacity](https://www.udacity.com/courses/all) for creating a great learning experience.  
Find the Licensing for the data and other descriptive information from [Figure-eight](https://www.figure-eight.com/dataset/combined-disaster-response-data/).

