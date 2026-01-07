# Install MariaDB di ArchLinux & Penggunaan Dasarnya (Step-by-Step)

## 1. Instalasi Database MariaDB

### A. Arch Linux (Buka Bash)

# Update Package List

`sudo pacman -Syu`

# Install MariaDB

`sudo pacman -S mariadb`

# Inisialisasi database (wajib pertama kali)

`sudo mariadb-install-db --user=mysql --basedir=/usr --datadir=/var/lib/mysql`

# Jalankan Service

`sudo systemctl start mariadb`

# Diaktifkan agar otomatis saat Boot

`sudo systemctl enable mariadb`

# Cek Status

`systemctl status mariadb`

# Konfigurasi diawal (Untuk Keamanan)

`sudo mysql_secure_installation`

# Cara Masuk ke MariaDB Shell

`mariadb -u root -p` atau `mysql -u root -p`

# Command-command Dasar di MariaDB

1. `SHOW DATABASES; `               -- tampilkan semua database
2. `CREATE DATABASE perpustakaan;`  -- buat database baru
3. `USE perpustakaan;`              -- pilih database
4. `SELECT DATABASE();`             -- cek database aktif
5. `DROP DATABASE perpustakaan;`    -- hapus database

# Cara Membuat Tabel

`CREATE TABLE mahasiswa (id INT AUTO_INCREMENT PRIMARY KEY, nama VARCHAR(50), umur INT);`

`SHOW TABLES;`                   -- tampilkan semua tabel
`DESCRIBE mahasiswa;`            -- lihat struktur tabel
`DROP TABLE mahasiswa;`          -- hapus tabel

# CRUD (Create, Read, User, dan Delete)

1. Insert data
`INSERT INTO mahasiswa (nama, umur) VALUES ("Yusuf", 21);`

2. Read data
`SELECT * FROM mahasiswa;`
`SELECT nama FROM mahasiswa WHERE umur > 20;`

3. Update data
`UPDATE mahasiswa SET umur = 22 WHERE nama = "Yusuf";`

4. Delete data
`DELETE FROM mahasiswa WHERE nama = "Yusuf";`

# User dan Privilege

1. Membuat user baru
`CREATE USER 'admin'@'localhost' IDENTIFIED BY 'passwordkuat';`

2. Beri hak akses
`GRANT ALL PRIVILEGES ON *.* TO 'admin'@'localhost' WITH GRANT OPTION;`

3. Terapkan perubahan
`FLUSH PRIVILEGES;`
