from centos:latest
run yum -y install php-fpm 
run sed -i '/^daemon/s/yes/no/g' /etc/php-fpm.conf  && sed  's#/run/php-fpm/www.sock#0.0.0.0:9000#g' -i /etc/php-fpm.d/www.conf && sed  's#/run/php-fpm/php-fpm.pid#/var/run/php-fpm.pid#g' -i  /etc/php-fpm.conf && sed -i '/listen.allow/d' /etc/php-fpm.d/www.conf
expose 9000
CMD ["php-fpm","-R"]
