FROM debian:stretch

MAINTAINER eaptekar <eaptekar@student.unit.ua>

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y ca-certificates openssh-server wget postfix tzdata && \
    apt-get clean && \
    wget https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh && \
    chmod 777 script.deb.sh && \
    ./script.deb.sh && \
    apt-get install -y gitlab-ce && \
    apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

EXPOSE 443 80 22

ENTRYPOINT /opt/gitlab/embedded/bin/runsvdir-start & gitlab-ctl reconfigure && echo "GitLab configured! Should be started now!" && wait

# docker-machine create -s /tmp -d virtualbox GitLabMachine
# eval $(docker-machine -s /tmp env GitLabMachine)
# docker build -t ex03 .
# docker run -it --rm -p 8080:80 -p 8022:22 -p 8443:443 --privileged ex03
# curl -L http://$(docker-machine -s /tmp ip GitLabMachine):8080
# docker-machine -s /tmp rm -y GitLabMachine
# eval $(docker-machine env Char)

