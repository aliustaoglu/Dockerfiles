FROM ubuntu:16.04

RUN apt-get -y update
RUN apt-get -y upgrade
RUN apt-get install -y software-properties-common
RUN apt-add-repository -y ppa:jeffreyratcliffe/ppa
RUN apt-get -y install gscan2pdf

CMD ["gscan2pdf"]
