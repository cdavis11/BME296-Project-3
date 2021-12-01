# BME296-Project-3

The dataset can be downloaded from http://bbci.de/competition/ii/index.html with entry of a name and an email. Once this is done, you will be directed to a site to download any of the datasets. For this project, the file sp1s_aa.mat from data set IV was downloaded.

Upon downloading the file, the function loadmat from the python scipy.io module can be used to load the .mat file into a dictionary, using the following code: 

``` python
from scipy.io import loadmat
data = loadmat('sp1s_aa.mat')
```
Field can then be extracted using the following code:
``` python
# extract eeg training data 
x_train = data['x_train']
# extract channel labels
clab = data['clab']
...
```
The fields of the dictionary are as follows:

clab: Contains the labels of the electrodes. There are 28 electrodes which follow the international 10-20 system.

x_train: Contains the training trial epoch data (50 x 28 x 316, where 50 represents the samples in seconds, 28 is the number of electrodes, and 316 is the number of epochs).

y_train: Contains the truth labels for upcoming hand movement (0 = left hand, 1 = right hand). This has a length of 316, one label for each trial. 

x_test: Contains the test trial epoch data (50 x 28 x 100, following the same format as x_train). This is not used in our project as the corresponding truth labels are not provided.

The sampling frequency used for the dataset was 100Hz. 


