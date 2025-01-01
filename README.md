# CODTECH-Task1
Name = RAJESH
Company = CODETECH IT SOLUTION
ID = CT6WDS2689
Domain = ARTIFICAL INTRLLIGENCE
Duration = DECEMBER 5TH 2024 TO JANUARY 20TH 2025
Mentor = NEELA SANTHOSH KUMAR

Overview of Data Preprocessing :

This Python code demonstrates a series of important data preprocessing techniques using the pandas and numpy libraries to prepare a dataset for machine learning tasks. The dataset in question includes information on customer demographics, such as age, salary, city, and whether they purchased a product. Below is a detailed breakdown of each step performed in the code:
1. Handling Missing Data:

   1). Objective: To deal with missing or NaN values in the dataset.
   2). Approach:
        Numerical Columns: Missing values in the 'Age' and 'Salary' columns are filled with the mean value of the respective column. This ensures that the dataset does not have gaps that could interfere with model training.
        Categorical Columns: Missing values in the 'City' column are replaced with the most frequent value (mode) of the column, ensuring that the categorical data remains consistent.

2. Encoding Categorical Data:

   1). Objective: To convert categorical variables into a numerical format that can be used in machine learning models.
   2). Approach:
        The 'City' column, which contains categorical data (e.g., 'New York', 'Los Angeles', 'Chicago'), is transformed using One-Hot Encoding. This process creates binary (0 or 1) columns for each city. The parameter drop_first=True ensures that the first city (New York) is dropped to avoid multicollinearity.

3. Scaling Numerical Features:

   1). Objective: To normalize numerical data, making it easier for machine learning algorithms to process.
   2). Approach:
        The 'Age' and 'Salary' columns are scaled using Min-Max Scaling, which transforms these features into a range between 0 and 1. This ensures that the features are comparable in magnitude and prevents one feature from dominating the model due to differences in scale.

4. Splitting the Data into Training and Test Sets:

   1). Objective: To divide the dataset into training and test sets to evaluate the performance of machine learning models.
    2).Approach:
        The data is manually split into an 80% training set and a 20% testing set. This allows the model to be trained on one portion of the data and validated on another unseen portion, providing an unbiased evaluation.
        The features (input variables) are separated from the target variable 'Purchased', which is encoded into binary values (1 for 'Yes', 0 for 'No').

5. Displaying the Processed Data:

    After all preprocessing steps are completed, the code prints out the training features, training target, test features, and test target to give an overview of the prepared dataset. This output is useful for verifying that the preprocessing steps were correctly applied and that the data is ready for model training.
