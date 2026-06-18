FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y --no-install-recommends \
    ca-certificates \
    git \
    cmake \
    build-essential \
    libboost-all-dev \
    libeigen3-dev \
    libpcl-dev \
 && update-ca-certificates \
 && rm -rf /var/lib/apt/lists/*
 
# Build the ETH3D binaries
RUN git clone https://github.com/ETH3D/multi-view-evaluation.git
RUN cd multi-view-evaluation; mkdir build; cd build; cmake ../. ; make;
