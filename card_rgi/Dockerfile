FROM continuumio/miniconda3@sha256:456e3196bf3ffb13fee7c9216db4b18b5e6f4d37090b31df3e0309926e98cfe2

# Metadata
LABEL software="CARD_RGI" \
      software.version="5.1.1" \
      about.home="https://github.com/arpcard/rgi" 

RUN apt-get update \
  && apt-get install procps wget -y

RUN conda install python=3.6

RUN conda install --channel bioconda --channel conda-forge --channel defaults rgi=5.1.1

RUN wget https://card.mcmaster.ca/latest/data
RUN tar -xvf data ./card.json
RUN rgi card_annotation -i card.json > card_annotation.log 2>&1 && \
    rgi load -i card.json --card_annotation card_database_v*.fasta
