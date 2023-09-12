# Student-Loan-Risk-Deep-Learning

### Resources: https://static.bc-edx.com/mbc/ai/m6/datasets/student_loans.csv
### Tools: Python, Pandas, SciKit-Learn, TensorFlow, Keras

## Goal
If a company can predict whether a borrower will pay their loan in full, it can provide a more accurate interest rate for the borrower. The goal of this model is to use neural networks to predict student loan repayment. 

## Steps:
### Prepare the Data for Use on a Neural Network Model
* The student_loans.csv file is read into a Pandas DataFrame.

![image](https://github.com/emaynard10/Student-Loan-Risk-Deep-Learning/assets/99676466/ab03f9ef-0075-417e-82db-db2b3a1aed28)

* Two datasets are created: a target (y) dataset, which includes the "credit_ranking" column, and a features (X) dataset, which includes the other columns.

![image](https://github.com/emaynard10/Student-Loan-Risk-Deep-Learning/assets/99676466/d31a5c47-7f84-43bd-aed4-bc50ea483528)

![image](https://github.com/emaynard10/Student-Loan-Risk-Deep-Learning/assets/99676466/849862ef-555f-4f9a-b133-2c07d26aa324)


* The features and target sets have been split into training and testing datasets.

![image](https://github.com/emaynard10/Student-Loan-Risk-Deep-Learning/assets/99676466/fa1d5d0b-02ed-4e64-a128-f71ca122946a)

* Scikit-learn's StandardScaler was used to scale the features data.

![image](https://github.com/emaynard10/Student-Loan-Risk-Deep-Learning/assets/99676466/1b7575df-ba81-4176-a9e8-3df009ed635d)

### Compile and Evaluate the Model Using a Neural Network 
* A deep neural network is created with appropriate parameters.

![image](https://github.com/emaynard10/Student-Loan-Risk-Deep-Learning/assets/99676466/9c4f3700-3c17-4fe4-834f-57a29764723f)

* The model is compiled and fit using the mse loss function, the adam optimizer, the mse evaluation metric, and a small number of epochs.

![image](https://github.com/emaynard10/Student-Loan-Risk-Deep-Learning/assets/99676466/ca120005-b40d-4989-b290-ac0aab8e9d91)

* The model is evaluated using the test data to determine its loss and accuracy.

![image](https://github.com/emaynard10/Student-Loan-Risk-Deep-Learning/assets/99676466/fbb2b4c9-5dc4-444d-a9cc-e53b7a9319e0)

* The model is saved and exported to an HDF5 file named student_loans.h5. 

### Predict Loan Repayment Success by Using your Neural Network Model
* The saved model is reloaded.
* The reloaded model is used to make predictions on the testing data.
* A DataFrame shows both the predictions and the actual values.

![image](https://github.com/emaynard10/Student-Loan-Risk-Deep-Learning/assets/99676466/a4b56bac-8786-4c58-8f8a-b1e9217a8b01)


## Usage

## Future Considerations
To improve the model, I could tune the model by adjusting the following: 
1. Acitivation Functions: I began with ReLu for the hidden layers. The target columns is continuous so this is a good place to start. 
2. Number of Layers and Neurons: I could see if increasing the nmber of neurons or hidden nodes leads to overfitting.
3. Batch Size: I didn't specify so the default is 32.
4. Epochs: I ran the model with 50 epochs, but could try to see if there are changes when that is increased to 100.
5. Learning Rate and Optimizer: I ran the model using Adam, but could also adjust this parameter.


