FROM tensorflow/tensorflow:latest-gpu
MAINTAINER Per Magnus Veierland <pveierland@gmail.com>

ENV PYTHONPATH=$PYTHONPATH:/vii_util:/tensorflow/tensorflow/models/research:/tensorflow/tensorflow/models/research/slim

RUN apt-get update && \
    apt-get install -y --no-install-recommends git protobuf-compiler && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    pip install jupyter lxml matplotlib pillow && \
    mkdir /tensorflow && \
    cd /tensorflow && \
    git clone https://github.com/tensorflow/tensorflow.git . && \
    rm -rf .git

RUN pip install plotly pymongo pyyaml seaborn tqdm
