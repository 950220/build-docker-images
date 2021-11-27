FROM nginx:latest
RUN mv /etc/apt/sources.list /etc/apt/sources.list.bak
COPY sources.list /etc/apt/
RUN mkdir -p /data/www/
ADD dist.tar.gz /data/www/
RUN rm -f /etc/nginx/conf.d/*
COPY nginx.conf /etc/nginx/conf.d 
EXPOSE 80
ENTRYPOINT ["/usr/sbin/nginx","-g","daemon off;"]
