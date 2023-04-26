FROM continuumio/miniconda3

RUN apt-get update -y; apt-get upgrade -y; apt-get install -y vim-tiny vim-athena ssh

COPY .docker/environment.yml /asl/environment.yml
WORKDIR /asl

RUN conda env create -f environment.yml
RUN echo "alias l='ls -lah'" >> ~/.bashrc
RUN echo "source activate asl" >> ~/.bashrc

# Setting these environmental variables is the functional equivalent of running 'source activate my-conda-env'
ENV CONDA_EXE /opt/conda/bin/conda
ENV CONDA_PREFIX /opt/conda/envs/asl
ENV CONDA_PYTHON_EXE /opt/conda/bin/python
ENV CONDA_PROMPT_MODIFIER (asl)
ENV CONDA_DEFAULT_ENV asl
ENV PATH /opt/conda/envs/asl/bin:/opt/conda/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin


