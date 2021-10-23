# Neural_Network_Charity_Analysis by Kieran Persaud

## Analysis Overview
From Alphabet Soup’s business team, Beks received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization. For this Challenge, using my knowledge of machine learning and neural networks, I identify features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. This requires three parts;
- preprocessing the csv data to be run in the neural network model
- compile, train and evaluate the model for its accuracy
- make three attempts to optimize the model by adjusting the preprocessing or by changing various parameters of the model.

## Resources
- Data Source: charity_data.csv
- Software: Anaconda 4.10.1, kernel mlenv; Jupyter Notebook

## Results

### Data Preprocessing
- The column ```IS_SUCCESSFUL``` is the target of the deep learning neural network.
- The columns ```APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT``` are the features of the model.
- The columns ```EIN``` and ```NAME``` are identification information and have been removed from the input data.

### Compiling, Training, and Evaluating the Model
- For this deep-learning neural network model is made of two hidden layers with 80 and 30 neurons respectively. For each hidden layer, I used a "relu" activation function, and a "sigmoid" function for the output layer.

![image](https://user-images.githubusercontent.com/84286467/138540179-b125ed70-6bbe-43cf-ada0-bb6a5e55d407.png)

- The model was unable to reach 75% accuracy. As the screenshot below depicts, it was only able to reach 69.77% accuracy.

![image](https://user-images.githubusercontent.com/84286467/138540231-a0e172f1-7b0c-4fe8-b27e-f069feb5513d.png)

- Additional Attempts

**Attempt 1**

In this attempt, in addition to dropping the columns ```EIN``` and ```NAME```, I dropped ```STATUS``` and ```SPECIAL_CONSIDERATIONS``` during preprocessing. I also changed the classification buckets to <500. This created a smaller Other category.

After running this model, this did not reach the 75% accuracy threshold. It achieved only 68.81%. These changes did not result in any major increase.

![image](https://user-images.githubusercontent.com/84286467/138540349-7e472ca0-0e41-4a81-9550-fdd24d250d44.png)

**Attempt 2**

In this attempt, I kept all the changes made in attempt 1, and added more neurons to the hidden layers and 1 additional hidden layer.

![image](https://user-images.githubusercontent.com/84286467/138540464-c37eb416-bf57-453a-873a-11ce6f85b147.png)

After running the model, the accuracy decreased to 54.68%.

![image](https://user-images.githubusercontent.com/84286467/138540488-3c55c9e0-8a01-4a3b-9860-d2ba3ffe5aaa.png)

**Attempt 3**

In this attempt, I kept all the changes made in attempts 1 and 2, and changed the activation function for 1 hidden layer from relu to tanh.

![image](https://user-images.githubusercontent.com/84286467/138540528-999c5fe4-b479-4c12-9164-56d5b8bc604e.png)

After running the model, the accuracy increased to 57.68%.

![image](https://user-images.githubusercontent.com/84286467/138540538-86e62bcd-8f70-4c55-a2d6-c23f76cb7782.png)

