# Paraphrase-Classificationz

Used Siamese network for parphrase classification.

Siamese neural network is a class of neural network architectures that contain two or
more identical subnetworks. identical here means they have the same configuration with
the same parameters and weights. Parameter updating is mirrored across both subnetworks.Sharing weights across subnetworks means fewer parameters to train for,
which in turn means less data required and less tendency to overfit.

Used 100 dimension pre-trained GloVe word-vector provided by Stanford.As main
building block of NN  used Bidirectional RNN with LSTM as memory unit since
sequence length is 50 there might be possibility of longer dependencies.

Used RMSprop as optimiser and default parameters as mention in keras
documentation.RMSprop is good choice for training RNN.( source ) I have used callbacks
in case of problem in power supply etc. Strategy for callback is validation accuracy
improvement.
