FROM centos:7.2.1511

RUN yum install -y epel-release \
  && yum install -y httpd git

RUN git clone https://github.com/jonberenguer/jsonviewer.git /var/www/html


ENTRYPOINT ["/usr/sbin/apachectl", "-d", "/etc/httpd/conf", "-f", "httpd.conf", "-e", "info", "-DFOREGROUND"]