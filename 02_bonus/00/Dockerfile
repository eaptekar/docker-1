FROM alpine

MAINTAINER eaptekar <eaptekar@student.unit.ua>

RUN apk update && \
	apk add busybox-extras

ENTRYPOINT telnet towel.blinkenlights.nl 23

# docker build -t bonus00 .
# docker run -it --rm bonus00