# Base image - Alternatives: Conda, Python...
FROM continuumio/miniconda3

# Metadata - optional
LABEL base.image="miniconda3"
LABEL version="0.1"
LABEL software="raven-assembler"
LABEL software.version="1.5.0"
LABEL description="raven-assembler for long read data"
LABEL website="https://github.com/lbcb-sci/raven"
LABEL documentation=""
LABEL license=""
LABEL tags=""

# Maintainer
LABEL maintainer="Inês Mendes <cimendes@medicina.ulisboa.pt>"

# System essentials
RUN conda install -c conda-forge -c bioconda -c defaults raven-assembler

# PS for nextflow
RUN apt-get install -y procps