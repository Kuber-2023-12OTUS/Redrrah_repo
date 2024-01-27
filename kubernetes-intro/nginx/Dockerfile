FROM nginx:latest
COPY default.conf /etc/nginx/conf.d/default.conf
WORKDIR /homework
COPY ./homework.html .
COPY ./homework.html ./index.html
RUN usermod -u 1001 nginx \
  && groupmod -g 1001 nginx
RUN chown -R nginx:nginx /homework
EXPOSE 8000
CMD ["nginx", "-g", "daemon off;"]