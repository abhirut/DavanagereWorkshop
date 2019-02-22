# DavanagereWorkshop
Workshop on Deep Learning and its applications. Speakers - Saneem Chemmengath, Sneha Mondal, and Abhirut Gupta.

## Contact Information
- Saneem Chemmengath (saneem.cg@in.ibm.com)
- Sneha Mondal (snmondal@in.ibm.com)
- Abhirut Gupta (abhirutgupta@in.ibm.com)

## Pre-requisites
1. Please download the following datasets -
  - Housing Prices https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data
  
  You will need to create a Kaggle account, and accept the terms of the competition. (Follow the instructions from the `Download All` button.
  - MNIST http://yann.lecun.com/exdb/mnist/
  Download all 4 files

2. You will need Python for the workshop, we suggest installing Anaconda for Python 3.7
Installer links for different OS can be found at -
```
Mac - https://repo.anaconda.com/archive/Anaconda3-2018.12-MacOSX-x86_64.pkg
Windows - https://repo.anaconda.com/archive/Anaconda3-2018.12-Windows-x86_64.exe
Linux - https://repo.anaconda.com/archive/Anaconda3-2018.12-Linux-x86_64.sh and power machines - https://repo.anaconda.com/archive/Anaconda3-2018.12-Linux-ppc64le.sh
```

Anaconda installation guide is at - https://docs.anaconda.com/anaconda/install/

3. After installing anaconda, you can install the following packages
  - nltk	https://anaconda.org/anaconda/nltk
  - gensim	https://anaconda.org/anaconda/gensim
  - keras	https://anaconda.org/anaconda/keras
  - tensorflow	https://anaconda.org/anaconda/tensorflow
  - pytorch		https://anaconda.org/pytorch/pytorch
  - torchtext	https://anaconda.org/derickl/torchtext

The link for each package (https://anaconda.org/anaconda/nltk) contains instructions on how to install it. 

For example for windows machines open `Anaconda prompt` from windows search menu and type the following command and press `Y` when asked to install. 

![alt text](https://docs.anaconda.com/_images/anaconda-prompt.png | width=25)

For Mac and Linux type these commands in bash. -
```
conda install -c anaconda nltk
```

4. Download the spacy English model - comnands
```
python -m spacy download en
```

and stopwords from nltk -

```
python -m nltk.downloader stopwords
```

Also download the IMDB sentiment dataset, and pre-trained Glove word embeddings on torchtext with the following python code -
```
import torch
from torchtext import data
from torchtext import datasets

TEXT = data.Field(tokenize='spacy')
LABEL = data.LabelField(dtype=torch.float)

train_data, test_data = datasets.IMDB.splits(TEXT, LABEL)
TEXT.build_vocab(train_data, max_size=25000, vectors="glove.6B.100d")
LABEL.build_vocab(train_data)
```
This is 84 MB and 862 MB respectively.

Also download the file - https://github.com/abhirut/DavanagereWorkshop/blob/master/kc_house_data.csv

5. Download the three `.ipynb` files in this repo
  - https://github.com/abhirut/DavanagereWorkshop/blob/master/IntroDL.ipynb
  - https://github.com/abhirut/DavanagereWorkshop/blob/master/Image_classification_MNIST.ipynb
  - https://github.com/abhirut/DavanagereWorkshop/blob/master/DL_NLP.ipynb
  
