FROM debian:stretch

MAINTAINER eaptekar <eaptekar@student.unit.ua>

ENV TS3SERVER_LICENSE="accept"

WORKDIR /home/teamspeak

RUN apt-get update && \
    apt-get -y upgrade && \
    apt-get -y install bzip2 wget && \
    wget "http://dl.4players.de/ts/releases/3.4.0/teamspeak3-server_linux_amd64-3.4.0.tar.bz2" && \
    tar -xvjf "teamspeak3-server_linux_amd64-3.4.0.tar.bz2"

ENTRYPOINT sh /home/teamspeak/teamspeak3-server_linux_amd64/ts3server_minimal_runscript.sh

# docker build -t ex01 .
# docker run --rm -p 9987:9987/udp -p 10011:10011 -p 30033:30033 ex01
# nc $(docker-machine ip Char) 10011