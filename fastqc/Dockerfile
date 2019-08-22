FROM ubuntu:16.04
MAINTAINER Inês Mendes <cimendes@medicina.ulisboa.pt>

RUN apt-get update && apt-get -y install \
    openjdk-8-jre \
    perl \
	python3 \
    unzip

RUN apt install procps

ADD http://www.bioinformatics.babraham.ac.uk/projects/fastqc/fastqc_v0.11.7.zip /NGStools/

WORKDIR /NGStools

# Install FastQC
RUN	unzip fastqc_*.zip && \
	chmod +x FastQC/fastqc && \
	rm -rf fastqc_*.zip

ENV PATH="/NGStools/FastQC:$PATH"