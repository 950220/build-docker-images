FROM nginx:latest

RUN mkdir -p /sdata/www/
ADD dist.tar.gz /sdata/www/
RUN rm -f /etc/nginx/conf.d/*
COPY nginx.conf /etc/nginx/conf.d 
EXPOSE 80
ENTRYPOINT ["/usr/sbin/nginx","-g","daemon off;"]
