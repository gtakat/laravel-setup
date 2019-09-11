FROM nginx

RUN set -e \
      && apt-get update -y -qq \
      && apt-get install -y -qq git zip tzdata net-tools dnsutils procps \
      && cp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime \
      && echo "Asia/Tokyo" > /etc/timezone

ADD ./docker/nginx/site.conf /etc/nginx/conf.d/default.conf
