FROM grafana/grafana:latest

MAINTAINER Bleza  <bleza.takouda@gmail.com>

LABEL version="1.0"

LABEL description="Grafana Image with added system variables"

RUN apt-get -q update &&\
    DEBIAN_FRONTEND="noninteractive" apt-get -q upgrade -y -o Dpkg::Options::="--force-confnew" --no-install-recommends &&\
    DEBIAN_FRONTEND="noninteractive" apt-get -q install -y -o Dpkg::Options::="--force-confnew" --no-install-recommends curl &&\
    apt-get -q autoremove &&\
    apt-get -q clean -y && rm -rf /var/lib/apt/lists/* && rm -f /var/cache/apt/*.bin


ADD run.sh /run.sh

RUN mkdir /opt/grafana

ADD ["*.json", "/opt/grafana/"]

EXPOSE 3000

#VOLUME ["/var/lib/grafana", "/var/log/grafana", "/etc/grafana"]


ENTRYPOINT ["/run.sh"]
