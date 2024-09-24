
## Project: Time Series Forecasting using Facebook's Prophet Model

### Introduction:
Time series forecasting is a critical task in various domains such as finance, energy consumption, and weather prediction. In this project, we explore the application of Recurrent Neural Networks (RNN) and Long Short-Term Memory (LSTM) networks for time series forecasting. Specifically, we aim to predict energy consumption using hourly data.

### Dataset:
The dataset used in this project is the PJME hourly energy consumption dataset, which provides hourly energy usage in megawatts (MW). The dataset spans multiple years and contains information about energy consumption patterns over time.

### Data Preprocessing:
Before training the models, we performed several preprocessing steps:

1. Outlier Analysis and Removal: Identified and removed outliers from the dataset to improve model performance.
Scaling Target: Normalized the target variable (energy consumption) using MinMaxScaler to scale it between 0 and 1.
2. Train/Test Split: Split the dataset into training and testing sets to evaluate model performance.

### Model Building:
I built two types of models for comparison: RNN and LSTM.

`RNN Model`: The RNN model consists of three SimpleRNN layers with dropout regularization to prevent overfitting.
`LSTM Model`: The LSTM model comprises three LSTM layers with dropout regularization to capture long-term dependencies in the data.

### Training and Evaluation:
Both models were trained using the training data and evaluated using the testing data. I used Mean Squared Error (MSE) as the loss function and Adam optimizer for model training. The models were trained for 15 epochs with a batch size of 1024.

### Results:

`RNN Model`: Achieved an R2 score of 0.9769 and an RMSE of 0.0226 on the testing data.
`LSTM Model`: Achieved an R2 score of 0.9774 and an RMSE of 0.0224 on the testing data.

### Visualization:
I visualized the actual and predicted energy consumption data using both RNN and LSTM models. Additionally, I compared the predictions of both models with the original data to assess their performance visually.

### Conclusion:
In conclusion, both RNN and LSTM models performed well in predicting energy consumption based on the PJME hourly dataset. However, the LSTM model slightly outperformed the RNN model in terms of accuracy. These models can be further optimized and deployed in real-world applications for energy consumption forecasting, assisting in efficient resource management and decision-making processes.

### Future Work:

Experiment with different architectures and hyperparameters to further improve model performance.
Explore other types of neural networks and machine learning algorithms for comparison.
Deploy the trained models in a production environment for real-time predictions and integrate them into energy management systems.
