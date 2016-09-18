FROM fluxcapacitor/package-ubuntu-14.04
FROM fluxcapacitor/package-java-1.8

ENV SPARK_VERSION=1.6.1
ENV SPARK_HOME=/root/spark-${SPARK_VERSION}-bin-fluxcapacitor

WORKDIR /root

RUN \
  # This is not a custom version of Spark.  It's merely a version with all the desired -P profiles enabled.
  wget https://s3.amazonaws.com/fluxcapacitor.com/packages/spark-${SPARK_VERSION}-bin-fluxcapacitor.tgz \
  && tar xvzf spark-${SPARK_VERSION}-bin-fluxcapacitor.tgz \
  && rm spark-${SPARK_VERSION}-bin-fluxcapacitor.tgz
