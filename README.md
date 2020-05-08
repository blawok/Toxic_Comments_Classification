# Toxic_Comments_Classification

In this project we analyzed toxic comment dataset from Kaggle challenge - https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge/overview. Our goal was to implement model that’s capable of detecting different types of of toxicity (like threats, obscenity, insults, and identity-based) in comments.

*Disclaimer: the dataset contains text that may be considered profane, vulgar, or highly offensive.*

We perform EDA and modelling of BiGRU in [this notebook](https://github.com/blawok/Toxic_Comments_Classification/blob/master/toxic_comments.ipynb).

Screenshot from [Embedding Projector](https://projector.tensorflow.org/) for our embeddings:

![murderous](https://user-images.githubusercontent.com/41793223/81406096-3f563880-9139-11ea-9401-3b32f2a4f27d.JPG)


However, recently, I came across a great example of using BERT for this problem. Code for it can be found [here](https://github.com/blawok/Toxic_Comments_Classification/blob/master/toxic_cnn_bert.ipynb)
