FROM fluxcapacitor/package-ubuntu-14.04

ENV PATH=/opt/conda/bin:$PATH

# Install Python with conda
RUN wget -q https://repo.continuum.io/miniconda/Miniconda3-4.0.5-Linux-x86_64.sh -O /tmp/miniconda.sh  && \
    echo 'a7bcd0425d8b6688753946b59681572f63c2241aed77bf0ec6de4c5edc5ceeac */tmp/miniconda.sh' | shasum -a 256 -c - && \
    bash /tmp/miniconda.sh -f -b -p /opt/conda && \
    /opt/conda/bin/conda install --yes python=2.7 sqlalchemy tornado jinja2 traitlets requests pip && \
    /opt/conda/bin/pip install --upgrade pip && \
    rm /tmp/miniconda.sh

RUN conda install --yes -c conda-forge tensorflow
RUN conda install --yes -c conda-forge matplotlib
RUN conda install --yes -c conda-forge pandas
RUN conda install --yes -c anaconda scikit-learn
