# Instal·lació owncloud

## Instal·lació Apache

```
sudo apt update
sudo apt install apache2
```

## Instal·lació MariaDB

```
sudo apt install mariadb-server
```

## Crear BBDD

```
sudo mariadb
```

```
CREATE DATABASE owncloud;
CREATE USER 'ownclouduser'@'localhost' IDENTIFIED BY 'Admin1234';
GRANT ALL ON owncloud.* TO 'ownclouduser'@'localhost' IDENTIFIED BY 'Admin1234' WITH GRANT OPTION;
FLUSH PRIVILEGES
EXIT;
```

## Instal·lar PHP 7.4

```
sudo apt-get install software-properties-common -y
sudo add-apt-repository ppa:ondrej/php
sudo apt update
sudo apt install php7.4 libapache2-mod-php7.4 php7.4-common php7.4-mbstring php7.4-xmlrpc php7.4-soap
sudo apt install php7.4-apcu php7.4-smbclient php7.4-ldap php7.4-redis php7.4-gd php7.4-xml php7.4-intl
sudo apt install php7.4-json php7.4-imagick php7.4-mysql php7.4-cli php7.4-mcrypt php7.4-ldap php7.4-zip php7.4-curl
```

## Editar el fitxer de configuració de PHP 7.4

```
sudo gedit /etc/php/7.4/apache2/php.ini
```

**Canviem els valors**

- file_uploads = On
- allow_url_fopen = On
- memory_limit = 256M
- upload_max_filesize = 100M
- display_errors = Off
- date.timezone = Europe/Madrid

## Instal·lar Owncloud

```
cd /tmp && wget https://download.owncloud.com/server/stable/owncloud-complete-latest.zip
unzip owncloud-complete-latest.zip
sudo mv owncloud /var/www/html/owncloud/
```
## Canviar els permisos del directori d'Owncloud

```
sudo chown -R www-data:www-data /var/www/html/owncloud/
sudo chmod -R 755 /var/www/html/owncloud/
```

## Configurar Apache

```
sudo nano /etc/apache2/sites-available/owncloud.conf
```
Copiem aquest text al fitxer:

https://dungeonofbits.com/images/owncloud1.jpg

