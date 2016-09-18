FROM fluxcapacitor/package-ubuntu-14.04
FROM fluxcapacitor/package-java-1.8

# TODO:  Figure out why pip isn't being found from utils-ubunt-14.04 above ^
RUN \
  apt-get update \
  && apt-get install -y python-dev \
  && apt-get install -y python-pip \
  && apt-get install -y git  

RUN \
  git clone https://github.com/edenhill/librdkafka.git \
  && cd librdkafka \
  && ./configure \
  && make \
  && make install

RUN \
#  apt-get install -y librdkafka1 \
  pip install --upgrade confluent-kafka
  
