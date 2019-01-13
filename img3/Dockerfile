FROM nginx:1.14-alpine

ARG author="Oliver lin <yuyuud@gmail.com>"
LABEL maintainer="${author}"

ENV NGX_DOC_ROOT="/data/web/html/"

ADD index.html ${NGX_DOC_ROOT}
ADD entrypoint.sh /bin/

EXPOSE 80/tcp

HEALTHCHECK --start-period=3s CMD wget -O - -q http://${IP:-0.0.0.0}:${PORT:-80}/


CMD ["/usr/sbin/nginx", "-g", "daemon off;"]
ENTRYPOINT ["/bin/entrypoint.sh"]