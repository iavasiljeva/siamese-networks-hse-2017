# siamese-networks-hse-2017

This is the lab of HSE students on the theme of Siamese networks  
Group:
* Kositsin Alexander
* Vasiljeva Inna
* Viko Maxim
* Pavlova Elena
---

In this project we are using lspvic/tensorboard-notebook Docker image:  
https://pypi.python.org/pypi/jupyter-tensorboard/0.1.3

This docker image contains:
* Tensorboard
* Tensorflow and Keras for Python 3
* Jupyter Notebook 5.0.x
* Conda Python 3.x environment
* pandas, matplotlib, scipy, seaborn, scikit-learn, scikit-image, sympy, cython, patsy, statsmodel, cloudpickle, dill, numba, bokeh, vincent, beautifulsoup, xlrd pre-installed

---
# HOW TO START WITH DOCKER:
* install docker from https://docs.docker.com/
* run command in Quick Docker Terminal `docker run -it —rm -p 8888:8888 lspvic/tensorboard-notebook`
* find configured IP address (by default 192.168.99.100).
* open a browser and make a call to http://192.168.99.100:8888 and enter a token from cmd.
---

Validation dataset used: 
https://github.com/zalandoresearch/fashion-mnist

it should be placed at data/fashion/ folder

---
# Siamese neural network
Siamese neural network is a class of neural network architectures that contain two identical sub-networks joined at their outputs. Identical here means that they have the same configuration with the same parameters and weights. Parameter updating occurs simultaneously in both networks.
The objective of the siamese neural network is not to classify input images, but to differentiate between a collection of same/different pairs or to evaluate new categories based on learned feature mappings for verification.

The architecture of Siamese neural networks is as follows. A Siamese neural networks consists of two identical neural subnetworks with the  same configurations (parameters and weights). Each subnetworks taking one of the two input images. Note that a pair of images are sent to the network in random order because Siamese neural networks have the symmetry property (if we reverse the order of the inputs to the neural network, the output should be the same). The last layers of the two networks are then fed to a contrastive loss function (or similarity metric), which calculates the similarity between the two images. Similarity metric is small if input images are from the same category, and large if they belong to different categories. Then the result obtained is used as input to a linear classifier that determines whether objects belong to the same or different class.

Siamese neural networks are popular among tasks related to finding similarities between two comparable things. Some examples are:
* signature verification;
* face recognition
* image comparison

---
# Our results
The aim of our work is to investigate the architecture of Siamese neural networks and the features of their application.

We create two models of the Siamese neural network for our research. The first model consists of three layers of a multilayer perceptron and the second model consists of four layers. Similarity between the two images is calculated using the Euclidean distance.
Our models are trained and tested on a dataset Fashion-MNIST (https://github.com/zalandoresearch/fashion-mnist). This dataset  consists of a training set of 60 000 examples and a test set of 10 000 examples. Each example is a 28x28 grayscale image, associated with a label from 10 classes.

We obtained the following results. The first model has an accuracy of 90.48% on a train and test dataset. The second model has an accuracy of 80.09% on a train dataset and 80% test dataset.
The first model has a quite good accuracy. The second model has an accuracy lower by 10%. Perhaps the low accuracy of the second model is due to the fact that the model was not trained enough. Therefore, it is necessary to learn more the second model in the future.

You can try to complicate these models or use another activation function or similarity metric to obtain higher accuracy. In addition, there is a desire to use CNN in the context of Siamese neural networks for tasks with higher dimensionality.
---
# References:
* https://sorenbouma.github.io/blog/oneshot/
* https://hackernoon.com/one-shot-learning-with-siamese-networks-in-pytorch-8ddaab10340e
* https://arxiv.org/pdf/1607.08438.pdf
* http://www.cs.cmu.edu/~rsalakhu/papers/oneshot1.pdf
* https://papers.nips.cc/paper/769-signature-verification-using-a-siamese-time-delay-neural-network.pdf
---
