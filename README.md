# Plant Disease Classification using PySpark
> [CIE 427] Big Data Analytics Course Project @ Fall 2022 - Zewail City

This project uses PySpark to develop a mobile illness diagnostics tool for plant disease classification, aiming to improve crop yields by providing accessible and affordable solutions for farmers.

## Getting Started

Due to the extensive library downgrades required, I was unable to run the project on Google Colab and instead executed it on my local machine.

### Prerequisites

You will need to have the following frameworks:

```
Python 3.5 or Python 3.6 
Spark 2.4.0
Hadoop 2.7
Java 8
jdk1.8.0_202
jre1.8.0_202
tensorflow==1.15.0
keras==2.2.5
pyspark==2.4.0
pic2vec==0.101.1
```

### Step by Step

- **Download Data**: Download the [dataset](https://www.kaggle.com/datasets/vipoooool/new-plant-diseases-dataset) from Kaggle using Kaggle API and initialize data and code folders to retrieve data.
- **Data Preprocessing**: Perform categorical name changes of plants using ordinal encoding to facilitate easy model training.
- **Feature Extraction**: Utilize pic2vec for feature extraction from each image using Xception Network. The resulting output should consist of label and feature columns, both of which are quantitative.
- **Split Data**: Split the dataset into training and testing sets with proportions of 0.7 and 0.3, respectively. Ensure there is no overlapping between the two sets to prevent data leakage.
- **Training Data**: Train the dataset using Logistic Regression based on OneVsRest Classifier.
- **Evaluating Data**: Evaluate the dataset using different metrics generated from the model summary, including Accuracy, ROC curve, and F1-score.
- **Hyperparameter Tuning**: Attempted hyperparameter tuning, but it took too much time to retrieve results.

## Code Files

Explain how to run the automated tests for this system

- **[1- Augmentation and Feature Extraction.ipynb](https://github.com/ahmedlila/Plant-Disease-Classification-using-PySpark/blob/main/1-%20Augmentation%20and%20Feature%20Extraction.ipynb)**: Data Preparation and Feature Extraction Modules.
- **[2- Analysis and Training.ipynb](https://github.com/ahmedlila/Plant-Disease-Classification-using-PySpark/blob/main/2-%20Analysis%20and%20Training.ipynb)**: Model Training and Evaluation Modules.

## Deployment

We uploaded half of the data to S3 socket at AWS, applied the model on it, and connected using Putty and SSH to the AWS server for model execution. The model achieved an accuracy of 97% and completed around 108 tasks for processing.
