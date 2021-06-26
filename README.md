# Rainfall-Prediction

## Table of Contents
* Overview/Problem Statement
* Dataset
* File Structure
* Major Packages/Libraries Used
* Installation/Working Environment
* Building the Web App
* App Implementation
* Drawbacks and Future Scope
* Credits

### 1. Overview/Problem Statement
* Australia is one of the Hottest Countries in the World averaging about 286mm rainfall in a year. So I decided to build a web app using ML to predict whether it will rain tomorrow or not! 
* For this problem, classification algorithms such as Logistic Regression, KNN, DecisionTree, RandomForest and XgBoost were implemented. XgBoost performed the best!

### 2. Dataset
* This dataset contains about 10 years of daily weather observations from many locations across Australia.
* Observations were drawn from numerous weather stations. The daily observations are available from http://www.bom.gov.au/climate/data. An example of latest weather observations in Canberra: http://www.bom.gov.au/climate/dwo/IDCJDW2801.latest.shtml
* RainTomorrow is the target variable to predict. It means -- did it rain the next day, Yes or No? This column is Yes if the rain for that day was 1mm or more.
* This dataset contains various independent features such as Maximum Temperature, Minimum Temperature, WindSpeed, etc.
* The dataset is available on Kaggle and the link is provided below.
* [Dateset Link](https://www.kaggle.com/jsphyg/weather-dataset-rattle-package)

### 3. File Structure
```
├── streamlit
│   ├── .stable_random_id
    ├── config.toml
    ├── credentials.toml
├── .gitattributes
├── Notebook.ipynb
├── Procfile
├── README.md
├── app.yaml
├── main.py
├── rain.jpg
├── rain.pkl
├── requirements.txt
├── setup.sh
```

### 4. Major Packages/Libraries Used
* pandas 
* numpy
* sci-kit learn
* matplotlib
* seaborn
* streamlit

### 5. Installation/Working Environment
Follow the instructions if you want to run the app from your local computer.
* The app is written using **Python 3.9.5**. You can download it from [here](https://www.python.org/downloads/).You can also download **Anaconda** which is a distribution of python from [here](https://www.anaconda.com/products/individual). I would recommend downloading anaconda since it is very useful as it comes with a lot of python libraries, Jupyter and Spyder IDE.
* Once you are done with the installation, you can clone this repository to your computer and install the required packages and libraries using the following line of code through the command prompt where your local environment is setup.
```
pip install -r requirements.txt
```
### 6. Building the Web App
* The web was developed using Streamlit web-app framework which is written in python suitable for small scale projects such as this one. For more information you can check the offical streamlit website by clicking [here](https://streamlit.io/)
* Basic understanding of streamlit and html was needed for designing the webpage and to make sure it was responsive to user inputs.

### 7. App Implementation  
* The app asks for user to enter the weather observations recorded by the weather station for a particular day, which included features such as Location, Date, Temperature, WindSpeed, etc. Based on these inputs, it is predicted whether it will rain tomorrow or not!

![1](https://user-images.githubusercontent.com/83957848/123480870-99a5a780-d620-11eb-97f6-e35fa4320808.JPG)
![2](https://user-images.githubusercontent.com/83957848/123480887-9f02f200-d620-11eb-9397-fd4aa460803f.JPG)
![3](https://user-images.githubusercontent.com/83957848/123480902-a32f0f80-d620-11eb-8989-77bb689c91ad.JPG)
![4](https://user-images.githubusercontent.com/83957848/123480917-a75b2d00-d620-11eb-8aab-42b434f7a9fb.JPG)

### 8. Drawbacks and Future Scope
* The data used for training and testing purpose of model was from 2007 till 2017 only.
* In this model OneHotEncoding has been implemented for categorical feature encoding. This has resulted in a large feature space. LabelEncoding could optimize the model.
* Although XgBoost performed the best, I was unable to use it for my model due to some dependency issue in app development.
* Although the web app has been successfully developed, I'm unable to deploy it because of some issue with the Pickle File.
* Complete removal of outliers has resulted in best model performance and same can be implemented in this problem.

### 9. Credits
I would like to thank [Krish Naik](https://github.com/krishnaik06) for hosting this problem statement on his youtube channel for the successful completion of this project.  
