# Base image - Alternatives: Conda, Python...
FROM continuumio/miniconda3

# Metadata - optional
LABEL base.image="miniconda3"
LABEL version="0.1"
LABEL software="wtdbg2"
LABEL software.version="2.5.0"
LABEL description="wtdbg2 assembler for long read data"
LABEL website="https://github.com/ruanjue/wtdbg2"
LABEL documentation=""
LABEL license=""
LABEL tags=""

# Maintainer
LABEL maintainer="Inês Mendes <cimendes@medicina.ulisboa.pt>"

# System essentials
RUN conda install -c conda-forge -c bioconda -c defaults wtdbg

# Set up work