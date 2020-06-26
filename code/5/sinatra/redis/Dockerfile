FROM ubuntu:14.04
MAINTAINER James Turnbull "james@example.com"
ENV REFRESHED_AT 2014-06-01

RUN apt-get update
RUN apt-get -y install redis-server redis-tools
RUN sysctl -w vm.overcommit_memory=1

EXPOSE 6379

ENTRYPOINT ["/usr/bin/redis-server"]
CMD []
