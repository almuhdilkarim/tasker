# tutorial instalasi mariadb di arch

## install packages mariadb
```
sudo pacman -S mariadb
```
## konfigurasi
```
mariadb-install-db --user=mysql --basedir=/usr --datadir=/var/lib/mysql
```

## menjalankan mariadb sebagai server
```
[mysql]$ mariadb
```

atau jika sebagai root atau administrator
```
mariadb
```

## membuat user
```
mariadb -u root -p
```

```
MariaDB> CREATE USER 'monty'@'localhost' IDENTIFIED BY 'some_pass';
```

```
MariaDB> GRANT ALL PRIVILEGES ON mydb.* TO 'monty'@'localhost';
```

```
MariaDB> quit
```
