# Neural Network Charity Analysis
## Overview
The purpose of this project was to have a look at deep-learning neural networks to analyze and classify the success of charitable donations. We decided to preprocess the data to run in the neural network model. After cleaning the data we decided to compile and train then evaluate the neural network model to see its accuracy on successful donations. Lastly, after looking at the model's accuracy we decided to see if we could optimize this model to enhance it's capabilities. 

## Results
### Data Preprocessing
- Columns "EIN" and "NAME" were neither targets or features and were removed from the data
- Columns "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION", "STATUS", "INCOME_AMT", "SPECIAL_CONSIDERATIONS" were the features of our model. Encoding of these catergorical variables, standardization, and splitting into training and testing datasets were applied to these features. 
- Columns "IS_SUCCESSFUL" was the target of our deep learning neural network since it contained binary data that showed wheter or not the donation was used properly. 

### Compiling, Training, and Evaluating the Model
- The deep learning neural network was made of two hidden layers one that contained 80 neurons and the other containing 30. The input data contained 43 features and 25,724 samples. We checked this by using "X_train_scaled.shape". From this we used the ReLU activation function for the hidden layers. Since our output is binary, classification we used the sigmoid function.
- From this we got an accuracy of 73%
- To optimize this model and increase performance we tried three different changes to the model,
1. Increased the number of neurons in the hidden layer 1 from 80 -> 100, the result,

![Image 1](https://github.com/mckjack/Neural_Network_Charity_Analysis/blob/main/Images/Adding%20more%20neurons.png)

2. Added a third hidden layer to our model, the result,
![Image 2](https://github.com/mckjack/Neural_Network_Charity_Analysis/blob/main/Images/3rd%20Hidden%20Layer.png)

3. Used the tanh activation function instead of the ReLU, the result, 
![Image 3](https://github.com/mckjack/Neural_Network_Charity_Analysis/blob/main/Images/Different%20Function.png)

## Summary 
In conclusion, based upon the three ideas to optimize the model we still could not achieve an accuracy of 75% as intended. A suggestion could hint towards using a supervised machine learning model since we our target is still binary classification. These models could include either a Support Vector Machine learning model or a Random Forest Classifier. We could test these models and compare it to our deep learning neural network model to see if the supervised ones are more accurate. 
