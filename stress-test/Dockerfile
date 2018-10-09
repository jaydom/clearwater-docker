#FROM clearwater/base
FROM registry.cn-shenzhen.aliyuncs.com/jaydomchen/clearwater:base
MAINTAINER maintainers@projectclearwater.org

RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y --force-yes clearwater-sip-stress-coreonly

EXPOSE 5082/udp 5082/tcp 
