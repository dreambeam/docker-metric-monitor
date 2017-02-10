FROM telegraf:latest
MAINTAINER Bleza Takouda <bleza.takouda@gmail.com>
LABEL version="1.0"
LABEL description="Telegraf as an aggregator, image with custom system variables"

ADD telegraf.template.conf /telegraf.template.conf

ADD run.sh /run.sh

CMD ["/run.sh"]
