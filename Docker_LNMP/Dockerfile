#Dockerfile
FROM nginx, mysql, php:7
ENV HOME /root
RUN docker pull --name nginx -d -p 80:80 --link php7 -v /home/luisjordan/Escritorio/Docker/wordpress:/var/www/html -v /home/luisjordan/Escritorio/Docker/config_nginx/:/etc/nginx/conf.d nginx
RUN docker pull --name php7 --link luis:luis -v /home/luisjordan/Escritorio/Docker/wordpress:/var/www/html -v /home/luisjordan/Escritorio/Docker/config_php:/usr/local/etc/php -d php:7.0-fpm
RUN docker pull --name luis -d -p 3306:3306 -e MYSQL_ROOT_PASSWORD=123456 -e MYSQL_DATABASE=ejemplo mysql
EXPOSE 3306
EXPOSE 80 
