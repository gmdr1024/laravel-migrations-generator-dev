# image
FROM amazonlinux:2

# install epel, remi
RUN amazon-linux-extras install -y epel
RUN yum install -y https://rpms.remirepo.net/enterprise/remi-release-7.rpm

# install apache
RUN yum install -y httpd \
  && yum clean all

COPY ./entrypoint.sh /
RUN chmod 755 /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]
