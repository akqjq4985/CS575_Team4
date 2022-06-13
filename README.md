# CS575_Team4
CS575 Final Project, Investigating Gender Bias in Pretrained Korean Word Embeddings

** This project is based on the 'A Causal Inference Method for Reducing Gender Bias in Word Embedding Relations(https://arxiv.org/pdf/1911.10787.pdf)' paper and 'KLUE: Korean Language Understanding Evaluation(https://arxiv.org/pdf/2105.09680.pdf)' paper **

## 1. Overview of project
The gender debiasing methods that used in our projects are based on the Yang and Feng(2019).

We tried to measure gender bias in pretrained Korean word embeddings and checked whether HSR methods works well on Korean dataset.

We made 3 Korean word lists for our project, and proved that our dataset was powerful to measure gender bias in Korean word embeddings compared Klue-Bert vocabulary set.

You can follow our experiments by using the codes in 'Usage' section.

## 2. Datasets
Ours

    Gender-definition word set
    Non-gender-definition word set
    Profession word set

Download

    Klue-Bert vocabulary set

## 3. Installation
Install transformers
    
    $pip install transformers
    
Install mpld3
    
    $pip install mpld3

To run the codes, you need a google account to use collaboratory.

## 4. Structure of this repository
preprocess.ipynb : make embeddings
remaining_bias.ipynb : make 
main.ipynb : load json and run gender-relation task

## 5. Usage
###    a) Data Preparation

Download the dataset from the folder ./data
