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
* run command in Quick Docker Terminal `docker run -it —rm -p 8888:8888 jupyter/tensorflow-notebook`
* find configured IP address (by default 192.168.99.100).
* open a browser and make a call to http://192.168.99.100:8888 and enter a token from cmd.
---

Validation dataset used: 
https://github.com/zalandoresearch/fashion-mnist

it should be placed at data/fashion/ folder


---
# References:
* https://sorenbouma.github.io/blog/oneshot/
* https://hackernoon.com/one-shot-learning-with-siamese-networks-in-pytorch-8ddaab10340e
* https://arxiv.org/pdf/1607.08438.pdf
---
