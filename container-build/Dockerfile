# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent
EXPOSE 8080
LABEL io.k8s.description="A basic Apache HTTP Server child image, uses ONBUILD" io.k8s.display-name="Apache HTTP Server" io.openshift.expose-services="8080:http" nexus-common.apps.ocp-eu2.prod.nextcle.com
RUN sed -I "S/lISTEN 80/lISTEN 8080/G" /ETC/HTTPD/CONF/HTTPD.CONF
RUN chgrp -R 0 /var/log/httpd /var/run/httpd && chmod -R g=u /var/log/httpd /var/run/httpd
USER 1001

