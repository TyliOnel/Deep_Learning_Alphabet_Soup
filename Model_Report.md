# Week 21 Deep Learning 
## Charity Funding Predictor

## **Overview**

The aim of this project is to develop an algorithm utilizing machine learning and neural networks to predict whether applicants will succeed if funded by the fictional non-profit foundation, Alphabet Soup.

## **Data Preprocessing**

The CSV file contains data on over 34,000 organizations that have received funding from Alphabet Soup, along with several columns of metadata for each organization.

### **Preprocessing**

To prepare the data for analysis, I performed the following steps:

    - Dropped non-beneficial columns.

    - Analyzed the number of data points for each unique value in the APPLICATION_TYPE and CLASSIFICATION columns, which had more than 10 unique values.

    - Chose cutoff points of 500 and 1850 respectively to bin rare categorical values into a new category called "Other".

    - Used pd.get_dummies() to convert categorical data into numeric form.

    - Split the data into target (IS_SUCCESSFUL) and feature arrays.

    - Applied train_test_split to create training and testing datasets.

    - Utilized StandardScaler to standardize the training and testing sets.

The preprocessing resulted in 44 features. The target variable was IS_SUCCESSFUL, and the data was divided into training and test subsets.

### Data Preprocessing Questions

What variable(s) are the target(s) for your model?
    - Target variable was the IS_SUCCESSFUL column
What variable(s) are the features for your model?
    - Every column that was not dropped were the features fed into the model
What variable(s) should be removed from the input data because they are neither targets nor features?
    - - 'EIN' & 'NAME'

## **Compiling, Training, and Evaluating the Model**

The objective was to achieve a predictive accuracy above 75%. I conducted seven official attempts using machine learning and neural network techniques. 
Each attempt resulted in an accuracy rate of approximately 72%, falling slightly short of the target accuracy. 


### Results from each model attempt are detailed below:

How many neurons, layers, and activation functions did you select for your neural network model, and why?


#### *ATTEMPT #1*

The first attempt (AlphabetSoupCharity_model_1.h5) resulted in an accuracy 
score of 73.3%.
 
The hyperparameters used were: 
• layers = 2 
o layer1 = 80 neurons and ‘relu’ activation function 
o layer2 = 30 neurons and ‘relu’ activation function 
• epochs = 100 
 
 ![alt text](/Accuracy_Charts/image.png)
  
 #### *ATTEMPT #2*

The first attempt (AlphabetSoupCharity_model_2.h5) resulted in an accuracy 
score of 73.7%. This was the highest accuracy score of the seven models.
 
The hyperparameters used were: 
• layers = 2 
o layer1 = 6 neurons and ‘relu’ activation function 
o layer2 = 3 neurons and ‘relu’ activation function 
• epochs = 100 

![alt text](/Accuracy_Charts/image-1.png)
 

#### *ATTEMPT #3*

The first attempt (AlphabetSoupCharity_model_3.h5) resulted in an accuracy 
score of 73.6%.
 
The hyperparameters used were: 
• layers = 2 
o layer1 = 250 neurons and ‘relu’ activation function 
o layer2 = 250 neurons and ‘relu’ activation function 
• epochs = 100 

![alt text](/Accuracy_Charts/image-2.png)
 
  
#### *ATTEMPT #4*

The first attempt (AlphabetSoupCharity_model_4.h5) resulted in an accuracy 
score of 72.4%. 
 
The hyperparameters used were: 
• layers = 3 
o layer1 = 80 neurons and 'relu' activation function 
o layer2 = 60 neurons and 'sigmoid' activation function
o layer3 = 10 neurons and 'sigmoid' activation function  
• epochs = 100 

![alt text](/Accuracy_Charts/image-3.png)
 
 
####  *ATTEMPT #5*

The first attempt (AlphabetSoupCharity_model_5.h5) resulted in an accuracy 
score of 72.3%.
 
The hyperparameters used were: 
• layers = 3 
o layer1 = 10 neurons and 'relu' activation function 
o layer2 = 80 neurons and 'relu' activation function
o layer3 = 60 neurons and 'relu' activation function  
• epochs = 100

![alt text](/Accuracy_Charts/image-4.png)
 
  
#### *ATTEMPT #6*

The first attempt (AlphabetSoupCharity_model_6.h5) resulted in an accuracy 
score of 61.7%. This was the lowest accuracy score of the seven models.
 
The hyperparameters used were: 
• layers = 3 
o layer1 = 20 neurons and 'relu' activation function 
o layer2 = 27 neurons and 'sigmoid' activation function
o layer3 = 3 neurons and 'sigmoid' activation function  
• epochs = 100 
 
 ![alt text](/Accuracy_Charts/image-5.png)
 

 ####  *ATTEMPT #7*

The first attempt (AlphabetSoupCharity_model_7.h5) resulted in an accuracy 
score of 61.9% 
 
The hyperparameters used were: 
• layers = 2 
o layer1 = 80 neurons and ‘relu’ activation function 
o layer2 = 30 neurons and ‘relu’ activation function 
• epochs = 100 
 
![alt text](/Accuracy_Charts/image-6.png)


### Were you able to achieve the target model performance?
    No (did not reach 75%)

### What steps did you take in your attempts to increase model performance?
    I changed the number of columns dropped, the cutoff points and the different amount of layers and neurons used.

## Summary

Despite seven attempts, the model was unable to achieve a predictive accuracy higher than 73.7%. The only big difference I was able to see in the different models was when I dropped extra columns the model ran faster and was less accurate. Changing the the cutoff points and the different amount of layers had little to no affect on the accuracy result for the model. Perhaps increasing the data or amending the approach, using different functions within Keras and Tensorflow on the appropriate data will better predict the success of applicants funded by Alphabet Soup.