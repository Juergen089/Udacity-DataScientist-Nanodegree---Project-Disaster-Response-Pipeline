# Udacity Data Scientist Nanodegree - Project Disaster Response Pipeline

## Table of Contents
1. [Description](#description)
2. [Dependencies](#dependencies)
3. [Installing and Executing](#execution)
3. [Additional Material](#additional)

<a name="descripton"></a>
## Description

This project "Disaster Response Pipeline" is part of the Udacity Data Scientist Nanodegree in cooperation with Figure Eight.
The target of the project is to classify disaster messages based on data from real disasters with the help of a Natural Language Processing Model (NLP).

This project is clustered in three Python scripts:

1. ./data/process_data.py:
Processing the data from real disaster messages, that came from Figure Eight in 2 csv files with an ETL pipeline: read the data from the csv-files, clean and wrangle it and save the data in a SQLite database.
2. ./models/train_classifier.py:
Build a NLP machine learning pipeline based on the data from the SQLite database to classify new disater messages.  
3. ./app/run.py
Run a flask-based web app with a user interface, into which new messages can be entered, which are classified on the basis of the NLP model.

<a name="dependencies"></a>
### Dependencies

* Python ver. 3.9 minimum
* Data Processing: NumPy, Pandas
* Machine Learning: Sciki-Learn
* Natural Language Processing: NLTK
* SQLlite Database: SQLalchemy
* Model Saving and Loading: Scikit-Learn / Pickle
* Web App and Visualization: Flask, Plotly

All of these modules can be installed by using the Anaconda package.

<a name="execution"></a>
### Installing and Executing:

1. Clone this Github repository to your local computer with python and the needed packages installed.

2. To run ETL pipeline to clean data and store the processed data in the database run from the project's root directory:
        `python ./data/process_data.py ./data/disaster_messages.csv data/disaster_categories.csv ./data/DisasterResponseDB.db`
3. To run the ML pipeline that loads data from DB, trains classifier and saves the classifier as a pickle file run from the project's root directory:
        `python ./models/train_classifier.py ./data/DisasterResponseDB.db ./models/classifier.pkl`

4. Go to `app` directory: `cd app` and run the web app: `python run.py`

5. Go to the displayed address in your web browser to see the web user interface, where you can enter a new disaster message to be categorized.

<a name="additional"></a>
### Additional Material:

In the folders ./data and ./models you find a Jupiter notebook each, which were used to prepare the code of the python scripts.
