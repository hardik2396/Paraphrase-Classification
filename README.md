# Paraphrase-Classification

Used Siamese network for parphrase classification.[paper](http://www.mit.edu/~jonasm/info/MuellerThyagarajan_AAAI16.pdf)


![myimage-alt-tag](https://www.researchgate.net/profile/Gregoire_Lefebvre/publication/260452382/figure/fig2/AS:297249520275457@1447881216257/Figure-2-A-Siamese-Neural-Network.png)

Used 100 dimension pre-trained GloVe word-vector provided by Stanford.As main
building block of NN  used Bidirectional RNN with LSTM as memory unit since
sequence length is 50 there might be possibility of longer dependencies.

Used RMSprop as optimiser and default parameters as mention in keras
documentation.RMSprop is good choice for training RNN.Strategy for callback is validation accuracy
improvement.

As metric for evaluation i use loss and accuracy. I got 0.18, 0.74 as loss and accuracy
respectively on Test-set.


# TO DO

Use of TF-IDF in two ways.
  1. Concatenated output of NN1 and TF-IDF(200 dim) vector and apply 128 dim
  hidden layer and same goes for NN2 and finally apply softmax layer.
  2. There might be possibility of Question having length higher than 50. To deal with
  problem we use TF-IDF to collect most important 50 words than apply model.

Hyperparameter Tuning  


# Requierements 

Keras,
NLTK
