FROM alpine:3.8

MAINTAINER eaptekar <eaptekar@student.unit.ua>

RUN	apk update && \
	apk upgrade && \
	apk add vim

ENTRYPOINT vim

#docker build -t ex00 .
#docker run --rm -ti ex00