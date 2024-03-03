ARG UPSTREAM_TAG

FROM kasmweb/chrome:${UPSTREAM_TAG}

USER root

# https://github.com/kasmtech/workspaces-core-images/issues/2
RUN <<EOF
    sed -i 's/-sslOnly //g' /dockerstartup/vnc_startup.sh
    sed -i 's/require_ssl: true/require_ssl: false/g'  /usr/share/kasmvnc/kasmvnc_defaults.yaml
EOF

USER 1000
