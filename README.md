# SPS-6811-Credit-Card-Fraud-Prediction-using-IBM-Auto-AI
Credit Card Fraud Prediction using IBM Auto AI

Steps using AutoAI

Step 1: Create an account with IBM Cloud

1.1. Sign up for IBM Cloud. By clicking on create a free account you will get 30 days trial account.


Step 2: Create a new Watson Studio project

2.1. Sign up for IBM's Watson Studio.
2.2. Click on New Project 
2.3. Define the project by giving a Name and hit 'Create'.


Step 3: Adding Data

3.1. Clone this repository and Navigate to data and save the file on the disk. 
3.2. Click on Assets and select Browse and add the csv file from your file system.


Step 4: Add Asset as Auto AI

4.1. Click on Add to project and select AutoAI experiment.


Step 5: Create and define experiment

5.1. Click on New AutoAI experiment and give a name to the experiment.
5.2. Click on Associate a Machine Learning service instance to this project and select the Machine Learning service instance and hit reload. If you do not have Machine Learning service instance, then click on Associate Machine learning service instance and select the machine learning service and associate the service.
5.3. The Create button at the bottom right gets highlighted, go ahead and hit Create.


Step 6: Import the csv file

6.1. We need to import the csv file into the experiment. Click on Browse or Select from project to choose the fraud_dataset.csv file to import.


Step 7: Run experiment

7.1. We have to select the target variable, in this case it is Fraud_Risk. Notice that Prediction Type and Optimized Metric get highlighted which tells us that we are working on Binary Classification use case and the evaluation metric is Accuracy which is used for classification usecases.
7.2. We can click on experiment settings to adjust the holdout sample and training sample under source settings.
7.3. We can click on prediction setting to modify the Prediction type, Positive Class & Optimized metric if required. In this case, we will leave'em as is and hit save and close.
7.4. Click on Run experiment.


Step 8: Analyze results

8.1. The AutoAI experiment has been completed in 97 seconds to generate four pipelines. The duration of experiment depends completly on the size of the dataset. AutoAI selects the appropriate machine learning algorithm (in the fifth stage of the process under Model Selection) which is best suited for the dataset.
8.2. Each pipeline is run with different parameters, pipeline 3 is run on a sequence of HPO (hyper parameters optimization) & FE (feature engineering) where as pipeline 4 includes HPO (hyper parameters optimization), FE (feature engineering) and a combination of both. 
8.3. All these are done on the fly! Isn't it amazing that we just have to sit and watch while AutoAI takes care of things for us and generates awesome machine learning models!! There's very minimal intervention required to get things going and in no time we have the generated pipelines to choose from.


Step 9: Deploy to Cloud

9.1. The saved model can be found under Models under the project in Watson Studio. 
9.2. Click on three dots on the right side below Actions and hit Promote. 
9.3. Click the Promote to deployment space. 
9.4. Choose an existing deployment space or create a new one. 
9.5. Click Add Deployment.
9.6. In the page that opens, fill in the fields: Specify a name for the deployment. Select “Web service” as the Deployment type. Click Save.
9.7. Define the deployment by giving a name and hit Save. Note that, the model will get deployed as web service as a ReST API.


Step 10: Test the Model

10.1. We have created and deployed the model as a web service, how do we test it?? We have to click on Test tab which will have two options which are form and json. 
10.2. We can use form if we are to test one record at a time where we can give the values to each attribute manually and hit Predict to generate predictions. 
10.3. The output of 0 under values indicate that it is a fraudulent transaction. 
10.4. The output can be either 0 or 1 as per the data glossary provided in the data folder.














