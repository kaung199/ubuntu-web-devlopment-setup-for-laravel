
## Remark
> install apache, mysql, php7.4, composer


## Update the package
> sudo apt update

> sudo apt upgrade

## 1. Installing Apache
> sudo apt install apache2

**Check currently available UFW application profiles and open port**
> sudo ufw app list

> sudo ufw allow in "Apache Full"

## 2. Installing MySQL
> sudo apt install mysql-server

> sudo systemctl start mysql.service

**Configuring MySQL**
> sudo mysql

> ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';

**Login MySQL with new password**
> mysql -u root -p

>exit

**connect to MySQL as your root user**
> ALTER USER 'root'@'localhost' IDENTIFIED WITH auth_socket;

## 3. Installing PHP 7.4
> sudo apt install php7.4 libapache2-mod-php7.4 php7.4-mysql

**Check PHP Version**
> php -v

**Install php 7.4 extension**
> sudo apt-get install -y php7.4-cli php7.4-json php7.4-common php7.4-mysql php7.4-zip php7.4-gd php7.4-mbstring php7.4-curl php7.4-xml php7.4-bcmath

## 4. Installing Composer
> sudo apt install php7.4-cli unzip

> cd ~

**Install CURL**
> sudo apt install curl

**Download and Install Composer**
> curl -sS https://getcomposer.org/installer -o /tmp/composer-setup.php

> HASH=`curl -sS https://composer.github.io/installer.sig`

> php -r "if (hash_file('SHA384', '/tmp/composer-setup.php') === '$HASH') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"

> sudo php /tmp/composer-setup.php --install-dir=/usr/local/bin --filename=composer

> composer

**you cand downgrade and upgrade with flowing command**
> composer self-update --1

> composer self-update --2

> composer self-update 1.10.12

> composer self-update 2.0.7

> composer self-update

> composer self-update rollback



