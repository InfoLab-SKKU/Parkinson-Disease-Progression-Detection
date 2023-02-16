A multitask deep learning model and multimodal time series data are utilized for detecting the progression of Parkinson's disease and predicting the prognosis of depression.
-------------
This repository contains the code and analysis findings used for depression prediction and Parkinson's disease progression detection with multitask deep learning.



### The design of the suggested framework's structure.

<div align="center">
  
![Alt text](Figures/figure2.png "framework")  
  
</div>

<p align="justify">
The proposed framework for multitask classification involves several steps. Firstly, a dataset with multiple modalities is collected. Secondly, various preprocessing techniques such as normalization and class imbalance correction are applied to ensure model stability. Thirdly, feature extraction is performed using a variational autoencoder (VAE). Fourthly, deep features are extracted from MRI data using a 3D CNN, which are then combined with the VAE-derived features. Evaluation is conducted through 5-fold cross-validation and testing. The model is trained using the selected features and fused features. Finally, the hyperparameters are tuned and the model is evaluated on the testing set to determine its effectiveness.
</p>

The optimization of single and multi-tasks is accomplished through the use of three different experimental approaches, which are referred to as Mods 1, 2, and 3. These approaches are explained in greater detail in the Results and Discussion section.




### PPMI Dataset 
<p align="justify">
The study utilizes the PPMI database, which can be accessed through this link: Database link. This database is a multinational and extensive repository that monitors the progression of Parkinson's disease, and includes comprehensive patient and clinical information.
</p>

#### Results analysis
<p align="justify">
The study is separated into two categories, consisting of single-task and multitask experiments. In the single-task experiments, we trained our proposed model to predict a specific classification task, such as the prediction of NHY stage, depression level, or the determination of depression presence in a patient. For the multitask experiments, we designed the model to predict two or three classification tasks concurrently. The effectiveness of our proposed model is evaluated in this section using performance metrics like accuracy, precision, recall, and F1-score.
</p>
<div align="center">
  
![Alt text](Figures/figure1.png "Results")  

</div>
<p align="justify">
The study assesses the performance of the proposed model in predicting the severity of Parkinson's disease (PD) in patients based on the NHY scale, with and without depression, as well as the level of depression across various time steps in both single-task and multitasking (three tasks) experiments. The evaluation is conducted using (a) a four-class NHY scale that specifies the stage of PD, (b) a binary class that indicates the presence or absence of depression, and (c) a four-class depression scale that indicates the degree of depression severity. The performance metrics are compared to the testing dataset, and the standard error is represented by the bar on top of each column.
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
