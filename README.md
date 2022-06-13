# CS575_Team4
CS575 Final Project, Investigating Gender Bias in Pretrained Korean Word Embeddings

** This project is based on the 'A Causal Inference Method for Reducing Gender Bias in Word Embedding Relations(https://arxiv.org/pdf/1911.10787.pdf)' paper and 'KLUE: Korean Language Understanding Evaluation(https://arxiv.org/pdf/2105.09680.pdf)' paper **

## 1. Overview of project
The gender debiasing methods that used in our projects are based on the Yang and Feng(2019).

We tried to measure gender bias in pretrained Korean word embeddings and checked whether Half Sibling Regression(HSR) methods works well on Korean dataset.

We made 3 Korean word lists for our project, and proved that our dataset was powerful to measure gender bias in Korean word embeddings compared Klue-Bert vocabulary set.

You can follow our experiments by using the codes in 'Usage' section.

## 2. Datasets
Ours

    Gender-definition word set -> male.txt, female.txt
    Non-gender-definition word set -> gender_neutral.txt
    Profession word set -> professions.txt

Download(https://huggingface.co/klue/bert-base/blob/main/vocab.txt)

    Klue-Bert vocabulary set -> vocab.txt

## 3. Installation
Install transformers
    
    $pip install transformers
    
Install mpld3
    
    $pip install mpld3

To run the codes, you need a google account to use collaboratory.

Change the path of "$os.chdir('project_path')" by your running path for each .ipynb file.

## 4. Structure of this repository

./word list : consist of word lists (gender_neutral.txt, female.txt, male.txt, professions.txt, vocab.txt)

Extract_KLUE_emb.ipynb : make embeddings and save them into dictionary form (only change the file path to make different embeddings)

HSR.ipynb : make embeddings after applying HSR gender debiasing method 

main.ipynb : load json and run gender-relation tasks

## 5. Usage
###    a) Data Preparation

Use this file to make json files that consists of dictionary {'낱말': List of embedding vectors}. Embeddings are made by pretrained KLUE-BERT-base model.

    Extract_KLUE_emb.ipynb
    
The result files will be saved at './word list/female.json', './word list/male.json', './word list/gender_neutral.json', and './word list/professions.json'

###    b) Apply HSR debiasing method

Use this file to make json files that consists of dictionary {'낱말': List of embedding vectors}.

    HSR.ipynb

The result files will be './word list/hsr_klue_bert_vectors_normalize.txt', and './word list/hsr_whole_normalize_vectors.txt'

###    c) Measuring Gender-bias with gender-relation tasks

Use this file to measure Bias-by-projection and gender bias in word embedding relation (Gonen and Goldberg, 2019)

    main.ipynb
