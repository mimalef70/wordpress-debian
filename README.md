# wordpress-debian


# Update Debian
apt-get update
apt-get upgrade
apt-get dist-upgrade

# Install MariaDB (https://www.digitalocean.com/community/tutorials/how-to-install-mariadb-on-debian-9)
apt install mariadb-server
mysql_secure_installation

# Set Password For root user on MariaDB
mysql
MariaDB [(none)]> GRANT ALL ON *.* TO 'root'@'localhost' IDENTIFIED BY 'password' WITH GRANT OPTION;
MariaDB [(none)]> FLUSH PRIVILEGES;
MariaDB [(none)]> exit

# Install Nginx
apt-get install nginx

# Install PHP
apt-get install curl php-fpm php7.2-common php-cli php-curl php-gd php-mcrypt php-xml php-mbstring php-soap php-intl php-mysql php-zip php-xmlrpc php-ldap

# Install WP-CLI From (https://wp-cli.org/)

------

#install MYSQL8

wget -c https://dev.mysql.com/get/mysql-apt-config_0.8.10-1_all.deb
apt install lsb-release
dpkg -i mysql-apt-config_0.8.10-1_all.deb
apt-get update
apt-get install mysql-server


#install PHP 7.2

wget -q https://packages.sury.org/php/apt.gpg -O- | sudo apt-key add -
echo "deb https://packages.sury.org/php/ stretch main" | tee /etc/apt/sources.list.d/php.list
apt-get install ca-certificates apt-transport-https
apt-get update
apt-get -y install php7.2
apt-get purge apache2
apt-get install nginx
apt-get install -y tmux curl wget php7.2-fpm php7.2-cli php7.2-curl php7.2-gd php7.2-intl 
apt-get install -y php7.2-mysql php7.2-mbstring php7.2-zip php7.2-xml php7.2-ldap php7.2-xmlrpc php7.2-soap php7.2-common unzip

#Install NGINX

wget https://nginx.org/keys/nginx_signing.key
apt-key add nginx_signing.key
nano /etc/apt/sources.list
add = > 
deb https://nginx.org/packages/debian/ stretch nginx
deb-src https://nginx.org/packages/debian/ stretch nginx
apt-get remove nginx-common
apt-get update
apt-get install nginx

#install wp
CREATE DATABASE your_domain DEFAULT CHARACTER SET utf8 COLLATE utf8_unicode_ci;
GRANT ALL ON your_domain.* TO 'wordpressuser'@'localhost' IDENTIFIED BY 'password';
FLUSH PRIVILEGES;
EXIT;




