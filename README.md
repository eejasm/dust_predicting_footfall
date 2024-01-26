# dust_predicting_footfall

This repository contains notebooks which lay out the steps for using an LSTM model to predict footfall in Melbourne.

To create the datasets that are used in these notebooks, see [masher92/footfall](https://github.com/masher92/footfall) repository for detailed instructions.

Information on notebooks:

## sensor_rnn_model
This notebook goes throught the steps for producing a model that predicts footfall for the next hourly timestep. Data can only be extracted from one sensor, which must have full data without missing gaps. Therefore, any model produced from this notebook is a prediction tool for the sensor it was trained on. There is a routine in the below code which check the available sensors that have no missing gaps.

## sensor_rnn_model_sliding_window
This notebook contains the same code as sensor_rnn_model. The difference comes at the end where multiple different training runs are performed to test how changing the window size affects the skill of the model's footfall predictions.

## rnn_whole_city
This notebook runs the same architecture as sensor_rnn_model and sensor_rnn_sliding_window except applied to a different dataset. In thes dataset used here, all the footfalls are accumulated at each timestep. This is in order to try and predict the footfall for the entire city at one time.
