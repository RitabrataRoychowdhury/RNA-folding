# 2023-Stanford-Ribonanza-RNA-Folding
This repository <b>is an unsubmitted Solution</b> of [the Stanford Ribonanza RNA Folding competition 2023](https://www.kaggle.com/competitions/stanford-ribonanza-rna-folding/overview). Training was conducted on one GeForce RTX 3080 GPU. The result of the 10-fold + 1 model in 100-fold ensemble models was as follows.  

# Summary
![Model structure](documents/Overall.jpeg)
* <b>Model:</b> Transformer + 1D Conv Residual BPP attention + GRU + LSTM


# File Description
```
├── exp
│   └── trainer.py
├── main
│   ├── bottle.py
│   ├── data.py
│   ├── modules.py
│   └── utils.py
└──  eda.ipynb
```
  
  
# How to use?
### 1. Clone this repository  
```
git clone 
cd into the directory where u saved
```
### 2. Download the dataset
### 3. Docker Image
```
i will provid later
```
### 4. Pseudo label pretraining
Set the <b>pretraining = False</b> in the trainer.py and 
```
cd exp
python trainer.py
```
### 5. Finetuning
Set the <b>pretraining = True</b> in the trainer.py and   
Set the load_ckpt path to you're pretrained checkpoint path.
```
cd exp
python trainer.py
```
# Inference
Set the value of the only_pred parameter to integer (n) to use nth directory's checkpoints in the log_dir.


