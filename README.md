# PROJECT - DIFFERENTIAL PRIVACY FOR DEEP LEARNING ON THE MNIST DIGIT DATASET

## ABSTRACT

Differential privacy is a system for publicly sharing information about a dataset by describing the patterns of groups within the dataset while withholding information about individuals in the dataset. Another way to describe differential privacy is as a constraint on the algorithms used to publish aggregate information about a statistical database which limits the disclosure of private information of records whose information is in the database. For example, differentially private algorithms are used by some government agencies to publish demographic information or other statistical aggregates while ensuring confidentiality of survey responses, and by companies to collect information about user behavior while controlling what is visible even to internal analysts.

Roughly, an algorithm is differentially private if an observer seeing its output cannot tell if a particular individual's information was used in the computation. Differential privacy is often discussed in the context of identifying individuals whose information may be in a database. Although it does not directly refer to identification and reidentification attacks, differentially private algorithms probably resist such attacks.



---



## Visualization of Differential Privacy



<img src="https://github.com/ateniolatobi/Differential-privacy-for-deeplearning-project/blob/master/assets/dp.png" width="100%">



## PROJECT DESCRIPTION

Differential privacy in Deep learning is the process where the concept of Differential Privacy is applied in Deep Learning models. The application of differential privacy in deep learning ensures that Deep learning models are created which are accurate and at the same time conserves user privacy.  

Differential privacy preserves privacy by introducing distortion or randomness into the data in a dataset(Local differential privacy) or in the output of a query (Global Differential privacy) in order to ensure that the dataset or the output of a query on the dataset are distorted enough to ensure that the output of a query varies slightly from the actual output hence protecting privacy and at the same time being accurate enough to represent the general trend in the dataset for any statistical analysis on the dataset.  

Global Differential privacy in Deep learning involves the use of teacher models trained on unique datasets to evaluate an unlabelled dataset which would be used to train the differentially private model.  


- In this project, Global differential privacy would be used. Global Differential privacy in Deep learning involves the use of teacher models trained on unique datasets to evaluate an unlabelled dataset which would be used to train the differentially private model.
- The labels generated by the teacher models would be evaluated through a mechanism known as PATE analysis which returns a result that indicates the trade-off between privacy and accuracy by the teacher models. The number of teacher models and the training epoch of the teacher models would be varied until a reasonable result is gotten after performing PATE analysis.
- The various labels generated for each data in the unlabelled dataset by the teacher models would then be randomized slightly by applying Laplacian noise ensuring that few data entries in the dataset would be purposely mislabeled to conserve privacy. 
- The now labeled dataset would be used to create and train a model that would be differentially private. 

---



## Tools Used

> The model was created and trained with PyTorch and the MNIST digit dataset was used to train the models.


- torch==1.1.0
- torchsummary==1.5.1
- torchtext==0.3.1
- torchvision==0.3.0
- syft==0.1.29a1
- numpy==1.16.4
- matplotlib==3.0.3




```

pip install torch

pip install syft

pip install pandas

pip install numpy 

pip install matplotlib

```



## References

1. [Understanding Differential Privacy](https://towardsdatascience.com/understanding-differential-privacy-85ce191e198a)

2. [Secure and Private AI course Udacity](https://www.udacity.com/course/secure-and-private-ai--ud185)

3. [Martín Abadi, Andy Chu, Ian Goodfellow, H. Brendan McMahan, Ilya Mironov, Kunal Talwar, Li Zhang. (2012). Deep Learning with Differential Privacy](https://arxiv.org/abs/1607.00133)

