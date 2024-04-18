FROM nginx:1.25
COPY default.conf /etc/nginx/conf.d/default.conf
RUN apt update && \
    apt install wget
RUN wget https://github.com/nginxinc/nginx-prometheus-exporter/releases/download/v1.1.0/nginx-prometheus-exporter_1.1.0_linux_amd64.tar.gz && \
    tar -xvf nginx-prometheus-exporter_1.1.0_linux_amd64.tar.gz && \
    mv nginx-prometheus-exporter /usr/local/bin/
EXPOSE 8000
CMD ["nginx", "-g", "daemon off;"]