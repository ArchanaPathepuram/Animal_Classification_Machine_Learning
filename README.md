# Automated Animal Species Classification

This project uses machine learning to classify animals into different categories based on their physical and biological characteristics. I worked with the Zoo dataset and implemented multiple classification algorithms to compare their performance and identify a suitable model for animal classification.

## About the Project

The project predicts an animal's class using features such as hair, feathers, eggs, milk, aquatic nature, number of legs, tail, and other characteristics.

I explored the dataset, visualized the relationships between features, trained different machine learning models, and compared their performance using evaluation metrics. I also tested the Random Forest model on an unseen dataset to check how it performed on additional data.

## Animal Classes

The model classifies animals into seven categories:

- Mammal
- Bird
- Reptile
- Fish
- Amphibian
- Bug
- Invertebrate

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib
- Jupyter Notebook / Google Colab

## Machine Learning Models

I implemented and compared the following classification algorithms:

- Logistic Regression
- Decision Tree Classifier
- K-Nearest Neighbors (KNN)
- Gaussian Naive Bayes
- Support Vector Machine (SVM)
- Random Forest Classifier

I also used GridSearchCV to tune hyperparameters for the Decision Tree and KNN models.

## Project Workflow

1. Loaded the Zoo dataset using Pandas.
2. Checked missing values and explored the dataset.
3. Performed exploratory data analysis using charts, count plots, box plots, and a correlation heatmap.
4. Separated the input features from the target class.
5. Split the dataset into training and testing sets.
6. Trained multiple classification models.
7. Evaluated the models using accuracy, confusion matrices, classification reports, and cross-validation.
8. Used GridSearchCV to find suitable hyperparameters for selected models.
9. Tested the Random Forest model on an unseen dataset.
10. Saved the trained Random Forest model using Joblib.

## Model Performance

The notebook reports the following test accuracies for the main model comparison:

| Model | Test Accuracy |
|---|---:|
| Logistic Regression | 96.77% |
| Decision Tree | 93.55% |
| K-Nearest Neighbors | 93.55% |
| Gaussian Naive Bayes | 96.77% |
| Support Vector Machine | 93.55% |
| Random Forest | 96.77% |

The Random Forest model achieved **96.77% test accuracy** in the recorded evaluation. On the separate unseen dataset, the notebook reports **92.86% accuracy** and a macro one-vs-rest ROC-AUC score of **0.9881**.

These results are from the notebook's recorded outputs and may vary when the code is run with different data splits or updated datasets.

## Dataset and Features

The project uses `zoo.csv` as its main dataset and `unseen_all7classes_animals.csv` for the unseen-data evaluation.

The input features include:

- Hair and feathers
- Eggs and milk
- Airborne and aquatic characteristics
- Predator and toothed characteristics
- Backbone and breathing
- Venomous and fins
- Number of legs and tail
- Domestic nature and body size (`catsize`)

The target variable is `class_type`. The `animal_name` column is excluded from model training.

**Note:** Both CSV files must be available in the expected locations before running the corresponding notebook cells.

## Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/ArchanaPathepuram/Animal_Classification_Machine_Learning.git
cd Animal_Classification_Machine_Learning
```

### 2. Install the required libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn joblib jupyter
```

### 3. Add the datasets

Place `zoo.csv` in the location expected by the notebook. For the unseen-data evaluation, make sure `unseen_all7classes_animals.csv` is also available and update its path if needed.

### 4. Run the notebook

Open the notebook in Jupyter Notebook or upload it to Google Colab. Run the cells in order.

## Saved Model

The notebook saves the trained Random Forest model as:

```text
zoo_random_forest.pkl
```

The saved model can be loaded using Joblib for later predictions, provided the input features are supplied in the same order and format used during training.

## Future Improvements

- Build a simple web interface to classify animals from their characteristics.
- Add input validation and clearer prediction results.
- Improve model evaluation using repeated cross-validation.
- Organize the training and prediction code into reusable Python modules.
- Add visualizations comparing model performance.

## Author

**Archana Pathepuram**

GitHub: [ArchanaPathepuram](https://github.com/ArchanaPathepuram)

Project Repository: [Animal Classification Machine Learning](https://github.com/ArchanaPathepuram/Animal_Classification_Machine_Learning)
