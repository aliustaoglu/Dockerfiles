FROM node:8.10-slim
LABEL maintainer="Cuneyt Aliustaoglu"

RUN cd tmp
RUN apt-get -y update
RUN apt-get -y install python-setuptools
RUN easy_install pip
RUN pip install esptool
RUN cd /

RUN npm install -g espruino-create-project

RUN mkdir espruino
RUN cd espruino
