# Base image - Alternatives: Conda, Python...
FROM continuumio/miniconda3

# Metadata - optional
LABEL base.image="miniconda3"
LABEL version="0.1"
LABEL software="ra"
LABEL software.version="0.9.0"
LABEL description="ra assembler for long read data"
LABEL website="https://github.com/lbcb-sci/ra"
LABEL documentation=""
LABEL license=""
LABEL tags=""

# Maintainer
LABEL maintainer="Inês Mendes <cimendes@medicina.ulisboa.pt>"

# System essentials
RUN conda install -c bioconda ra
