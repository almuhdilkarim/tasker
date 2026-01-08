# Cara Install MariaDB Linux Mint
### 1. Masuk ke mode root dengan syntax berikut lalu masukkan password:
```
sudo su
```

### 2. Ketik syntax berikut untuk update system linux:
```
apt update
```

```
apt upgrade
```
![Dokumentasi 1 Maria DB](https://github.com/user-attachments/assets/e558a50e-2c2a-48ff-88a8-8df3f4f0803c)

### 3. Selanjutnya ketik syntax:
```
apt install mariadb-server
```
![Dokumentasi 2 Maria DB](https://github.com/user-attachments/assets/e8c8946b-dc64-47db-84e5-104091a008cf)

### 4. Ketik "Y" Untuk menyetujui
![Dokumentasi 3 Maria DB](https://github.com/user-attachments/assets/35524fe3-5bd1-457e-8fbf-e80b7e99ea94)

### 5. Lalu Ketik syntax berikut untuk memulai sistem MariaDB:
```
systemctl start mariadb
```
![Dokumentasi 4 Maria DB](https://github.com/user-attachments/assets/fcef6e3e-dd81-4a72-9183-1e2b5fcb69a6)

### 6. Selanjutnya pastikan layanan MariaDB dimulai setiap kali sistem boot dengan syntax:
```
systemctl enable mariadb
```
![Dokumentasi 5 Maria DB](https://github.com/user-attachments/assets/7786182f-5932-4a12-8494-30cafd379330)

### 7. Untuk cek status MariaDB ketik:
```
systemctl status mariadb
```
![Dokumentasi 6 Maria DB](https://github.com/user-attachments/assets/962ab26c-2272-45c2-a93c-555641a79571)

### 8. Untuk meningkatkan keamanan instalasi server pada MariaDB ketik syntax:
```
mysql_secure_installation
```
![Dokumentasi 7 Maria DB](https://github.com/user-attachments/assets/b07ea065-b4af-4252-8089-48e8b61b7ed0)

### 9.Jika terdapat pilihan "Y"/"N", pilih "N" 2x. Terakhir pilih "Y" 4x. MariaDB akhirnya siap dijalankan!
![Dokumentasi 8 Maria DB](https://github.com/user-attachments/assets/9fcd5b8e-f461-4b11-b217-44dcdcded8dc)

![Dokumentasi 9 Maria DB](https://github.com/user-attachments/assets/9ce39ba1-6f63-4f39-90ff-15317db99d7c)
