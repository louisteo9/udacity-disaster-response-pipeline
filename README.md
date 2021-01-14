# Disaster Response Pipeline Project (Udacity - Data Scientist Nanodegree Program)
## Table of Contents
1. Introduction
2. File Descriptions
3. Installations
4. Instruction
5. Acknowledgements
6. Screenshots

## Introduction
This project is part of the Udacity's Data Scientist Nanodegree Program in collaboration with [Figure Eight](https://www.figure-eight.com/).

In this project, the pre-labeled disaster messages will be used to build a disaster response model that can categorize messages received in real time during a disaster event, so that messages can be sent to the right disaster response agency.

This project includes a web application where disaster response worker can input messages received and get classification results.

## File Descriptions
### Folder: app
run.py - python script to launch web application.
Folder: templates - web dependency files (go.html & master.html) required to run the web application.

### Folder: data
disaster_messages.csv - real messages sent during disaster events (provided by Figure Eight). 
disaster_categories.csv - categories of the messages
process_data.py - ETL pipeline used to load, clean, extract feature and store data in SQLite database.
ETL Pipeline Preparation.ipynb - Jupyter Notebook used to prepare ETL pipeline.
DisasterResponse.db - cleaned data stored in SQlite database.

### Folder: models
train_classifier.py - ML pipeline used to load cleaned data, train model and save trained model as pickle (.pkl) file for later use.
classifier.pkl - pickle file contains trained model.
ML Pipeline Preparation.ipynb - Jupyter Notebook used to prepare ML pipeline.

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
1. main page shows the overview of Training Dataset & distribution of message categories
![image](https://user-images.githubusercontent.com/47262286/104581402-7ce06d80-5699-11eb-99d4-684ec07feb0a.png)

2. Enter message and click 'Classify Message'
![image](https://user-images.githubusercontent.com/47262286/104581479-9aadd280-5699-11eb-905b-d26235333360.png)

3. After clicking 'Classify Message', we can see the category(ies) of which the message is classified to , highlighted in green
![image](https://user-images.githubusercontent.com/47262286/104581568-b87b3780-5699-11eb-8605-8b224a2186e5.png)

4. Run process_data.py for ETL pipeline
![image](https://user-images.githubusercontent.com/47262286/104581657-d8aaf680-5699-11eb-8022-65335afcfbd3.png)

5. Run train_classifier.py for ML pipeline
![image](https://user-images.githubusercontent.com/47262286/104581701-e82a3f80-5699-11eb-8692-2556d3995a75.png)
![image](https://user-images.githubusercontent.com/47262286/104581849-1c056500-569a-11eb-890d-50ff9493756f.png)

6. Run run.py in app's directory to run web app<br/>
![image](https://user-images.githubusercontent.com/47262286/104581902-2d4e7180-569a-11eb-8df3-536f98e6f26c.png)
