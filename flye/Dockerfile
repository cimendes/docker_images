# Base image - Alternatives: Conda, Python...
FROM continuumio/miniconda3

# Metadata - optional
LABEL base.image="miniconda3"
LABEL version="0.1"
LABEL software="flye"
LABEL software.version="2.8.3"
LABEL description="Flye Assembler for long read data"
LABEL website="https://github.com/fenderglass/Flye"
LABEL documentation=""
LABEL license=""
LABEL tags=""

# Maintainer
LABEL maintainer="Inês Mendes <cimendes@medicina.ulisboa.pt>"

# System essentials
RUN conda install -c conda-forge -c bioconda -c defaults flye

# Set up workdir for installation 
WORKDIR /data
