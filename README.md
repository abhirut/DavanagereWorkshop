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

The link for each package (https://anaconda.org/anaconda/nltk) contains instructions on how to install it. For example -
```
conda install -c anaconda nltk
```

4. Download the spacy English model -
```
python -m spacy download en
```

and nltk corpora -

```
python -m nltk.downloader all
```

Also install the IMDB sentiment dataset on torchtext with the following python code -
```
import torch
from torchtext import data
from torchtext import datasets

TEXT = data.Field(tokenize='spacy')
LABEL = data.LabelField(dtype=torch.float)

train_data, test_data = datasets.IMDB.splits(TEXT, LABEL)
```
