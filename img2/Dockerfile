FROM busybox
LABEL maintainer="Oliver lin <yuyuud@gmail.com>" app="httpd"

ENV WEB_DOC_ROOT='/data/web/html/'

RUN mkdir -p ${WEB_DOC_ROOT} && \
echo "<h1>Busybox httpd server.</h1>" > ${WEB_DOC_ROOT}/index.html

# CMD /bin/httpd -f -h ${WEB_DOC_ROOT}
# CMD ["/bin/sh", "-c", "/bin/httpd -f -h ${WEB_DOC_ROOT}"]
CMD ["/bin/httpd -f -h /data/web/html"]
ENTRYPOINT ["/bin/sh", "-c"]