FROM cimendes/midas:1.3.2-0.1

# MIDAS DB v1.2
WORKDIR /MidasDB
RUN wget http://lighthouse.ucsf.edu/MIDAS/midas_db_v1.2.tar.gz
RUN tar xf midas_db_v1.2.tar.gz
RUN rm midas_db_v1.2.tar.gz

ENV PATH="/MidasDB:$PATH"