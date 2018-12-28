FROM aliustaoglu/ubuntu

RUN apt-get update -y
RUN add-apt-repository ppa:mc3man/mpv-tests -y
RUN apt-get install mpv -y

CMD ["mpv ", "$1"]
