# Iris Dataset Classification using Logistic Regression  

This project focuses on building a multi-class classification model for the **Iris dataset** using **logistic regression**, both from scratch and using Scikit-learn's built-in tools. The aim is to classify the three Iris species (Setosa, Versicolor, and Virginica) based on their sepal and petal dimensions.                  
     
## Project Overview     
  
The project demonstrates: 
1. **Data Cleaning**: Preparing the Iris dataset for machine learning by handling irrelevant features and encoding target variables.
2. **Feature Scaling**: Standardizing features for better convergence in logistic regression.
3. **Multi-Class Logistic Regression**:
   - **From Scratch**: Implementing logistic regression with gradient descent and binary cross-entropy loss.  
   - **Scikit-learn**: Comparing custom implementation with the library implementation. 
4. **Evaluation**: Assessing the model's accuracy, precision, recall, and F1-score using classification metrics. 
 
## Table of Contents 

- [Installation](#installation)
- [Dataset](#dataset)
- [Project Workflow](#project-workflow)
- [Key Results](#key-results)
- [Conclusion](#conclusion)  
- [License](#license)

## Installation

To run this project, ensure you have the following libraries installed:

```bash
pip install numpy pandas matplotlib scikit-learn
```

## Dataset

The **Iris dataset** is a classic dataset for classification tasks, consisting of 150 samples with the following features:
- `SepalLengthCm`: Length of the sepal.
- `SepalWidthCm`: Width of the sepal.
- `PetalLengthCm`: Length of the petal.
- `PetalWidthCm`: Width of the petal.
- `Species`: Target variable with three classes:
  - `Iris-setosa`
  - `Iris-versicolor`
  - `Iris-virginica`

## Project Workflow

### Step 1: Data Preprocessing
- Removed unnecessary columns (`Id`).
- One-hot encoded the `Species` column for multi-class logistic regression.

### Step 2: Feature Scaling
- Standardized the features (`SepalLengthCm`, `SepalWidthCm`, `PetalLengthCm`, `PetalWidthCm`) using **StandardScaler** for better performance during gradient descent.

### Step 3: Logistic Regression from Scratch
- Implemented logistic regression for binary classification using:
  - Sigmoid hypothesis function.
  - Binary cross-entropy cost function.
  - Gradient descent optimization.
- Extended the binary logistic regression to a multi-class setting by training three binary classifiers:
  - One for each class (`Setosa`, `Versicolor`, `Virginica`) using a one-vs-rest approach.

### Step 4: Prediction
- Predicted class probabilities for each sample using trained weights.
- Assigned the class with the highest probability to each sample.

### Step 5: Evaluation
- Calculated classification metrics:
  - Accuracy
  - Precision
  - Recall
  - F1-Score
- Compared results with the Scikit-learn implementation of logistic regression.

## Key Results

- **Custom Implementation**:
  - Test Accuracy: **90%**
  - Classification Metrics:
    ```
                  precision    recall  f1-score   support

      versicolor       0.88      0.78      0.82         9
          setosa       1.00      1.00      1.00        10
       virginica       0.83      0.91      0.87        11

        accuracy                           0.90        30
       macro avg       0.90      0.90      0.90        30
    weighted avg       0.90      0.90      0.90        30
    ```

- **Scikit-learn Implementation**:
  - Similar accuracy and classification metrics as the custom implementation, demonstrating the correctness of the scratch-built model.

## Conclusion

This project showcases:
- The power of logistic regression for multi-class classification using a one-vs-rest approach.
- How to implement gradient descent and evaluate a model's performance.
- The importance of feature scaling in improving model convergence.

Future enhancements could include:
- Comparing logistic regression with other classifiers like SVM or decision trees.
- Visualizing decision boundaries to gain deeper insights.

## License

This project is licensed under the MIT License.
