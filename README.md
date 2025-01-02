# Health-Insurance-Charge
Health Insurance Charge Prediction

The notebook contains the details and processes used to predict the cost of insurance based on certain features
![image](https://github.com/user-attachments/assets/6d798e5d-401e-4f75-a69d-85018b4ed713)

As part of the preprocessing, the data cleaning involved standardizing the data structure and removing null data.
Some of the identified issues with the data are:
- The number of rows available is inconsistent, there are missing values in the dataset.
- The naming convention for the regions that are written is inconsistent and has to be standardized.
- The data type as seen from the info for smokers is an object, that can be changed to a boolean for convenience.
- It can be noted that from looking at the first 5 rows of the data, the charges column has some values with currency and others without.
- The data type as seen from the info for charges is an object, hence why the numeric description is not available.

For data visualization, a pair plot was created using the Seaborn library
![image](https://github.com/user-attachments/assets/97d8a370-9a33-4446-a1b7-11a50add9d49)

Just before rounding off data wrangling, samples of the data were selected and it was discovered that there is a negative value in the age column. This could be a typographical error. It was decided that the absolute error of the data should be gotten considering that the numerical values in this dataset should be positive.
![image](https://github.com/user-attachments/assets/90175d5a-16c0-4245-813d-a9fdeb17e33d)

3 regression models namely Linear Regression, Ridge Regression, and LARS Lasso Regression were initialized and fitted on the training data. The models were used to predict based on the test data and the respective R2Scores were computed.
The best-performing model was the Ridge Regression model with 0.697672 R2Score. 
The model was applied to the validation data to predict the charges of insurance based on the features. 
There was an instruction to handle any negative values by replacing them with the minimum basic charge, set at 1000. Also, save the data frame as validation_data. 
This led to the decision to set the predicted charges to the basic charge of 1000 if the charge is less than 1000. 
![image](https://github.com/user-attachments/assets/2e4d5c7e-ef6b-466c-a84a-7db3a70cb115)

More information about the data and the resulting model can be found here: https://github.com/juwonlo-tech/Health-Insurance-Charge/blob/main/Health_Insurance_Prediction.ipynb



