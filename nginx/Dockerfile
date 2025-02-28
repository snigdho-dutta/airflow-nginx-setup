
FROM nginx:latest

ARG NGINX_CONF_DIR

COPY ./nginx.conf /etc/nginx/nginx.conf
COPY ./${NGINX_CONF_DIR}/default.conf /etc/nginx/conf.d/default.conf
EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]