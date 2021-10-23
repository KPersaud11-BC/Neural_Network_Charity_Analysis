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
- The column `IS_SUCCESSFUL` is the target of the deep learning neural network.
- The columns `APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT` are the features of the model.
- The columns `EIN` and `NAME` are identification information and have been removed from the input data.

### Compiling, Training, and Evaluating the Model
- For this deep-learning neural network model is made of two hidden layers with 80 and 30 neurons respectively. For each hidden layer, I used a "relu" activation function, and a "sigmoid" function for the output layer.
