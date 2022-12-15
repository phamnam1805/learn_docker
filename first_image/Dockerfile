FROM ubuntu:20.04
LABEL maintainer="nam.pv1805@gmail.com"

RUN apt-get update

ENV TZ=Asia/Ho_Chi_Minh
RUN set -x \
    && ln -snf /usr/share/zoneinfo/$TZ /etc/localtime \
    && echo $TZ > /etc/timezone
    
RUN apt-get install -y nginx

WORKDIR /venv
COPY start.sh /venv
RUN chmod a+x /venv/*
ENTRYPOINT ["/venv/start.sh"]
EXPOSE 80
