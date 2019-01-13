# Description: test image
FROM busybox:latest
LABEL maintainer="Oliverlin <yuyuud@gmail.com>"
ENV DOC_ROOT=/data/web/html/ \
    WEB_SERVER_PACKAGE="nginx-1.15.7.tar.gz"

COPY index.html ${DOC_ROOT:-/data/web/html/}
COPY yum.repos.d /etc/yum.repos.d/
ADD  http://nginx.org/download/${WEB_SERVER_PACKAGE} /usr/local/src/

WORKDIR /usr/local/

# ADD ${WEB_SERVER_PACKAGE} ./src/

VOLUME /data/mysql/

EXPOSE 80/tcp
RUN cd /usr/local/src && \
    tar xf ${WEB_SERVER_PACKAGE}
   