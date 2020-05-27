# Reproducible results with Tensorflow?

This notebook was tested with Python 3.6 and Tensorflow 2.0 and Tensorflow 2.1. It was created to demonstrate an example for non-deterministic behaviour in training. The example was tested with these containers
nvcr.io/nvidia/tensorflow:19.12-tf2-py3
nvcr.io/nvidia/tensorflow:20.01-tf2-py3
nvcr.io/nvidia/tensorflow:20.02-tf2-py3

Start like this (using your current directory):
docker run -it --gpus all -p 8888:8888 --rm -v `pwd`:`pwd` -w `pwd` nvcr.io/nvidia/tensorflow:19.12-tf2-py3
or
docker run -it --gpus all -p 8888:8888 --rm -v `pwd`:`pwd` -w `pwd` nvcr.io/nvidia/tensorflow:20-02-tf2-py3

Start jupyter notebook in the container 
jupyter notebook --ip 0.0.0.0 --port 8888 --allow-root

Open the browser localhost:8888 on your local computer


This first exercise considers the 
1. randomtf.random.set_seed function and  
2. training of a simple convolutional network using keras (TF2)

