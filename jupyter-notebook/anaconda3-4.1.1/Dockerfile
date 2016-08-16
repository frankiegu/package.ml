FROM fluxcapacitor/utils-anaconda3:4.1.1

# Put contents of local directory into image
ADD . /usr/src/jupyter-notebook

# Add a notebook profile
RUN \
  mkdir -p -m 700 /root/.jupyter/ \
  && echo "c.NotebookApp.ip = '*'" >> /root/.jupyter/jupyter_notebook_config.py

VOLUME /notebooks
WORKDIR /notebooks

EXPOSE 8888

ENTRYPOINT ["tini", "--"]
CMD ["jupyter", "notebook", "--no-browser"]
