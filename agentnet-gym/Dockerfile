FROM continuumio/anaconda

MAINTAINER Dmitry Persiyanov <dmitry.persiyanov@gmail.com>

# Install build-essential, cmake and other dependencies
RUN apt-get clean && apt-get update && apt-get install -y \
  build-essential \
  cmake \
  libopenblas-dev \
  zlib1g-dev \
  libjpeg-dev

RUN apt-get install -y \
    xvfb libav-tools xorg-dev python-opengl swig

# Install bleeding-edge Theano
RUN pip install --upgrade --no-deps git+git://github.com/Theano/Theano.git

RUN pip install --upgrade https://github.com/Lasagne/Lasagne/archive/master.zip

# Install AgentNet
RUN git clone https://github.com/justheuristic/AgentNet ~/AgentNet \
    && cd ~/AgentNet \
    && python setup.py install

# Install OpenAI Gym
RUN git clone https://github.com/openai/gym ~/gym \
    && cd ~/gym \
    && pip install -e .[all]


WORKDIR /root