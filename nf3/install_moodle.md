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

Moodle ens avisa de que hem d'instal·lar els mòduls de PHP anomenats php-curl i php-zip i uns quants que ens demanarà més endavant.

![image](https://github.com/user-attachments/assets/ac532708-4133-4bfa-89c0-52ccead55b20)

```
sudo apt install php-curl php-zip php-xml php-mysqli php-mbstring
sudo service apache2 restart
```

![image](https://github.com/user-attachments/assets/7c8bfb22-c4bf-4a5d-8220-33506844ffeb)
![image](https://github.com/user-attachments/assets/1c8e72cc-9ca7-4274-9886-3b075ff2ccf6)

Seleccionem el controlador per la BBDD

![image](https://github.com/user-attachments/assets/feee9f9e-7414-498f-b883-42a6e3626008)

![image](https://github.com/user-attachments/assets/afb662eb-6aaf-4527-b9b6-8f1a89757370)

![image](https://github.com/user-attachments/assets/c1084b4d-79d1-4539-896f-dd121d843fc5)

Moodle ens diu que falten mòduls per instal·lar de PHP

```
sudo apt install php-soap php-gd php-intl
sudo service apache2 restart
```

Hem de modificar un fitxer de configuració:

![image](https://github.com/user-attachments/assets/1218b224-d398-47ce-98a5-c8634b155824)

![image](https://github.com/user-attachments/assets/7b79854e-7dd7-418f-8317-abd812a8779e)

![image](https://github.com/user-attachments/assets/c74da37d-10fd-4b4d-b868-ca7d499652f7)

Reiniciem Apache i recarguem la web.

## Resetejar password ususari Moodle:

![image](https://github.com/user-attachments/assets/89114281-94fd-488c-9139-ae2730ed5500)

## Vídeo tutorial Moodle:

[https://youtu.be/sKhYV19Rgw0](https://youtu.be/sKhYV19Rgw0)

Al tutorial falta la part d'editar el fitxer php.ini:

![image](https://github.com/user-attachments/assets/9915c55b-0ad1-4188-8ee3-966d83562409)
![image](https://github.com/user-attachments/assets/44eb1c2e-7b38-4166-81ed-4121435cbab9)
![image](https://github.com/user-attachments/assets/941c8aa4-e1da-4f0c-962a-45f7b1ea132f)


