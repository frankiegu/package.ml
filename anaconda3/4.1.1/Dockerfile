FROM fluxcapacitor/utils-ubuntu-14.04

RUN \
  apt-get update --fix-missing \
  && apt-get install -y \
     wget \
     bzip2 \
     ca-certificates \
     libglib2.0-0 \
     libxext6 \
     libsm6 \
     libxrender1 \
     git \
     mercurial \
     subversion
  
  RUN \ 
    wget --quiet http://repo.continuum.io/archive/Anaconda3-4.1.1-Linux-x86_64.sh -O ~/anaconda.sh \
    && /bin/bash ~/anaconda.sh -b -p /opt/conda \
    && rm ~/anaconda.sh

ENV PATH /opt/conda/bin:$PATH

