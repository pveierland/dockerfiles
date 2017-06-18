FROM vii-tensorflow-gpu-py3-opencv3
MAINTAINER Per Magnus Veierland <pveierland@gmail.com>

RUN add-apt-repository -y ppa:otto-kesselgulasch/gimp && \
    apt-get update && \
    apt-get install -y --no-install-recommends gmic && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*