FROM node

WORKDIR /var/www/app
COPY app /var/www/app

EXPOSE 3000

RUN apt-get update && \
	apt-get install -y apt-transport-https && \
	curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -
RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list
RUN apt-get update && \
	apt-get install yarn && \
	yarn

CMD node index.js

# docker build -t bonus04 .
# docker run -it --rm -p 3000:3000 bonus04