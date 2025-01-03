# Practical Machine Learning Course Project

## **Overview**
This project is part of the Coursera Practical Machine Learning course. It involves building a predictive model to classify how individuals perform barbell lifts using data collected from accelerometers on various parts of the body. The project demonstrates the application of machine learning techniques to real-world sensor data.

## **Data**
The dataset used in this project was sourced from the Weight Lifting Exercise Dataset provided by Groupware@LES, PUC-Rio. It contains measurements from wearable devices capturing movement data of six participants performing barbell lifts.

- **Training data:** [pml-training.csv](https://d396qusza40orc.cloudfront.net/predmachlearn/pml-training.csv)
- **Test data:** [pml-testing.csv](https://d396qusza40orc.cloudfront.net/predmachlearn/pml-testing.csv)

For more information, visit the [Weight Lifting Exercise Dataset](http://groupware.les.inf.puc-rio.br/har).

## **Objective**
The goal of this project is to predict the `classe` variable, which represents the manner in which an exercise is performed. This is achieved by training a machine learning model on the training dataset and applying it to classify 20 test cases.

## **Analysis Workflow**

### **1. Data Cleaning and Preprocessing**
- Columns with more than 50% missing values were removed.
- Near-zero variance features were excluded.
- Irrelevant columns such as timestamps and IDs were dropped.

### **2. Exploratory Data Analysis**
- The distribution of the target variable (`classe`) was visualized to ensure balance across categories.

### **3. Model Development**
- A Random Forest model was trained with the following specifications:
  - **500 trees**
  - Optimized `mtry` parameter set to the square root of the number of features.

### **4. Model Evaluation**
- The model achieved an accuracy of **99.92%** on the test subset.
- Most misclassifications occurred between classes `C` and `D`.

### **5. Feature Importance**
- Key features identified:
  - `roll_belt`
  - `yaw_belt`
  - `pitch_belt`
- These features significantly contributed to the model's high accuracy.

### **6. Predictions**
- Predictions were made for the 20 test cases, and the results were saved for submission.

## **Files**
- `pml-training.csv`: Training dataset.
- `pml-testing.csv`: Test dataset.
- `analysis.Rmd`: R Markdown file containing the code and analysis.
- `analysis.html`: Compiled HTML report of the analysis.

## **How to Run**
1. Clone this repository to your local machine.
2. Ensure R and the required libraries (`caret`, `randomForest`, `ggplot2`) are installed.
3. Open `analysis.Rmd` in RStudio and knit it to generate the HTML report.

## **References**
- Groupware@LES, PUC-Rio. "Weight Lifting Exercise Dataset." [http://groupware.les.inf.puc-rio.br/har](http://groupware.les.inf.puc-rio.br/har)
- Coursera Practical Machine Learning Course. "Course Project Instructions." [Course Link](https://www.coursera.org/learn/practical-machine-learning/)

## **Author**
Godwin Osuji
