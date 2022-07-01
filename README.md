# Thesis_BERT_Model
Code written for my thesis on classifying cartoon captions

This repository contains the following files:
1.	dependencies.ipynb
2.	dataset.ipynb
3.	BERT.ipynb

The dependencies file installs all libraries and dependencies used in this project, opening this file and clicking Cell -> Run all will install everything. The following libraries are used in this research:
•	Pytorch
•	Pandas
•	Transformers
•	Nlpaug
•	Nltk
•	Scikit-learn

The file dataset.ipynb contains all code used in forming the datasets used. In this file important functions are augmentMyData, oversample and undersample. These functions balance the data.

The file BERT.ipynb creates and trains the BERT model, the BERT model is loaded from: https://tfhub.dev/tensorflow/bert_en_uncased_L-12_H-768_A-12/4; And code from: https://github.com/codebasics/deep-learning-keras-tf-tutorial/tree/master/47_BERT_text_classification was used to construct the final model. In this file it is also possible to save and load the weights of pretrained models unfortunately GitHub limits the file size to 25MB thus I cannot provide pretrained models. Training the model using either the unbalanced or undersampled takes the least amount of time, training using SMOTE or the oversampled dataset takes approximately 10 hours.

The repository also contains the premade SMOTE, oversampled, undersampled and unbalanced datasets. Loading these files can be done using get_data(“filename”) in dataset.ipynb or pd.read_csv(“directory+filename”) in both dataset and BERT.ipynb. New dataset can also be saved using pd.to_csv(“directory+filename”). To use this dataset the first column of the file must be removed, to_csv() adds an extra column. 
