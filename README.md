Wordpress for ADM
=================

This wordpress fork is dedicated for the Phonations website:
http://www.phonations.com

Installation
------------

    sudo apt-get install apache2 php5 mysql-server libapache2-mod-php5 php5-mysql

    git clone https://github.com/atelierdesmedias/WordPress adm
    cd adm
    git submodule init
    git submodule update


    <VirtualHost *:80>
      ServerName www.phonations.com

      ServerAdmin martin@phonations.com

      DocumentRoot /var/www/phonations/
      <Directory /var/www/phonations>
        Options Indexes FollowSymLinks MultiViews
        AllowOverride All
        Order allow,deny
        allow from all
      </Directory>

      ErrorLog /var/log/apache2/file.log
      CustomLog /var/log/apache2/file.log combined

      RewriteEngine On
    </VirtualHost>

