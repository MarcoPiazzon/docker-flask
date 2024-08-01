FROM ubuntu:22.04
RUN rm /bin/sh && ln -s /bin/bash /bin/sh

SHELL ["/bin/bash", "-c"]

FROM nginx
RUN rm /etc/nginx/conf.d/default.conf
COPY nginx.conf /etc/nginx/conf.d/
