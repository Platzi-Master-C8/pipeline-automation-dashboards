# Pipelines for Automation Dashboards

This is how was created the pipeline to get data to create the Automation dashboards

![general_pipeline](assets/pipeline.png)


## 1. Create a project in Google Drive

You need to create a project folder to save the following files:
* Jupyter Notebook (Google colab)
* Json key from project Google Cloud project.
* *Google Sheet* with data to ingest the dashboard.

![drive_folder](assets/drive_folder.png)

## 2. Get data from Postgres and Mongodb

## 2.1 Google Cloud Platform

2.1.1 Create a project in Google Cloud Platform in order to connect the spreadsheets:
![new_project](assets/new_project.png)

2.1.2 Enable the APIs in the Google Cloud project. [Enable the APIs you want to use](https://developers.google.com/workspace/guides/enable-apis), for this project:  
* Google Sheets API 
* Google Drive API

2.1.3 Create access credentials: Service account type.
* Create key json type.
* Save into a drive folder.
![credentials](assets/credentials.png)

2.1.4 Create a *Google Sheet* in the drive project folder and share with the *service account email*.
![email](assets/email.png)

### 2.2 Jupyter Notebook (Google Colab)

* Notebook to get data [from Postgres](Notebooks/postgres_data.ipynb)
* Notebook to get data [from Mongodb](Notebooks/mongodb_data.ipynb)

## 3. Import data to Google Data Studio

![data](assets/data.png)
