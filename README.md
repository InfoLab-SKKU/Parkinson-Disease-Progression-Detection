In this work, we proposed a deep learning model capable of identifiing Parkinson's disease progression and the prognostic prediction of depression utilizing multimodal time series data.
-------------
This repository contains the code and analysis findings used for depression prediction and Parkinson's disease progression detection with multitask deep learning.



### The design of the suggested framework's structure.

<div align="center">
  
![Alt text](Figures/figure2.png "framework")  
  
</div>

<p align="justify">
The proposed framework for multitask classification encompasses multiple stages. The initial step involves compiling a dataset incorporating information from various sources. Subsequently, to ensure the model's reliability, numerous preprocessing techniques, such as normalization and class imbalance correction, are employed. In the third step, a Variational Autoencoder (VAE) is implemented for feature extraction. In the fourth stage, a 3D Convolutional Neural Network (CNN) extracts deep features from MRI data, which are then combined with the VAE-generated data. The evaluation process involves employing five-fold cross-validation and testing. The selected features, along with the fused features, are used to train the model. After optimizing the hyperparameters, the model is assessed on a validation dataset to determine its performance.
</p>

Improvements 1, 2, and 3 are three distinct experimental methodologies used to optimize single and multi-task performance. The methods used to achieve these outcomes are elaborated upon in the next section: Results and Discussion.




### PPMI Dataset 
<p align="justify">
This research makes use of the PPMI database, which may be viewed at Database link. This database tracks the development of Parkinson's disease throughout the world and includes rich patient and clinical details.
</p>

#### Results analysis
<p align="justify">
The research is broken down into two groups: single-task experiments and multitask experiments. Single-task tests focused on training our proposed model to predict a single classification task, such as NHY stage, depression degree, or the existence of depression in a patient. In order to anticipate two or three separate classification tasks at once, we built the model for the multitask tests with that in mind. In this part, we use measures like as accuracy, precision, recall, and F1-score to assess the efficacy of our suggested model.
</p>
<div align="center">
  
![Alt text](Figures/figure1.png "Results")  

</div>
<p align="justify">
This research evaluates the efficacy of the suggested model in predicting Parkinson's disease (PD) severity in patients using the NHY scale, both with and without depression, and at varying time steps in single-task and multitask (three-task) tests. The evaluation uses (a) a four-class NHY scale to determine the stage of PD, (b) a binary class to determine the presence or absence of depression, and (c) a four-class depression scale to determine the degree of depression severity. The standard error is depicted by the bar at the top of each column, and the performance metrics are compared to the testing dataset.
</p>

### Guideline for reproducing results 

# Upon obtaining the dataset, it is preprocessed according to the problem statement.

Run 
```bash
01_Depression_BiLSTM.ipynb 
```
To find out Best model parameters 
Run
```bash
02_KerasT_Bilstm.ipynb    
```
# Directory
<pre>

├─model
│  ├─01_Depression_BiLSTM.ipynb
│  │─02_KerasT_Bilstm.ipynb      
│  └─03_Keras tuner.ipynb 
│          
│─Figures
│    └─Figure1.png
│    ├─Figure2.png
│   
└─requirements.txt
</pre>
