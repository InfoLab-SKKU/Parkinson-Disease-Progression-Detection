# Depression Prognosis and Parkinson’s Disease Progression Detection Using Multitask Deep Learning Model and Multimodal Time Series Data
This repository contains the code and analysis findings used for depression prediction and Parkinson's disease progression detection with multitask deep learning.



### The architecture of the proposed framework 
<img src="assets/Figures/figure1.png">  

Detail of the proposed framework for the multitask classification. First, collect the dataset with multi-modalities. Second, a number of preprocessing
steps are performed for the model stability such as normalization, and class imbalanced technique. Third, we used a variational autoencoder (VAE) for feature
extraction. Fourth, a 3D CNN extracts the MRI deep features and used them with the fusion of VAE obtained features. 5-fold cross-validation and testing are
used for evaluation. The model is trained on the selected features and fused features. In the end, the results are evaluated on the testing set after hyperparameter
optimization for single and multi-tasks. Mods 1,2,3 are the approaches of experiments, explain in detail in the Results and Discussion section.

#### PPMI Dataset 
This research is conducted using the PPMI database [Database link](http://www.ppmi-info.org/data). The database is a multi-national, large-scale database that records the progression of PD. The database is comprehensive in its coverage of patient,clinical information

#### Results analysis

Our study is divided into two groups: single-task and multitask experiments. We conducted three single-task experiments in which our proposed model trained on a specific classification task (e.g., prediction of NHY stage or depression level or whether the patient is depressed or not). We designed the model for multitasking studies to predict two or three classification tasks simultaneously. Our proposed model is evaluated in this section using performance matrices such as accuracy, precision, recall, and F1-score.

<img src="assets/Figures/figure2.png">  

The performance evaluation on the prediction of the severity of PD patients based on NHY scale with or without depression and the level of depression across different time steps for single-task and multitasking ( three tasks) experiment. (a) A four-class NHY scale that defines the stage of PD. (b) A binary class that determines whether or not a patient is depressed. (c) A four-class depression scale that indicates the severity of depression. The performance matrices compare to the testing dataset. The bar on the top of each column represents the standard error.
