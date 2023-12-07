FROM ubuntu:20.04

RUN apt-get update
RUN apt install -y  make \
		    mpich \
		    gfortran

RUN apt install -y git-core

RUN git clone https://github.com/ParaFEM/ParaFEM.git

WORKDIR /ParaFEM/parafem

RUN ./make-parafem MACHINE=Linuxdesktop

ENV PATH ="${PATH}":/ParaFEM/parafem/bin
WORKDIR /ParaFEM/parafem/examples

RUN mkdir /scratch

ENTRYPOINT /bin/bash

