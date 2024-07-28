# Food-Component-Classification

## Introduction
This project aims to classify food components based on their ingredients and potential allergens. The goal is to develop a predictive model that can accurately determine whether a food product contains allergens based on its listed components. This README provides an overview of the data preprocessing, modeling steps, and results.

## Dataset
The dataset food_ingredients_and_allergens.csv is used, containing detailed information about various food products, including their main ingredients, sweeteners, fats/oils, seasonings, allergens, and the predicted allergen content.

## Data Preprocessing

### Initial Data Exploration:
The dataset's shape, the presence of null values, and duplicates are checked.
Columns in the dataset are listed along with their unique values.
Duplicate rows are removed from the dataset.

### Handling Specific Conditions:
Rows where 'Allergens' is 'None' but 'Prediction' is 'Contains' are corrected to 'Does not contain'.

### Feature Encoding:
Features are encoded to numerical labels using mapping and the LabelEncoder.
Frequency counts for categorical columns (e.g., 'Food Product', 'Main Ingredient') are calculated and mapped back to the DataFrame.

### Feature Selection:
Unnecessary columns are dropped, leaving only the frequency counts and the target variable 'Prediction'.

## Data Visualization
### Pairplot:
A pairplot is created to visualize the relationships between features, colored by the 'Prediction' column.

### Correlation Heatmap:
A heatmap is generated to show the correlation between features.

## Model Building
### Splitting the Data:
The dataset is split into features (X) and the target (y).
The data is further split into training and testing sets.

### Training the Model:
A Decision Tree Classifier is chosen.
Grid Search Cross-Validation is used to find the best parameters (criterion and max_depth).
The best model is trained on the training data.

### Model Evaluation:
The model is evaluated using the test data.
Metrics such as accuracy, precision, recall, and F1-score are calculated.
A confusion matrix is generated.

## Results
### Best Parameters:
Criterion: gini
Max Depth: 1
### Best Score:
0.996

### Accuracy:
100.00%

## Conclusion
The Decision Tree Classifier achieved an accuracy of 100.00% on the test set, indicating perfect classification performance for this dataset. This model can accurately classify the presence of allergens in food products based on their ingredients.
