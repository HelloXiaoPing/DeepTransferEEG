# T-TIME: Test-Time Information Maximization Ensemble for Plug-and-Play BCIs

Welcome! This is the official implementation of our paper named "T-TIME: Test-Time Information Maximization Ensemble for Plug-and-Play BCIs".

## Steps for reproduction of results in paper:

#### 1. Install Dependencies

Install Conda dependencies based on  `environment.yml` file.

#### 2. Download Datasets

Download datasets used for experiments running ```python ./utils/data_utils.py```

#### (Optional) 3. Training Source Subject Models

Run ```sh train.sh``` or ```python ./tl/dnn.py``` to train the source models.  
Note that such source models serve as EEGNet baselines, and are also used in SFUDA and TTA approaches as the initializations.  
So to save time for TTA/SFUDA for target subject adaptation, it is better to do this step first.  

#### 4. Conduct Transfer Learning on Target Subject

Run ```sh test.sh``` or ```python ./tl/ttime.py``` to test the T-TIME algorithm.  
Run any of ```python ./tl/*.py``` for its corresponding results.  
As an example, T-TIME results can be reproduced using ```python ./tl/ttime.py```  
Note that ensemble is seperated in ```python ./tl/ttime-ensemble.py``` for the purpose of clarity.  
For CSP approach, it is not a deep learning approach and is seperated from the others. Run ```python ./feature.py``` for results.

## Hyperparameters

Most hyperparameters/configurations of approaches/experiments are under the *args* variable in the "main" function of each file, and naming should be self-explanatory.

## Contact

Please contact me at syoungli@hust.edu.cn or lsyyoungll@gmail.com for any questions.