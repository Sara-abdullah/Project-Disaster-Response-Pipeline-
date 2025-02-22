# Disaster Response Pipeline Project
Udacity Disaster Response Pipeline Project.
![Screenshot](/screenshots/011.png)

# Project Motivation
This Project is part of the Data Science Nanodegree Program by Udacity. The initial dataset contains pre-labeled tweets and messages from real-life disasters. The aim of the project is to build a Natural Language Processing tool that categorizes messages.

The Project is divided into the following sections:

- Data Processing, ETL Pipeline to extract data from the source, clean data, and save them in a proper database structure
- Machine Learning Pipeline to train a model able to classify text message in categories
- Web App to show model results in real-time.

# Content
* Data

       - process_data.py: reads in the data, cleans and stores it in a SQL database. Basic usage is python- process_data.py MESSAGES_DATA CATEGORIES_DATA NAME_FOR_DATABASE.
       - disaster_categories.csv and disaster_messages.csv (dataset)
       - DisasterResponse.db: created database from transformed and cleaned data.

* Models

      - train_classifier.py: includes the code necessary to load data, transform it using natural language processing, run a machine learning model using GridSearchCV and train it. Basic usage is python train_classifier.py DATABASE_DIRECTORY SAVENAME_FOR_MODEL
      
* App

      _ run.py: Flask app and the user interface used to predict results and display them.
      - templates: folder containing the html templates

# Install
 libraries installed:
 
- Machine Learning Libraries: NumPy, SciPy, Pandas, Sciki-Learn
- Natural Language Process Libraries: NLTK
- SQLlite Database Libraqries: SQLalchemy
- Web App and Data Visualization: Flask, Plotly

You will also need to have software installed to run and execute an iPython Notebook

# Instructions : 

1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/

# Screenshots
![Screenshot](/screenshots/012.png)


![Screenshot](/screenshots/013.png)

# Results
The Disaster Response Project web app allows the user to enter a message and classifies the message into categories. It also shows some visual insights into the data such as the distribution of categories in the data sets that the model was trained on.

All code is in public repository at the link below:
https://github.com/Sara-abdullah/Project-Disaster-Response-Pipeline-

Note: The focus of this learning project is not on model performance, but more on data engineering and clean code. For this reason and due to limited time, the performance of the model is unacceptable for a real-world problem at this stage of development. 

# Acknowledgements
Udacity  for providing such a complete Data Science Nanodegree Program
