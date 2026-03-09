# House Price Prediction Web Application 

PROJECT OVERVIEW

This project is a Machine Learning web application that predicts the price of a house based on several housing features. The application demonstrates the complete workflow of a Data Science and Machine Learning project, from data preprocessing and model training to deploying the model as an interactive web application.

Users can enter details about a property such as its size, number of bedrooms, number of bathrooms, parking availability, and other characteristics. The system then uses a trained machine learning model to estimate the predicted market price of the house.

The application was built using Python, Scikit-learn, and Streamlit, and is deployed online so that anyone can interact with the model through a web browser. This project demonstrates how data science solutions can be transformed from research notebooks into real-world usable tools.

LIVE APPLICATION 

The deployed application can be accessed here: house---price---app-fmdrxfvlswyhrnh8yyuh2m.streamlit.app

Users can open the link, enter house characteristics, and instantly receive a predicted price.

DATASET 

The model was trained using the Housing Prices Dataset from Kaggle.

Dataset Source: Kaggle Housing Prices Dataset
The dataset contains 545 housing records with information about house characteristics and their corresponding prices.
Each row represents a house listing.


DATASET FEATURES 

Feature	Description
price	Target variable representing the house price
area	Size of the house in square feet
bedrooms	Number of bedrooms
bathrooms	Number of bathrooms
stories	Number of floors in the house
mainroad	Whether the house has access to a main road
guestroom	Whether the house includes a guest room
basement	Whether the house includes a basement
hotwaterheating	Availability of hot water heating
airconditioning	Availability of air conditioning
parking	Number of parking spaces
prefarea	Whether the house is located in a preferred area
furnishingstatus	Furnishing status of the house


MACHINE LEARNING WORKFLOW 
This project follows the standard Machine Learning Lifecycle:

Data Collection
Data Cleaning and Preprocessing
Feature Engineering
Model Training
Model Evaluation
Model Serialization
Application Development
Model Deployment


DATA PREPROCESSING 
The dataset contains both numerical and categorical variables. Since machine learning models require numerical inputs, categorical features were converted to numeric values.

BINARY ENCODING 

Binary variables (e.g., yes/no) were encoded as:

yes → 1
no → 0

Categorical Encoding
The furnishingstatus variable was encoded as:

furnished → 2
semi-furnished → 1
unfurnished → 0


MODEL TRAINING 
A Linear Regression model from the Scikit-learn library was used to learn the relationship between housing features and house prices.

Training Set: 80% of the data
Testing Set: 20% of the data
The model was trained using the training set and evaluated using the testing set.

MODEL EVALUATION 
The performance of the model was evaluated using Mean Absolute Error (MAE).

MAE measures the average difference between predicted prices and actual prices.
A lower MAE indicates a more accurate model.


MODEL SERIALIZATION 
After training, the machine learning model was saved using Joblib:

joblib.dump(model, "house_model.pkl")
This creates a portable file that can later be loaded by the web application.

WEB APPLICATION 
The machine learning model was integrated into a Streamlit web application. Streamlit allows developers to build interactive web interfaces using only Python.

The application collects user inputs such as Area, Bedrooms, Bathrooms, Stories, Parking, and other property features. These inputs are processed and passed to the trained machine learning model, which then returns a predicted house price.

DEPLOYMENT 
The application was deployed using Streamlit Community Cloud, allowing the model to be hosted and accessed publicly through a web browser.

Deployment steps included:

Creating a GitHub repository
Uploading the project files
Creating a requirements.txt file
Deploying the application through Streamlit Cloud


TECHNOLOGIES USED 
Python
Pandas
NumPy
Scikit-learn
Joblib
Streamlit


PROJECT STRUCTURE 
house-price-app
│
├── app.py              # Main Streamlit application
├── house_model.pkl     # Serialized ML model
├── requirements.txt    # List of dependencies
└── README.md           # Project documentation

Key Learning Outcomes
This project demonstrates several essential skills for modern data scientists:

Data preprocessing and feature engineering
Training machine learning models
Evaluating model performance
Saving and loading trained models
Building web applications for ML models
Deploying machine learning solutions online
Future Improvements
Possible improvements for this project include:

Adding additional machine learning models such as Random Forest or Gradient Boosting
Implementing feature scaling
Improving model performance through hyperparameter tuning
Enhancing the user interface
Adding data visualizations
Deploying using containerized environments such as Docker
Implementing advanced MLOps workflows

Educational Use
This project was designed as a teaching demonstration for students learning Data Science and Machine Learning deployment. It provides a simple but realistic example of how machine learning models transition from experimentation environments (Jupyter Notebook/Google Colab) into real-world applications accessible to users.
