FROM aliustaoglu/ubuntu

RUN apt-get update -y
RUN add-apt-repository ppa:qbittorrent-team/qbittorrent-stable -y
RUN apt-get install qbittorrent -y

CMD ["qbittorrent"]
