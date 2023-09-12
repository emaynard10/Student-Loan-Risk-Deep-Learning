# Student-Loan-Risk-Deep-Learning

### Resources: https://static.bc-edx.com/mbc/ai/m6/datasets/student_loans.csv
### Tools: Python, Pandas, SciKit-Learn, TensorFlow, Keras, Linear Regression

## Steps:
### Prepare the Data for Use on a Neural Network Model
* The student_loans.csv file is read into a Pandas DataFrame.
* Two datasets are created: a target (y) dataset, which includes the "credit_ranking" column, and a features (X) dataset, which includes the other columns.
* The features and target sets have been split into training and testing datasets. 
* Scikit-learn's StandardScaler was used to scale the features data.

### Compile and Evaluate a Binary Classification Model Using a Neural Network 
* A deep neural network is created with appropriate parameters. 
* The model is compiled and fit using the mse loss function, the adam optimizer, the mse evaluation metric, and a small number of epochs.
* The model is evaluated using the test data to determine its loss and accuracy.
* The model is saved and exported to an HDF5 file named student_loans.h5. 

### Predict Loan Repayment Success by Using your Neural Network Model
* The saved model is reloaded.
* The reloaded model is used to make predictions on the testing data.
* A DataFrame shows both the predictions and the actual values.

## Usage

## Future Considerations
