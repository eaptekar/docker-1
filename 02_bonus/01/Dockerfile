FROM debian:stretch

MAINTAINER eaptekar <eaptekar@student.unit.ua>

RUN apt-get update && \
	apt-get install -y cowsay fortune lolcat

ENTRYPOINT /usr/games/fortune | /usr/games/cowsay | /usr/games/lolcat

# docker build -t bonus01 .
# docker run -t --rm bonus01