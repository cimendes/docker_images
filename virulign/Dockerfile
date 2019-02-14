FROM ubuntu:16.04
MAINTAINER Inês Mendes <cimendes@medicina.ulisboa.pt>

WORKDIR /NGStools

RUN apt-get update

# Dependencies
RUN apt-get install -y wget

# Virulign
WORKDIR virulign
RUN wget https://github.com/rega-cev/virulign/releases/download/v1.0.1/virulign-linux-64bit.tgz
RUN tar xzf virulign-linux-64bit.tgz && rm virulign-linux-64bit.tgz
ENV PATH="/NGStools/virulign:${PATH}"

# Reference sequences
WORKDIR references

# DENV
RUN wget https://raw.githubusercontent.com/rega-cev/virulign/master/references/DENV/DENV1-NC001477.xml
RUN wget https://raw.githubusercontent.com/rega-cev/virulign/master/references/DENV/DENV2-NC001474.xml
RUN wget https://raw.githubusercontent.com/rega-cev/virulign/master/references/DENV/DENV3-NC001475.xml
RUN wget https://raw.githubusercontent.com/rega-cev/virulign/master/references/DENV/DENV4-NC002640.xml

# CHIKV
RUN wget https://raw.githubusercontent.com/rega-cev/virulign/master/references/CHIKV/CHIKV-NC004162-gp1.xml
RUN wget https://raw.githubusercontent.com/rega-cev/virulign/master/references/CHIKV/CHIKV-NC004162-gp2.xml

# HIV
RUN wget https://raw.githubusercontent.com/rega-cev/virulign/master/references/HIV/HIV-HXB2-env.xml
RUN wget https://raw.githubusercontent.com/rega-cev/virulign/master/references/HIV/HIV-HXB2-gag.xml
RUN wget https://raw.githubusercontent.com/rega-cev/virulign/master/references/HIV/HIV-HXB2-pol.xml

# ZIKV
RUN wget https://raw.githubusercontent.com/rega-cev/virulign/master/references/ZIKV/ZIKV-rega.xml

