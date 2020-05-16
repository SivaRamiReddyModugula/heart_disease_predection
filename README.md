# Heart Disease Predection: Project Overview
- Created a tool that estimates Heart disease predection  to help the patients are suffering from the heart disease or not.
- Data collected from the [Kaggel](https://www.kaggle.com/ronitf/heart-disease-uci).
- Engineered Features from the data and handling the missing values and outliers.
- Logistic Regression, Decision Tree Classifier, K-Neighbors Classifier, Linear Discriminant Analysis, Navi-Baies Classifier, Support Vector Machine.
- Built a client facing API using flask.
## Code and Resources Used
**Python Version:** 3.7
**Packages:** pandas, numpy, sklearn, matplotlib, seaborn, flask, json, pickle
**For Web Framework Requirments:** >pip install -r requirements.txt
## Data Collection
For this project we collected the data from the [Kaggel](https://www.kaggle.com/ronitf/heart-disease-uci).
- age
- sex
- cp
- trestbps
- chol
- fbs
- restecg
- thalach
- exang
- oldpeak
- slope
- ca
- thal
- target
## Data Cleaning
After the data is collected from the Kaggle, I need to clean it up so that it was usable for our model. I made the the following changes:
- Find any missing values in the data. if there are any handel the missing values.
- Identify if there are any im-balance data. it is better to do **IQR** strategy.
- Drop the unusable columns.
## EDA
![alt data image not found](https://github.com/SivaRamiReddyModugula/heart_disease_predection/blob/data_gathering/Heart%20disease%20images/data.PNG)
![alt hist image not found](https://github.com/SivaRamiReddyModugula/heart_disease_predection/blob/data_gathering/Heart%20disease%20images/hist.PNG)
## Model Building
First I split the data into train and test data.
I tried six different models using the KFold from the model selection for selection the best model. 
- LogisticRegression
- DecisionTreeClassifier
- KNeighborsClassifier
- LinearDiscriminantAnalysis
- GaussianNB
- SVC
## Model Performance
Out of all the models **Decision Tree Classfier** give the better accuracy when compared with the other models.
- LogisticRegression---> accuracy: 85, (min,max)->accuracy: (42,100)
- DecisionTreeClassifier---> accuracy: 99, (min,max)->accuracy: (85,100)
- KNeighborsClassifier---> accuracy: 71, (min,max)->accuracy: (14,100)
- LinearDiscriminantAnalysis---> accuracy: 84, (min,max)->accuracy: (42,100)
- GaussianNB---> accuracy: 84, (min,max)->accuracy: (57,100)
- SVC---> accuracy: 97, (min,max)->accuracy: (71,100)
## Productionization
In this stepm I build a flask API endpoint that hosted on a local webserver by following along with the TDS tutorial. The API endpoint takes in a request with a list of values from patients report and returns an estimated result as you are suffering from the heart disease (or) not.
Later, I uploades this project [Heroku](https://heart-disease-pediction-api.herokuapp.com/)
