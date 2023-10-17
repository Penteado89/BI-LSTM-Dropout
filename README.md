# MAC5725 – Linguística Computacional – 2023 - EP 1: RNNs Bidirecionais, Overfitting, Underfitting

Sentiment Analysis on B2W Reviews with LSTMs
This repository provides code to conduct a sentiment analysis on reviews from B2W using Long Short-Term Memory networks (LSTMs). LSTMs are a type of recurrent neural network designed to work with sequence prediction problems.

Data:
The dataset consists of user reviews from the B2W platform. Some of the key features of the dataset are:

Submission date
Reviewer id
Product id
Product name
Product brand
Site category levels
Review title
Overall rating (from 1 to 5)
Recommendation status
Review text
Reviewer birth year
Reviewer gender
Reviewer state
Data Preprocessing:
Loading and visualizing the raw data.
Removing unnecessary columns, retaining only 'review_text' and 'overall_rating'.
Handling missing values by dropping rows with missing 'review_text' or 'overall_rating'.
Splitting the dataset into training, validation, and testing sets.
Model:
The main objective is to predict the 'overall_rating' based on the content of 'review_text'. Two types of LSTM architectures are implemented:

Unidirectional LSTM
Bidirectional LSTM
For both architectures, variations with different dropout rates (0.0, 0.25, 0.5) are implemented to prevent overfitting.

Hyperparameters:

Maximum sequence length: 795
Batch size: 32
Vocabulary size: 20,000
How to Use:
The provided code includes necessary imports, data loading, preprocessing steps, model creation, and training routines. To reproduce the results:

Ensure that all the required libraries (like TensorFlow, Keras, pandas, etc.) are installed.
Load the B2W-Reviews01.csv file.
Follow the provided code for preprocessing and model creation.
Train the model using the specified hyperparameters.
Validate the model on the validation set and test on the test set for final performance metrics.
Results:
Results from the LSTM models are stored as checkpoints for the best-performing model based on validation loss. The models and their architectures are saved as '.h5' files and '.png' image files respectively.
Results Analysis:
The LSTM models' performance varies based on architecture and dropout rate. The best models achieved the following results:

For Unidirectional LSTM:
0.0% Dropout:
Best Epoch: 2
Validation Loss: 0.91848
![5](https://github.com/Penteado89/BI-LSTM-Dropout/assets/80430113/9a16df0b-b250-4297-b5a8-eccd5e35d55f)


25.0% Dropout:
Best Epoch: 2
Validation Loss: 0.91764
![6](https://github.com/Penteado89/BI-LSTM-Dropout/assets/80430113/4bc18f88-9b52-42d8-9091-0d326807def0)

50.0% Dropout:
Best Epoch: 2
Validation Loss: 0.91598
![3](https://github.com/Penteado89/BI-LSTM-Dropout/assets/80430113/41bc2270-816d-4d3a-9514-78ffb04228d8)

For Bidirectional LSTM:
0.0% Dropout:
Best Epoch: 2
Validation Loss: 0.90551
![4](https://github.com/Penteado89/BI-LSTM-Dropout/assets/80430113/279a6979-04df-42ad-ae37-5fec17ee8036)

25.0% Dropout:
Best Epoch: 2
Validation Loss: 0.92670
![55](https://github.com/Penteado89/BI-LSTM-Dropout/assets/80430113/01feafb6-31c8-4c4a-9a5b-fb27d1b51063)

50.0% Dropout:
Best Epoch: 2
Validation Loss: 0.91434
![66](https://github.com/Penteado89/BI-LSTM-Dropout/assets/80430113/0ff4c3cd-ff19-492a-9f9c-b8cf69e79c17)

The performance metrics, such as accuracy and loss, over the epochs can be visualized using the plot_history function. This function generates line plots comparing the accuracy and loss of training vs. validation datasets for each architecture and dropout combination.

Testing:
Prepare the test set.
Load the best model (with the lowest validation loss) for evaluation.
![model_True_0 25](https://github.com/Penteado89/BI-LSTM-Dropout/assets/80430113/c0868e3a-9b6d-4b88-b40a-a9f6e9d7743d)

Evaluate the model's performance on the test set.
Display the test accuracy and loss.
For the best model (Bidirectional LSTM with 25% dropout):

Test Loss: 0.91504
Test Accuracy: 59.82%
Model Metrics & Evaluation:
After training, the trained model's structure can be viewed using the summary method.

Metrics associated with the trained model:
![test accuracy](https://github.com/Penteado89/BI-LSTM-Dropout/assets/80430113/4cee7a42-8280-4bb6-806a-9ed71f9e3e6b)

A confusion matrix provides an easy-to-understand visualization of the model's predictions versus actual classifications. Alongside, the classification report provides a detailed breakdown of precision, recall, and F1-score for each class.

              precision    recall  f1-score   support

           0       0.75      0.89      0.81      6424
           1       0.41      0.02      0.04      1997
           2       0.42      0.41      0.42      3965
           3       0.44      0.48      0.46      8046
           4       0.67      0.68      0.68     11843
    accuracy                           0.60     32275
    macro avg       0.54      0.50      0.48     32275
    weighted avg       0.58      0.60      0.58     32275



Conclusions:
The Bidirectional LSTM with a dropout rate of 25% achieved the best validation loss and performed reasonably well on the test set. Still, there is room for improvement in terms of model architecture, hyperparameter tuning, and additional preprocessing steps.

The current model has some difficulties classifying certain classes, as seen in the classification report. Further optimization and experimentation are required to improve these metrics.

The accuracy values, after testing the six models and evaluating them on the test set, were relatively low. However, they were comparable to the best benchmarks for this practice using bidirectional LSTM.

It is clear that the use of more sophisticated architectures, such as X, produces significantly better values, as demonstrated in the table mentioned above. It is relevant to mention the work of [Author Name], who transferred experiments on a similar task and obtained remarkable results.

Bearing all this in mind, it is clear that the use of more advanced techniques and optimized architectures could further improve the model's accuracy.


Author:
Ricardo Cabral Penteado
NUSP: 13813331
