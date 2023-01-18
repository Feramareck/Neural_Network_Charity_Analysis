# Neural_Network_Charity_Analysis 

# Overview of the analysis:
The goal of this project is to use neural networks to create a binary classifier capable of predicting whether candidates will be successful if funded by Alphabet Soup.  
For this, we will use a dataset of 34,000 organizations that have received funding from Alphabet Soup over the years.

# Results:
### Data Preprocessing
To carry out this analysis, we used the charity_data.csv file provided by Alphabet Soup, which presented the data below:  
![data](https://user-images.githubusercontent.com/111664141/213281326-8c5bd331-2f67-4547-9886-613335e490d7.JPG)

- We consider the IS_SUCCESSFUL variable as the target variable for this model, as it is the variable that indicates whether the money was used effectively.
- As features, we use all numerical variables that could be significant for the model. They are: AFFILIATION,
CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, ASK_AMT.
- The EIN and NAME variables were removed because they are just identification columns. In the optimization model, the SPECIAL_CONSIDERATIONS variable was removed because we believe it does not have much weight in the model and we are trying to improve accuracy.

### Compiling, Training, and Evaluating the Model
- In the AlphabetSoupCharity file, we use the number of layers and neurons below based on the premise that the number of neurons should be 2 to 3 times the number of columns.  
![Layer1](https://user-images.githubusercontent.com/111664141/213281473-d6a90553-e9aa-46ae-a700-d0475d50eca7.JPG)

- In the optimization file, we changed the number of neurons and increased the number of layers, following the same premise of the previous item.  
![Layer2](https://user-images.githubusercontent.com/111664141/213281510-e2d80e5c-2492-4708-9d8d-00fee2581cdf.JPG)

- Even with several tests, we were unable to achieve the performance of the target model.

- To try to increase the model's performance, we excluded the SPECIAL_CONSIDERATIONS variable because we believed that it would not be adding much performance, which was confirmed when running the target model only with its exclusion. We also changed several times the number of neurons in the hidden layers, included hidden layers and tried the most diverse combinations in the activation modes.


# Summary:
After several attempts to improve the model's performance, as we can see in the two images below, both the target model and the optimized model presented a very low accuracy both for the training data, 0.7392 and 0.7380 respectively, and for the test data, 0.7301 and 0.7293.  
The loss data also corroborate that the target and optimized models are not considered good. For the training data we had a loss of 0.5350 and 0.5405, and for the test data the loss was 0.5552 and 0.5605.
## Target Model
![accuracytarget](https://user-images.githubusercontent.com/111664141/213283950-1fe3b7fd-202d-4dab-a666-f08b2b721fca.JPG)

## Optimized Model
![accuracy](https://user-images.githubusercontent.com/111664141/213284385-49e2ff98-ffd8-48ca-b49c-13fa27980c30.JPG)

In this way, we suggest the use of a supervised learning model, since we can use a target variable. And to define which of the models within supervised learning, we suggest performing an analysis on the percentage of options for the target variable to verify which model would be the most suitable.  
The target model is encoded in the AlphabetSoupCharity.ipynb file and the optimized model in the AlphabetSoupCharity_Optimization.ipynb file.
