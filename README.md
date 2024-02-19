# Anomaly Detection LSTM-Autoencoder

This project aims to show how an LSTM autoencoder can be built to detect anomalies in time series.

### 1. The dataset
The dataset contains readings from multiple sensors which measure different aspects of a water treatment plant. Measurements are tajen every second. Sensor LIT101 has been chosen for this anomaly detector.

The train set contains no anomalies while the test set shows both anomalous and normal behavior.

### 2. The model
An LSTM autoencoder is an architecture of a recurrent neural network, which performs very well for these type of tasks.

For each datapoint, the model will use 100 timesteps to predict the next datapoints using the information it has learnt from the train set. If the reconstruction error between the what the neural network has predicted and the ground truth is above a certain threshold, the point will be marked as an anomaly.

### 3. The notebooks
This project contains three notebooks:
1. ```sensor-anomalies.data_exp.ipynb```
2. ```sensor-anomalies.etl-feature-eng.ipynb```
3. ```sensor-anomalies.model.ipynb```

Each notebook contains the appropriate steps of building the model. Note that some notebooks contain multiple functionality to reduce the problem of having an unnecessarily large number of short notebooks.