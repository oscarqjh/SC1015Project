# SC1015 Mini-project AY2023

## League of Legends Data Analysis
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white) ![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black) ![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white) ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white) ![Plotly](https://img.shields.io/badge/Plotly-%233F4F75.svg?style=for-the-badge&logo=plotly&logoColor=white) ![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white) ![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white) ![SciPy](https://img.shields.io/badge/SciPy-%230C55A5.svg?style=for-the-badge&logo=scipy&logoColor=%white)








### Team members:
- Oscar
- Dimas
- Mokshitt

---
### Section 1: Dataset and Misc.
#### 1.1 Dataset
All Dataset found in this repository is taken from [Kaggle](https://www.kaggle.com/datasets/chuckephron/leagueoflegends?select=LeagueofLegends.csv). There are many datasets, but we will be mainly using:  
```
├── datasets   
|   ├── LeagueofLegends.csv   
|   ├── Kills.csv   
```
#### 1.2 Suggested Read Order
We seperated our jupyter notebook into different segments for easier reading, we suggest reading in the following order:
1. EDA.ipynb
2. LogisticRegression.ipynb
3. RNN.ipynb

#### 1.2 Dependancies
- Matplotlib 3.7
- Pandas 2.0 
- Seaborn 0.12
- Numpy 1.24
- SciPy 1.10.1
- Scikit-learn 1.2.2
- PyTorch 2.0

#### 1.3 Environment Set up
Since we will be using PyTorch's RNN Model, installation of the API is required for `RNN.ipynb`
> Instructions taken from https://pytorch.org/get-started/locally/

#### Without Anaconda (skip this if using Anaconda)
Create a Conda environment:
```
conda create -n env_pytorch python=3.7
```
Activate Conda environment:
```
conda activate env_pytorch
```
#### With Anaconda (important)
Install PyTorch using pip:
```
pip install torchvision
```

---
### Section 2: Introduction   
#### 2.1 About League of Legends   
League of Legends (LoL) is a multiplayer online battle arena (MOBA) game developed and published by Riot Games in 2009, with over 153 million monthly active players. 

#### 2.2 Project Objectives

---
### Section 3: Machine Learning Models
In this project, we experimented with a few machine-learning models:   

#### 3.1 Logistic Regression    
Logistic Regression is a statistical model often used for classification. It estimates the probability of an event (dependent variable) based on a given dataset of independent variables[1].   

For this project, will be using it to predict the outcome of a game (win/lose) based on "x kills obtained before y minutes". For the model based on "x kills obtained before 5 minutes" we are able to obtain a model with ~64% accuracy

#### 3.2 Multi Variated Decision Tree   
A decision tree is a non-parametric supervised learning algorithm utilised for classification and regression tasks. Multi Variated Decision Tree models is a type of classfication model that are based on multiple variables[2]

#### 3.3 Random Forest    
Random Forest is a commonly used machine learning algorithm which combines the output of multiple decision trees to reach a single result[3].

#### 3.4 Recurrent Neural Network   
RNN is a class of artificial neural networks which uses sequential data. A characteristic feature of RNN is that they are about to take a hidden output from previous iteration as inputs for the next iteration[4]. 

For this project, we used sequential data of "difference between events occurred at every minute from 0 to x minutes" for different variables which we identified to be important such as Baron kills, Dragon kills, Tower takedowns, Gold difference and Champion kills to predict the outcome of the game. With the PyTorch's RNN model[5] we are able to obtain an accuracy of ~84%, the best so far within our project.

---
### Section 4: Conclusion   
#### 4.1 Possible Strategies Derived   

#### 4.2 Prediction of Match Outcome   


<h3 align="center">Reference</h3>

[1]: [*What is Logistic Regression*. IBM, 2023](https://www.ibm.com/topics/logistic-regression#:~:text=Resources-,What%20is%20logistic%20regression%3F,given%20dataset%20of%20independent%20variables.)    
[2]: [*What is Decision Tree*. IBM, 2023](https://www.ibm.com/topics/decision-trees)   
[3]: [*What is Random Forest*. IBM, 2023](https://www.ibm.com/topics/random-forest#:~:text=Random%20forest%20is%20a%20commonly,both%20classification%20and%20regression%20problems.)      
[4]: [*What is RNN*. IBM, 2023](https://www.ibm.com/topics/recurrent-neural-networks)    
[5]: [PyTorch's RNN model](https://blog.floydhub.com/a-beginners-guide-on-recurrent-neural-networks-with-pytorch/)    


