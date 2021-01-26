FROM ubuntu:16.04
LABEL author="I Mendes"
LABEL email="cimendes@medicina.ulisboa.pt"
LABEL name="kraken2"
LABEL version="2.11"

WORKDIR /NGStools/

# INSTALL DEPENDENCIES
RUN apt-get update && apt-get -y install \
    bzip2 \
    gzip \
    python \
    python3 \
    wget

RUN apt-get -y install rsync

WORKDIR /NGStools

# INSTALL MINICONDA
RUN wget https://repo.continuum.io/miniconda/Miniconda2-latest-Linux-x86_64.sh
RUN chmod +x Miniconda2-latest-Linux-x86_64.sh
RUN ./Miniconda2-latest-Linux-x86_64.sh -b -p /NGStools/miniconda
ENV PATH="/NGStools/miniconda/bin:$PATH"
# Configure channels for bioconda
RUN conda config --add channels defaults && conda config --add channels conda-forge && \
    conda config --add channels bioconda

# INSTALL kraken & bracken
RUN conda install -c bioconda kraken2 bracken

WORKDIR /kraken_db

# Standard DB 8GB - for kraken2 and bracken 
RUN wget https://genome-idx.s3.amazonaws.com/kraken/k2_standard_8gb_20201202.tar.gz && \
    tar xf k2_standard_8gb_20201202.tar.gz && rm k2_standard_8gb_20201202.tar.gz

# 16S RDP 11.5 DB
RUN wget https://genome-idx.s3.amazonaws.com/kraken/16S_RDP11.5_20200326.tgz && \
    tar xf 16S_RDP11.5_20200326.tgz && rm 16S_RDP11.5_20200326.tgz

ENV KRAKEN2_DB_PATH="/kraken_db:${KRAKEN2_DB_PATH}"

WORKDIR /data/
