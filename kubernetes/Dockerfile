FROM fluxcapacitor/package-ubuntu-14.04

ENV KUBERNETES_RELEASE=v1.3.7
ENV KUBERNETES_HOME=/root/kubernetes/

WORKDIR /root

RUN \
  wget https://storage.googleapis.com/kubernetes-release/release/$KUBERNETES_RELEASE/kubernetes.tar.gz

RUN \
  tar -xzvf kubernetes.tar.gz \
  && rm kubernetes.tar.gz

RUN \
  sudo cp $KUBERNETES_HOME/platforms/linux/amd64/kubectl /usr/local/bin/kubectl \
  && sudo chmod a+x /usr/local/bin/kubectl
