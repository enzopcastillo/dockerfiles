FROM nginx

RUN useradd enzo

COPY web-TP03/ /usr/share/nginx/html

ENV archivo docker

WORKDIR /usr/share/nginx/html

RUN echo "${archivo}" > /usr/share/nginx/html/env.html

EXPOSE 90

LABEL version=1

USER enzo

RUN echo "I am $(whoami)" > /tmp/test.html

USER root

RUN cp /tmp/test.html /usr/share/nginx/html/docker.html

VOLUME /var/log/nginx

CMD nginx -g 'daemon off;'
