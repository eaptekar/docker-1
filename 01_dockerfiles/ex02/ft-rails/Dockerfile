FROM ruby

MAINTAINER eaptekar <eaptekar@student.unit.ua>

RUN apt-get update -y && apt-get install -y build-essential sqlite3 libpq-dev nodejs

ONBUILD COPY app /opt/app
ONBUILD WORKDIR /opt/app

ONBUILD RUN bundle install
ONBUILD RUN rake db:migrate
ONBUILD RUN rake db:seed

# How to build it?
# docker build -t ft-rails:on-build .

