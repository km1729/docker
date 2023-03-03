FROM docker.io/conda/miniconda3

WORKDIR /app

COPY ./app/requirement.txt /app

RUN apt update -y && apt upgrade -y && \
    conda update conda 
RUN pip install --no-cache-dir -r requirement.txt
RUN conda install -c conda-forge cylc-flow
RUN conda install -c conda-forge cylc-uiserver
RUN conda install -c conda-forge cylc-rose metomi-rose


VOLUME ./app
