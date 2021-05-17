# Base image - Alternatives: Conda, Python...
FROM continuumio/miniconda3

# Metadata - optional
LABEL base.image="miniconda3"
LABEL version="0.1"
LABEL software="shasta"
LABEL software.version="0.6.0"
LABEL description="shasta assembler for long read data"
LABEL website="https://github.com/chanzuckerberg/shasta"
LABEL documentation=""
LABEL license=""
LABEL tags=""

# Maintainer
LABEL maintainer="Inês Mendes <cimendes@medicina.ulisboa.pt>""

# System essentials
RUN conda install -c conda-forge -c bioconda -c defaults shasta

# Set up workd