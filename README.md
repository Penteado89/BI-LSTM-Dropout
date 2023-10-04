# EP01 - MAC5725 – Linguística Computacional – 2023 - BI-LSTM-Dropout

Este diretório relata uma atividade de classificação de comentários através de LSTMs, a qual está associada a disciplina MAC5725 – Linguística Computacional – USP - 2023, ministrada pelo professor Dr. Marcelo Finger.

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

Author:
Ricardo Cabral Penteado
NUSP: 13813331
#Resultados:
O MELHOR MODELO identificado pode ser visualizado na imagem model_True_0 25.

![model_True_0 25](https://github.com/Penteado89/BI-LSTM-Dropout/assets/80430113/c0868e3a-9b6d-4b88-b40a-a9f6e9d7743d)


Os valores de acurácia, após testar os seis modelos e avaliá-los no conjunto de teste, foram relativamente baixos. No entanto, eles foram comparáveis às referências dos melhores benchmarks para essa prática usando LSTM bidirecional.

É notório que o uso de arquiteturas mais sofisticadas, como X, produz valores significativamente melhores, conforme demonstrado na tabela mencionada anteriormente. É relevante citar o trabalho de [Nome do Autor], que conduziu experimentos em uma tarefa similar e obteve resultados notáveis.

Tendo tudo isso em mente, é evidente que o uso de técnicas mais avançadas e arquiteturas otimizadas poderia melhorar ainda mais a acurácia do modelo.
