# Toxic_Comments_Classification

[![forthebadge](https://forthebadge.com/images/badges/no-ragrets.svg)](https://forthebadge.com)

In this project we analyzed toxic comment dataset from a Kaggle challenge - https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge/overview. 

Our goal was to implement model that’s capable of detecting different types of of toxicity (like threats, obscenity, insults, and identity-based) in comments.

*Disclaimer: the dataset contains text that may be considered profane, vulgar, or highly offensive.*

## Classification 
We perform EDA and modelling of BiGRU in [this notebook](https://github.com/blawok/Toxic_Comments_Classification/blob/master/toxic_comments.ipynb). 

#### Final model consisted of:
* 100d GloVe embeddings (followed by dropout for training)
* 1d Convolution and 1d MaxPooling layer (played a role of an encoder)
* Bidirectional GRU with 128 hidden units and GlobalMaxPooling layer (followed by dropout for training) - aka decoder
* Finally Dense layer and an output layer

You can reproduce it on your own following the steps from [the notebook](https://github.com/blawok/Toxic_Comments_Classification/blob/master/toxic_comments.ipynb).

#### Embeddings
We experimented with training our own embeddings, but GloVe without any fine-tuning turn out to have better results.

Screenshot from [Embedding Projector](https://projector.tensorflow.org/) for our own embeddings:

<p align="center">
  <img width="460" height="300" src="https://user-images.githubusercontent.com/41793223/81406096-3f563880-9139-11ea-9401-3b32f2a4f27d.JPG">
</p>


## BERT experiment
We came across a great [example](https://github.com/romanorac/romanorac.github.io/blob/master/assets/notebooks/2019-12-02-identifying-hate-speech-with-bert-and-cnn-comments.ipynb) of using BERT for this problem implemented by [Roman Orac](https://github.com/romanorac). Adjusted code for our needs can be found [here](https://github.com/blawok/Toxic_Comments_Classification/blob/master/toxic_cnn_bert.ipynb).
