FROM jupyter/datascience-notebook

## install imagemagick
USER root

#RUN conda install -c conda-forge imagemagick

ENV SHELL=/bin/bash

# Hack for controlling how chromium works with no-sandbox and allow-downloads
RUN mkdir -p /home/jovyan/.jupyter
COPY .devcontainer/jupyter_lab_config.py /home/jovyan/.jupyter/jupyter_lab_config.py

RUN fix-permissions /home/jovyan/.jupyter

USER ${NB_UID}

RUN jupyter server extension disable nbclassic  

