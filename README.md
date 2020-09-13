# Data Scientist Nanodegree

## Project: Recommendations with IBM

## Table of Contents

- [Project Overview](#overview)
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

## 2. Files

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

## 3. Software Requirements

This project uses **Python 3.6.3** and the necessary libraries are mentioned in _requirements.txt_.
The standard libraries which are not mentioned in _requirements.txt_ are _json_, _operator_, _pickle_, _pprint_, _re_, and _sys_.

<a id='credits'></a>

## 4. Credits and Acknowledgements <a name='licensing'></a>

Must give credit to [Figure-eight](https://www.figure-eight.com/) for the data and [Udacity](https://www.udacity.com/courses/all) for creating a great learning experience.  
Find the Licensing for the data and other descriptive information from [Figure-eight](https://www.figure-eight.com/dataset/combined-disaster-response-data/).

