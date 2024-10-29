# Instal·lar Moodle

## Instal·lar LAMP (Linux, Apache, MariaDB, PHP)

### Actualitzem els repositoris de software de Linux

```
sudo apt update
```

### Instal·lem Apache

```
sudo apt install apache2
```

### Instal·lem MariaDB

```
sudo apt install mariadb-server
```

### Instal·lem PHP

```
sudo apt install php
```

## Descarregar Moodle

```
wget https://download.moodle.org/download.php/direct/stable405/moodle-latest-405.zip
```

## Descomprimir Moodle a un directori accessible pel server

```
sudo unzip moodle-latest-405.zip -d /var/www/html
```

## Canviem el propietari del directori de Moodle per a que Apache pugui accedir

``` 
sudo chown www-data:www-data -r /var/www/html/moodle
```

![image](https://github.com/user-attachments/assets/3359b833-b0cd-49f3-9452-e71aacb43193)

## Creem un directori de dades

```
cd /home
sudo mkdir moodle_data
sudo chown www-data:www-data moodle_data/
```

## Configurem la base de dades

![image](https://github.com/user-attachments/assets/3ad3d846-5300-4556-8c28-d9783e3a2131)

## Configurar Moodle

Obrim un navegador i escrivim **localhost/moodle**.

![image](https://github.com/user-attachments/assets/b211a05d-a23a-4f98-94e0-a01acc4cae62)

Moodle ens avisa de que hem d'instal·lar els mòduls de PHP anomenats php-curl i php-zip.

![image](https://github.com/user-attachments/assets/ac532708-4133-4bfa-89c0-52ccead55b20)

```
sudo apt install php-curl php-zip
sudo service apache2 restart
```

![image](https://github.com/user-attachments/assets/7c8bfb22-c4bf-4a5d-8220-33506844ffeb)
![image](https://github.com/user-attachments/assets/1c8e72cc-9ca7-4274-9886-3b075ff2ccf6)

Seleccionem el controlador per la BBDD

![image](https://github.com/user-attachments/assets/feee9f9e-7414-498f-b883-42a6e3626008)

![image](https://github.com/user-attachments/assets/afb662eb-6aaf-4527-b9b6-8f1a89757370)




