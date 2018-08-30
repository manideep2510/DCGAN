# DCGAN

## About

Implementation of paper '[Unsupervised representation learning with Deep Convolutional Generative Adversarial Networks](https://arxiv.org/pdf/1511.06434.pdf)', Alec Radford, Luke Metz and Soumith Chintala.

This implementation is in `python3` using [Keras](https://keras.io/) framework with [Tensorflow](https://www.tensorflow.org/) as backend.

The model is trained on the [LUSN](http://lsun.cs.princeton.edu/2017/) dataset. 

The original dataset is in a somewhat awkward format (lmdb) and the widely-used bedroom category is very large (43GB), and it requires a python2-only script to download it. 

Therefore thERE is a repackaged version as a simple folder of jpgs, containing a random sample. The partial dataset with images in JPG format can be found at [LSUN bedroom scene 20% sample](https://www.kaggle.com/jhoward/lsun_bedroom/home) on Kaggle and is prepared by [Jeremy Howard](http://www.fast.ai/about/#jeremy).

When reading the images, folder arrangement of this dataset should be carefully taken care of.

## Files

- [`dcgan.py`](dcgan.py) : This is the code for python implementation of [Unsupervised representation learning with Deep Convolutional Generative Adversarial Networks](https://arxiv.org/pdf/1511.06434.pdf)
- [`images`](images) : DCGAN generated bedrooms at every sample interval (5) when training the model for 100 epochs

### Note

The model hasn't been trained on all the epochs due to hardware constraints. So, the images folder will only contain 1 image from first epoch (trained for 1 epoch just for the sake of testing whether the code is working or not).

I will be training the model and will update the repo soon.

## Usage

Clone the repository, change your present working directory to the cloned directory, Now create a now folder in this directory named `images` to save the generated images after every sampled interval and now train the model. Below commands accomplishes these steps.

```
$ git clone https://github.com/manideep2510/DCGAN.git
$ cd DCGAN
$ mkdir images
$ python dcgan.py
```

Download the dataset from [this link](https://www.kaggle.com/jhoward/lsun_bedroom/home).

In the [`dcgan.py`](dcgan.py) code when we are reading the images into a numpy array, take care of the images path carefully. You will be required to change that part of code as your paths for the images would be diffirent than mine.
