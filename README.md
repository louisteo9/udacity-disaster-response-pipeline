# Disaster Response Pipeline Project (Udacity - Data Scientist Nanodegree Program)
## Table of Contents
1. [Introduction](https://github.com/louisteo9/udacity-disaster-response-pipeline#introduction)
2. [File Descriptions](https://github.com/louisteo9/udacity-disaster-response-pipeline#file-descriptions)
3. [Installation](https://github.com/louisteo9/udacity-disaster-response-pipeline#installation)
4. [Instructions](https://github.com/louisteo9/udacity-disaster-response-pipeline#instructions)
5. [Acknowledgements](https://github.com/louisteo9/udacity-disaster-response-pipeline#acknowledgements)
6. [Screenshots](https://github.com/louisteo9/udacity-disaster-response-pipeline#screenshots)

## Introduction
This project is part of the Udacity's Data Scientist Nanodegree Program in collaboration with [Figure Eight](https://www.figure-eight.com/).

In this project, the pre-labeled disaster messages will be used to build a disaster response model that can categorize messages received in real time during a disaster event, so that messages can be sent to the right disaster response agency.

This project includes a web application where disaster response worker can input messages received and get classification results.

## File Descriptions
### Folder: app
**run.py** - python script to launch web application.<br/>
Folder: templates - web dependency files (go.html & master.html) required to run the web application.

### Folder: data
**disaster_messages.csv** - real messages sent during disaster events (provided by Figure Eight)<br/>
**disaster_categories.csv** - categories of the messages<br/>
**process_data.py** - ETL pipeline used to load, clean, extract feature and store data in SQLite database<br/>
**ETL Pipeline Preparation.ipynb** - Jupyter Notebook used to prepare ETL pipeline<br/>
**DisasterResponse.db** - cleaned data stored in SQlite database

### Folder: models
**train_classifier.py** - ML pipeline used to load cleaned data, train model and save trained model as pickle (.pkl) file for later use<br/>
**classifier.pkl** - pickle file contains trained model<br/>
**ML Pipeline Preparation.ipynb** - Jupyter Notebook used to prepare ML pipeline

## Installation
There should be no extra libraries required to install apart from those coming together with Anaconda distribution. There should be no issue to run the codes using Python 3.5 and above.

## Instructions
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/

## Acknowledgements
* [Udacity](https://www.udacity.com/) for providing an excellent Data Scientist training program.
* [Figure Eight](https://www.figure-eight.com/) for providing dataset to train our model.

## Screenshots
1. Main page shows the Overview of Training Dataset & Distribution of Message Categories
![image](https://github.com/louisteo9/udacity-disaster-response-pipeline/blob/main/screenshots/1.%20main%20page.JPG)

2. Enter message and click 'Classify Message'
![image](https://github.com/louisteo9/udacity-disaster-response-pipeline/blob/main/screenshots/2.%20enter%20msg%20click%20classify.JPG)

3. After clicking 'Classify Message', we can see the category(ies) of which the message is classified to , highlighted in green
![image](https://github.com/louisteo9/udacity-disaster-response-pipeline/blob/main/screenshots/3.%20classify%20result.JPG)

4. Run process_data.py for ETL pipeline
![image](https://github.com/louisteo9/udacity-disaster-response-pipeline/blob/main/screenshots/4.%20run%20process_data.JPG)

5. Run train_classifier.py for ML pipeline
![image](https://github.com/louisteo9/udacity-disaster-response-pipeline/blob/main/screenshots/5.%20run%20train_classifier_1_rev1.JPG)
![image](https://github.com/louisteo9/udacity-disaster-response-pipeline/blob/main/screenshots/5.%20run%20train_classifier_2_rev1.JPG)
![image](https://github.com/louisteo9/udacity-disaster-response-pipeline/blob/main/screenshots/5.%20run%20train_classifier_3_rev1.JPG)

6. Run run.py in app's directory to run web app<br/>
![image](https://github.com/louisteo9/udacity-disaster-response-pipeline/blob/main/screenshots/6.%20run%20app.JPG)
