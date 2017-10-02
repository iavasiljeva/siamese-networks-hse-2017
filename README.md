# siamese-networks-hse-2017

In this project we are using TensorFlow Docker image from docker-stacks: 
https://github.com/jupyter/docker-stacks/tree/master/tensorflow-notebook

HOW TO:
* install docker from https://docs.docker.com/
* git clone https://github.com/jupyter/docker-stacks.git
* run command in Quick Docker Terminal docker run -it —rm -p 8888:8888 jupyter/tensorflow-notebook
It will start Docker Container. Find configured IP address (by default 192.168.99.100).
If everything is fine, open a browser and make a call to http://192.168.99.100:8888 and enter a token from cmd.

Validation dataset used: 
https://github.com/zalandoresearch/fashion-mnist

it should be placed at data/fashion/ folder
