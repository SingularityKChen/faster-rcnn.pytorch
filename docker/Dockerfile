# faster-rcnn.pytorch
######################################
## stage 1: install dependencies
######################################
ARG UBUNTU_VERSION=20.04
ARG BASE_IMAGE=ubuntu:${UBUNTU_VERSION}

FROM ${BASE_IMAGE} AS builder
# set timezone
RUN apt-get update && apt-get install -y tzdata
ENV TZ=Asia/Singapore
# install dependencies and python3 libraries
RUN apt-get install -y git python3-pip curl software-properties-common python-dev python-tk libsm6 libxext6 libxrender-dev \
    && add-apt-repository universe \
    && apt-get update \
    && apt-get install -y python2 \
    && curl https://bootstrap.pypa.io/pip/2.7/get-pip.py --output get-pip.py \
    && python2 get-pip.py \
    && pip2 install numpy cython cffi opencv-python==4.2.0.32 scipy msgpack easydict matplotlib pyyaml tensorboardX torch torchvision future
