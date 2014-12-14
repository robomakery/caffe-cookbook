# caffe-cookbook

Chef cookbook for installing the [Caffe deep learning framework](http://caffe.berkeleyvision.org/).

It was developed using an AWS g2.2xlarge instance running Ubuntu 14.04 (base Ubuntu AMI used was: [ami-4ae27e22](http://thecloudmarket.com/image/ami-4ae27e22--ubuntu-images-hvm-ssd-ubuntu-trusty-14-04-amd64-server-20141125)).

It installs [CUDA](http://www.nvidia.com/object/cuda_home_new.html), [cuDNN](https://developer.nvidia.com/cuDNN) (see notes below), [Caffe](http://caffe.berkeleyvision.org/), and Caffe's python bindings.

## cuDNN

In order to have the cookbook compile Caffe with cuDNN support, you need to download the cuDNN tarball from the NVIDIA website.

You first need to create a CUDA Registered Developer account, wait for the account to be activated, and then download the cuDNN tarball.  Once you have the tarball (cudnn-6.5-linux-R1.tgz as of Dec 2014), you should place it in the files/default/cudnn-tarball directory.  This will trigger the cookbook to install it and use it when compiling Caffe.
