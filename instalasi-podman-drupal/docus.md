---

# Bagian 1 — Install Podman di Debian

### 1. Update sistem

```
sudo apt update && sudo apt upgrade -y
```

### 2. Install Podman

Pada Debian 12:

```
sudo apt install podman -y
```

Pada Debian 11 (Bullseye, versi default agak lama), gunakan backports:

```
echo "deb http://deb.debian.org/debian bullseye-backports main" | sudo tee /etc/apt/sources.list.d/backports.list
sudo apt update
sudo apt -t bullseye-backports install podman -y
```

### 3. Cek versi

```
podman --version
```


---

# Bagian 2 — Install Drupal Menggunakan Podman (Debian)

Struktur:

* Drupal (PHP + Apache)
* MariaDB (database)

---

## Langkah 1 — Buat Podman Network

```
podman network create drupal-net
```

---

## Langkah 2 — Jalankan MariaDB

```
podman run -d --name drupal-db \
  --network drupal-net \
  -e MYSQL_DATABASE=drupal \
  -e MYSQL_USER=drupal \
  -e MYSQL_PASSWORD=drupalpass \
  -e MYSQL_ROOT_PASSWORD=rootpass \
  -v drupal-db-data:/var/lib/mysql \
  docker.io/library/mariadb:latest
```

Cek apakah database berjalan:

```bash
podman ps
```

---

## Langkah 3 — Jalankan Drupal

```
podman run -d --name drupal \
  --network drupal-net \
  -p 8080:80 \
  -e DRUPAL_DB_HOST=drupal-db \
  -e DRUPAL_DB_NAME=drupal \
  -e DRUPAL_DB_USER=drupal \
  -e DRUPAL_DB_PASSWORD=drupalpass \
  docker.io/library/drupal:latest
```

---

## Langkah 4 — Akses Drupal

Buka browser:

```
http://localhost:8080
```
Masukkan database:

* Database name: drupal
* Username: drupal
* Password: drupalpass
* Host: drupal-db