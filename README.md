# Operationalizing Machine Learning
***
This project shows the code, images and results of an operationalizing project using Azure ML Studio, Azure SDK and Swagger.
## An overview of the project
***
This project first begins with uploading the dataset and using the AutoML function on Azure to generate the best model using a metric and ending criteria. The model is then deployed using Azure ACI to generate a swagger URI and REST API endpoint. The dataset used for this project is obtained from the direct marketing campaigns of a company which intends to predict whether a client will accept a term deposit or not. Using Azure and its workspace, this project looks at creating a cloud based machine learning model, from deployment to consumption and finally publication. Commands for the deployment, processing and endpoint results are executed using Git Bash. The image in the next section shows the steps and is followed by a description of the steps accompanied by useful figures.
## Architectural Diagram
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/screen-shot-2020-09-15-at-12.36.11-pm.png)
## Step I:- Uploading Data and Authentication
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/Image1.PNG)
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/Image2.PNG)
## Step II:- Using AutoML and Generating Model
At this point, security is enabled and authentication is completed. In this step, you will create an experiment using Automated ML, configure a compute cluster, and use that cluster to run the experiment.

Note: Be careful with your configuration if you use the lab provided to you. Your experiment will timeout after a certain amount of time! All your work saved locally in the lab will be lost once it times out. Always SAVE your work in Github!!!

You will use the same Bankmarketing dataset with course 1.

Copy the link to a new browser window to download the data:
https://automlsamplenotebookdata.blob.core.windows.net/automl-sample-notebook-data/bankmarketing_train.csv

Upload the bankmarketing_train.csv to Azure Machine Learning Studio so that it can be used when training the model.
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/Image3.PNG)
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/Image4.PNG)
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/Image5.PNG)
## Step III:- Azure Authentication
Now that the Best Model is deployed, enable Application Insights and retrieve logs. Although this is configurable at deploy time with a check-box, it is useful to be able to run code that will enable it for you.

Enabl
## Step IV:- Swagger UI
In this step, you will consume the deployed model using Swagger.

Azure provides a Swagger JSON file for deployed models. Head to the Endpoints section, and find your deployed model there, it should be the first one on the list.

A few things you need to pay attention to:

swagger.sh will download the latest Swagger container, and it will run it on port 80. If you don't have permissions for port 80 on your computer, update the script to a higher number (above 9000 is a good idea).

serve.py will start a Python server on port 8000. This script needs to be right next to the downloaded swagger.json file. NOTE: this will not work if swagger.json is not on the same directory.
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/Image9.PNG)
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/Image10.PNG)
## Step V:- Model Deployment
After the experiment run completes, a summary of all the models and their metrics are shown, including explanations. The Best Model will be shown in the Details tab. In the Models tab, it will come up first (at the top). Make sure you select the best model for deployment.

Deploying the Best Model will allow to interact with the HTTP API service and interact with the model by sending data over POST requests.
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/Image6.PNG)
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/Image7.PNG)
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/Image8.PNG)
## Step VI:- Enable Logging and Consuming Endpoints
Once the model is deployed, use the endpoint.py script provided to interact with the trained model. In this step, you need to run the script, modifying both the scoring_uri and the key to match the key for your service and the URI that was generated after deployment.

Hint: This URI can be found in the Details tab, above the Swagger URI.
## Step VII:- Jupyter Notebook Coding
For this part of the project, you will use the Jupyter Notebook provided in the starter files. You must make sure to update the notebook to have the same keys, URI, dataset, cluster, and model names already created. The notebook has several notes that look similar to this:
## Step VIII:- Publishing a Pipeline

A short description of how to improve the project in the future
Screenshots required with a short description to demonstrate key steps
A link to the screencast video on YouTube (or a similar alternative streaming service)


![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/Image11.PNG)
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/Image12.PNG)
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/Image13.PNG)
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/Image14.PNG)
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/Image15.PNG)
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/ApplicationInsightEnabled.PNG)
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/Consume_Publish_SDK.PNG)
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/Endpoint_JSON_Output.PNG)
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/Endpoint_Pipeline_Complete.PNG)
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/Endpoint_Pipeline_Complete_1.PNG)
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/Endpoint_Pipeline_Complete_2.PNG)
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/Endpoint_Pipeline_Complete_11.PNG)
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/Endpoint_py.PNG)
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/Enpoint_SDK_Check.PNG)
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/HTTPAPI_1.PNG)
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/HTTPAPI_2.PNG)
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/Insights.PNG)
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/Logspyresult.PNG)
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/Pipeline_1.PNG)
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/Pipeline_2.PNG)
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/Pipeline_Endpoint_5.PNG)
![alt text](https://raw.githubusercontent.com/AmDeep/Project2_Udacity_Microsoft_ML/main/Images/Pipeline_Rest_Endpoint_6.PNG)
## Link To Screencast
***
https://youtu.be/rN536O9UOLQ
***
