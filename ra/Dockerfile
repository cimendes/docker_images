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
RUN apt-get update && apt-get -y install build-essential \
                                         cmake \
                                         zlib1g-dev

# Install RA
RUN git clone --recursive https://github.com/rvaser/ra.git ra
WORKDIR ra
RUN mkdir build && cd build && cmake -DCMAKE_BUILD_TYPE=Release ..
RUN cd build && make

ENV PATH /ra/build/bin:$PATH

# PS for nextflow
RUN apt-get install -y procps