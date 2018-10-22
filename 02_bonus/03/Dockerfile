FROM ubuntu

COPY Life.java /tmp

RUN apt-get update && \
	apt-get upgrade -y && \
	apt-get install -y default-jdk default-jre git vim

WORKDIR /tmp

RUN javac Life.java

CMD java -classpath . Life

# docker build -t bonus03 .
# docker run -it --rm bonus03