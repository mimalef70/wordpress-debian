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

# Install Nginx
apt-get install nginx

# Install PHP
apt-get install curl php-fpm php-common php-cli php-curl php-gd php-mcrypt php-xml php-mbstring php-soap php-intl php-mysql php-zip php-xmlrpc php-ldap

# Install WP-CLI From (https://wp-cli.org/)

