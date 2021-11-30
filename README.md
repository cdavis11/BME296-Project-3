# BME296-Project-3

The file sp1s_aa.mat contains 416 epochs of data. 
Each epoch is 500ms in length.
316 of the epochs are labeld with a 0 or a 1. A 0 indicates an upcoming left hand movement and a 1 indicates an upcoming right hand movement. 
100 epochs are unlabled and will be disreguarded. 
The sampling frequency used for the dataset was 100Hz. 

Variables: 

clab: Contains the labels of the electrodes. 
x_train: Contains the training trial epoch data (time x channels x trials).
y_train: Contains the labels for upcoming hand movement (0 = left, 1 = right).
x_test: Contains the test trial epoch data (time x channels x trials).
