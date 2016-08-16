FROM fluxcapacitor/utils-ubuntu-14.04

# Update and install local dependencies
RUN \
  apt-get update --fix-missing \
  && apt-get install -y \
     wget \
     git
  
# Install Anaconda3
RUN \ 
  wget --quiet http://repo.continuum.io/archive/Anaconda3-4.1.1-Linux-x86_64.sh -O ~/anaconda.sh \
  && /bin/bash ~/anaconda.sh -b -p /opt/conda \
  && rm ~/anaconda.sh

ENV PATH /opt/conda/bin:$PATH

# Install tini
ENV TINI_VERSION v0.10.0
ADD https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini /usr/local/bin/tini
RUN chmod +x /usr/local/bin/tini

RUN curl -L https://github.com/krallin/tini/releases/download/v0.10.0/tini > tini \
  && echo "1361527f39190a7338a0b434bd8c88ff7233ce7b9a4876f3315c22fce7eca1b0 *tini" | sha256sum -c - \
  && mv tini /usr/local/bin/tini \
  && chmod +x /usr/local/bin/tini 


ENTRYPOINT ["/usr/local/bin/tini", "--"]
CMD ["/bin/bash"]
