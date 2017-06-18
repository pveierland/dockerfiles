FROM gcr.io/tensorflow/tensorflow:latest-gpu
MAINTAINER Per Magnus Veierland <pveierland@gmail.com>

ENV PYTHONPATH=$PYTHONPATH:/tensorflow/tensorflow/models:/tensorflow/tensorflow/models/slim

RUN apt-get update && \
    apt-get install -y --no-install-recommends git protobuf-compiler && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    pip install jupyter lxml matplotlib pillow && \
    mkdir /tensorflow && \
    cd /tensorflow && \
    git clone https://github.com/tensorflow/tensorflow.git . && \
    rm -rf .git && \
    cd tensorflow && \
    git clone https://github.com/tensorflow/models.git && \
    cd models && \
    rm -rf .git && \
    protoc object_detection/protos/*.proto --python_out=.

RUN pip install pymongo pyyaml tqdm