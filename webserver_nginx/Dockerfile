FROM alpine:latest

EXPOSE 8080

COPY setup_nginx.sh .
COPY start_nginx.sh .

RUN chmod +x ./setup_nginx.sh
# RUN chmod +x ./start_nginx.sh

RUN ./setup_nginx.sh

COPY config/nginx.conf /etc/nginx/nginx.conf
COPY src/ /www/

COPY config/supervisord.conf /etc/supervisor/conf.d/supervisord.conf

# USER nobody

CMD ["/usr/bin/supervisord", "-c", "/etc/supervisor/conf.d/supervisord.conf"]
# CMD ["./start_nginx.sh"]

# CMD ["./setup_nginx.sh"]

# CMD ["nginx", "-g", "daemon off;"]

# CMD ["rc-service", "nginx", "start"]

# CMD ["service", "nginx", "start"]


############## fetch stage ##############

############## packages stage ##############

############## build stage ##############

############## runtine stage ##############