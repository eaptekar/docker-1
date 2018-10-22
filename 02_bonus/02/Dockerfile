FROM alpine

RUN apk --no-cache add \
	shadow \
	zsh \
	&& chsh -s /bin/zsh \
	&& apk add gcc libc-dev make binutils gdb vim git


ENV SHELL /usr/bin/zsh

WORKDIR /root
ENTRYPOINT /bin/zsh

# docker build -t bonus02 .
# docker run -it --rm bonus02