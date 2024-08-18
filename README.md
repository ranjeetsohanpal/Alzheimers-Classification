# 🧠 Alzheimer's Diagnosis Classifier 🧠

## About the Project 🔰
In this project, I have built and compared various Machine Learning **Classification** models to predict the diagnosis of **Alzheimer's Disease** and also performed **Exploratory Data Analysis** which gives insight about all the features present in the data. This project is built using [Alzheimers Disease Dataset](https://www.kaggle.com/datasets/rabieelkharoua/alzheimers-disease-dataset). You can also visit this notebook at [Kaggle](https://www.kaggle.com/code/ranjeetsohanpal/alzheimers-classifier-eda-gridsearch).The entire project is built using Python programming language.

### Project workflow
The first step involves the EDA to have insights about the features and find out which features actually significantly contribute to the target variable. In this dataset,there is no correlation among the features which makes the part of Feature Engineering easier.

#### Important Insights from the Project : 
1. It is medically proven that risk of Alzheimers increases with [Age](https://www.nia.nih.gov/health/alzheimers-causes-and-risk-factors/what-causes-alzheimers-disease#:~:text=Age%20is%20the%20biggest%20known,their%20risk%20of%20Alzheimer's%20increases.), however from the data it is observed that there is no correlation with age as there are equal percentage of cases from age of 60 - 90 years. ![Percentage of Diagnosed Patients in different Age bins](/images/age_plot.png)

2. The **education level** of the patient does not play a significant role in the diagnosis of Alzheimer's. It is observed that patients who have **no formal education**, there are about **38 %** that are diagnosed. In case of patients with **higher education**, there are about **33%** cases. The percentage of cases from each education level drops as the level increases, however the decrement is not that prominent.![Percentage of Diagnosed Patients by Education level](/images/edu_level.png)


3. It is possible to predict to diagnosis only on the basis of **Cognitive Assessments** irrespective of the lifestyle and medical history of the patient. In the given data, it is found that there is **no contribution** of the features related to the **lifestyle** (smoking, alcohol consumption) and **medical history**(whether there is history of Alzheimer's in the family).In fact, the **symptoms** associated with Alzheimer's are not prominent in predicting the diagnosis. This results in having only fewer features which significantly makes the training of model easier.
![ADL score Swarm Plot](/images/adl_score.png)
We can also observe it from the Pearson Correlation Plot for Diagnosis.
![Pearson Correlation with Diagnosis](/images/pearson.png)   

#### Models And Evaluation :
First of all the data was split into train and test data to build the model. Since this is a skewed classification problem, metrics such as confusion matrix, precision and recall are used to evaluate the models. This project involves predicting the diagnosis, so the model must be able to identify the actual positive cases as much as possible.Therefore, the aim is to have the precision of the model as high as possible since false negatives imply missed patients which actually require diagnosis but missed by the model.

**Precision** = $\\frac{\text{True Positives}}{\text{True Positives} + \text{False Negatives}}\$

***Evaluation Result of Models :***

| Serial No. | Model                 | Precision |
|------------|-----------------------|-----------|
| 1          | Logistic Regression   | 0.85      |
| 2          | Decision Tree         | 0.95      |
| 3          | Random Forest         | 0.96      |
| 4          | Gradient Boost        | 0.96      |


## Libraries Used 📚
  1. Pandas
  2. MatplotLib/Seaborn
  3. Scikit-Learn

### Installation 
You can clone this repo by using the following command: 
    `git clone https://github.com/ranjeetsohanpal/Alzheimers-Classification.git`

### Usage
I believe this project could be deployed to a web application or software to predict the diagnosis of the patients. The relevant features used in the model could be given as the input. I will also try to make a web application in the future to deploy this model.

## Contributing 🤝
In case, you are interested in contributing and collaborating on this project, please do contact me on [LinkedIn](www.linkedin.com/in/ranjeetsinghiitrpr)

## License 📃
This Notebook has been released under the [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0) open source license.

## Thank You 🙏
