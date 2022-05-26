FROM bitnami/postgresql:13

USER root
# RUN sed -i 's/archive.ubuntu.com/mirrors.ustc.edu.cn/g' /etc/apt/sources.list
RUN install_packages build-essential wget libcurl4-gnutls-dev librtmp-dev


ENV PGSQL_HTTP_VER=1.5.0

# curl-config not found issue:
# https://gist.github.com/lxneng/1031014/f643787d9df008109656638095e2e7192ae8414a
RUN mkdir -p /tmp/pgsql-http && cd /tmp/pgsql-http && \
  wget  -O - https://github.com/pramsey/pgsql-http/archive/refs/tags/v$PGSQL_HTTP_VER.tar.gz > pgsql-http.tgz && \
  tar zxvf pgsql-http.tgz && \
  cd pgsql-http-$PGSQL_HTTP_VER && \
  make && make install && \
  cd /tmp && rm -rf /tmp/pgsql-http

USER 1001
