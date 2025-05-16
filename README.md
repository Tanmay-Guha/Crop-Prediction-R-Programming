# Crop Prediction System using R

## Overview

This project utilizes **machine learning algorithms in R** to predict the most suitable crop based on environmental conditions. It is designed to assist in smart agricultural practices and precision farming. The project covers data analysis, visualization, model building, and evaluation using various supervised and unsupervised learning techniques.

## Features

- Data preprocessing and visualization using `ggplot2` and `GGally`
- Classification using:
  - K-Nearest Neighbors (KNN)
  - Logistic Regression
  - Naive Bayes
- Model evaluation using confusion matrix, accuracy, precision, recall, and F1-score
- Implementation of clustering using K-Means and the Elbow Method
- Workflow includes data wrangling, training, testing, and deployment simulation

## Technologies Used

- **R programming**
- **RStudio IDE**
- **Machine Learning packages**: `caret`, `e1071`, `caTools`, `class`, `lattice`
- **Visualization**: `ggplot2`, `GGally`

## Dataset

A CSV dataset is used containing:
- Soil nutrients (N, P, K)
- Temperature
- Humidity
- pH level
- Rainfall
- Crop labels (target variable)

Example row:
```
N  P  K temperature humidity ph rainfall label
90 42 43   20.88       82.00   6.5  202.93  rice
```

## Project Workflow

1. **Data Collection**
2. **Preprocessing & Visualization**
3. **Data Splitting**
4. **Model Training**
5. **Prediction & Evaluation**
6. **Model Comparison**
7. **Results Output**

## How to Run

1. **Install R and RStudio**
2. **Install required packages**:
```r
install.packages(c("ggplot2", "GGally", "caTools", "class", "caret", "lattice", "e1071"))
```
3. **Load the dataset**:
```r
data <- read.csv("data.csv")
```
4. **Split, train and test the models**:
```r
library(caTools)
split <- sample.split(data, SplitRatio = 0.7)
train_cl <- subset(data, split == TRUE)
test_cl <- subset(data, split == FALSE)
```
5. **Run KNN, Naive Bayes, or Logistic Regression models**
6. **Evaluate using confusion matrix and metrics**

## Sample Output

- Classification accuracy up to **99.3%** using Naive Bayes
- Visual correlation plots using `ggpairs()`
- Confusion Matrix and classification report output

## Authors & Acknowledgments

- Project Authors: TANMAY GUHA
- Email: tanmayguha15@gmail.com
- LinkedIn Profile: https://www.linkedin.com/in/tanmay-guha-ba431833a
- Libraries: caret, e1071, ggplot2, GGally, etc.
- Tools: R, RStudio
- Thanks to the open-source R community

## License

This project is for educational and non-commercial use.