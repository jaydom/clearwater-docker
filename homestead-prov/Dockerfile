#FROM clearwater/base
FROM registry.cn-shenzhen.aliyuncs.com/jaydomchen/clearwater:base
MAINTAINER maintainers@projectclearwater.org

RUN sudo apt-get update && sudo DEBIAN_FRONTEND=noninteractive apt-get install -y --force-yes homestead-prov clearwater-prov-tools

COPY homestead-prov.supervisord.conf /etc/supervisor/conf.d/homestead-prov.conf
COPY nginx.supervisord.conf /etc/supervisor/conf.d/nginx.conf
COPY clearwater-group.supervisord.conf /etc/supervisor/conf.d/clearwater-group.conf

# We need to start the socket factories so that we can write to SAS.
RUN cp /etc/clearwater/socket-factory.supervisord.conf /etc/supervisor/conf.d/

EXPOSE 8889
