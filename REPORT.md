# Report on the Neural Network Model  
## Overview
- The purpose of this analysis is to create a deep learning neural network model that can help the nonprofit foundation Alphabet Soup to select the applicants for funding with the best  chance of success in their ventures.  
- The dataset is a CSV containing more than 34,000 organizations that have received funding from the foundation over the years. Within the dataset, there are 11 columns and 34299 rows.
- this is how our data looks:  
<img src="./images/df_info.png" alt="drawing" width="300"/>
- For the Neural Network Model we utilized the `Sequential` from `Keras`  
- The aim was to achieve the highest accuracy which we achieved by using a tuner


## Results  
- Data Preprocessing
    - What variable(s) are the target(s) for your model?
        - My aim is to create a neural network model to predict the `IS_SUCCESSFUL`
    - What variable(s) are the features of your model?
        - The dataset contained the following features:  
        - `EIN` and `NAME`—Identification columns  
        - `APPLICATION_TYPE`—Alphabet Soup application type  
        - `AFFILIATION`—Affiliated sector of industry  
        - `CLASSIFICATION`—Government organization classification  
        - `USE_CASE`—Use case for funding  
        - `ORGANIZATION`—Organization type  
        - `STATUS`—Active status INCOME_AMT—Income classification  
        - `SPECIAL_CONSIDERATIONS`—Special considerations for application  
        - `ASK_AMT`—Funding amount requested  
        - `IS_SUCCESSFUL`—Was the money used effectively  
    - What variable(s) should be removed from the input data because they are neither targets nor features?  
        - We dropped `EIN` and `NAME` since they are for identification.
- Compiling, Training, and Evaluating the Model
    - How many neurons, layers, and activation functions did you select for your neural network model, and why? 
        -  
    - Were you able to achieve the target model performance?  
        - No
    - What steps did you take in your attempts to increase model performance?  
        - I implemented a function to optimize the model with hyperparameter options using `kerastuner` to pick the most efficient activation, number of neurons, and number of layers 

## Summary   
For this challenge, I had to develop a deep learning neural network model for Alphabet Soup to select the applicants for funding with the best chance of success in their ventures. I started by preprocessing the data which involved dropping identification columns, binning some columns, dummifying categorical columns, and scaling the training and testing features datasets.

Then with the help of a hyperparameters tuner, I computed the accuracy and loss for the best model, after which I compiled, trained, and evaluated my model which gave me a loss of 60% and an accuracy of 73%.

After this, I tried to optimize my model by fine-tuning the activation functions, number of layers, and number of neurons. There were three attempts made which gave the following results.  
<img src="./images/analysis.png" alt="comparision" width="300"/>  

A different model that can potentially be used is a Functional API, which is an easy-to-use, keras industry strength model. The functional API is a way to build layers to create a model that is more flexible than the Sequential model, so you can specify its inputs and outputs in layers.
So we can fine-tune the hyperparameters to get the highest accuracy.
We can additionally include built-in layers for example  
- Convolutional layers  
- Pooling layers  
- RNN layers, etc.  

We can also try an ensemble approach that combines machine-learning models like random forests and decision trees.
