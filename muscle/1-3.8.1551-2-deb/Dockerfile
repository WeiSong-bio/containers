FROM biocontainers/biocontainers:vdebian-buster-backports_cv1
MAINTAINER biocontainers <biodocker@gmail.com>
LABEL    software="muscle" \ 
    base_image="biocontainers/biocontainers:vdebian-buster-backports_cv1" \ 
    container="muscle" \ 
    about.summary="Multiple alignment program of protein sequences" \ 
    about.home="http://www.drive5.com/muscle/" \ 
    software.version="1-3.8.1551-2-deb" \ 
    version="1" \ 
    extra.identifiers.biotools="muscle" \ 
    about.copyright=" Robert C. Edgar Bob <muscle@drive5.com>" \ 
    about.license="PD-dedication" \ 
    about.license_file="/usr/share/doc/muscle/copyright" \ 
    extra.binaries="/usr/bin/muscle" \ 
    about.tags="biology::format:aln, biology::peptidic, field::biology,:biology:bioinformatics, implemented-in::c++,:commandline, role::program, scope::utility, use::comparing,:plaintext, works-with::TODO" 

USER root
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update && (apt-get install -t buster-backports -y muscle || apt-get install -y muscle) && apt-get clean && apt-get purge && rm -rf /var/lib/apt/lists/* /tmp/*
USER biodocker
