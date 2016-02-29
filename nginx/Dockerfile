FROM centos:7

RUN yum install -y epel-release \
 && curl -sL -o /etc/yum.repos.d/hnakamur-nginx.repo https://copr.fedoraproject.org/coprs/hnakamur/nginx/repo/epel-7/hnakamur-nginx-epel-7.repo \
 && yum install -y nginx

ENV TERM xterm
CMD ["/usr/sbin/nginx", "-g", "daemon off;"]
