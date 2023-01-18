# Neural_Network_Charity_Analysis 

# Overview of the analysis:
The goal of this project is to use neural networks to create a binary classifier capable of predicting whether candidates will be successful if funded by Alphabet Soup.
For this, we will use a dataset of 34,000 organizations that have received funding from Alphabet Soup over the years.

# Results:
### Data Preprocessing
- We consider the IS_SUCCESSFUL variable as the target variable for this model, as it is the variable that indicates whether the money was used effectively.
- As features, we use all numerical variables that could be significant for the model. They are: AFFILIATION,
CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, ASK_AMT.
- The EIN and NAME variables were removed because they are just identification columns. In the optimization model, the SPECIAL_CONSIDERATIONS variable was removed because we believe it does not have much weight in the model and we are trying to improve accuracy.

### Compiling, Training, and Evaluating the Model
- In the AlphabetSoupCharity file, we use the number of layers and neurons below based on the premise that the number of neurons should be 2 to 3 times the number of columns.
#paste layer 1
- In the optimization file, we changed the number of neurons and increased the number of layers, following the same premise of the previous item.
# paste layer2

- Even with several tests, we were unable to achieve the performance of the target model.

- To try to increase the model's performance, we excluded the SPECIAL_CONSIDERATIONS variable because we believed that it would not be adding much performance, which was confirmed when running the target model only with its exclusion. We also changed several times the number of neurons in the hidden layers, included hidden layers and tried the most diverse combinations in the activation modes.


# Summary:
After several attempts to improve the model's performance, as we can see in the two images below, both the target model and the optimized model presented a very low accuracy both for the training data, 0.7392 and 0.7380 respectively, and for the test data, 0.7301 and 0.7293. The loss data also corroborate that the target and optimized models are not considered good. For the training data we had a loss of 0.5350 and 0.5405, and for the test data the loss was 0.5552 and 0.5605.
In this way, we suggest the use of a supervised learning model, since we can use a target variable. And to define which of the models within supervised learning, we suggest performing an analysis on the percentage of options for the target variable to verify which model would be the most suitable.
The target model is encoded in the AlphabetSoupCharity.ipynb file and the optimized model in the AlphabetSoupCharity_Optimization.ipynb file.