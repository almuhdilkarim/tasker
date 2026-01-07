# Tutorial Install MariaDB di Linux Mint 
## Buka Situs Resmi MariaDB Untuk Melihat Instruksi Peng*install*an
Klik link ini: https://mariadb.com/docs/server/mariadb-quickstart-guides/installing-mariadb-server-guide
<img width="706" height="536" alt="image" src="https://github.com/user-attachments/assets/ef419584-dc03-48b6-933f-6302a86124c4" />

## Step 1: Update Sistem Terlebih Dahulu
Kita harus memastikan bahwa sistem Linux yang kita gunakan sudah yang terbaru. Buka terminal, ketik:

```
sudo apt update
```
```
sudo apt update -y
```
<img width="585" height="211" alt="image" src="https://github.com/user-attachments/assets/9bafed75-8974-4ae3-80dd-4d33e45b7101" />

Command di atas akan mengecek dan upgrade semua package di sistem.Tunggu sebentar sampai prosesnya selesai.
## Step 2: Mulai Install MariaDB
Ketik di terminal:

``` 
sudo apt install mariadb-server mariadb-client -y
```
<img width="770" height="596" alt="image" src="https://github.com/user-attachments/assets/c6895bb1-c2c9-4cc6-8069-7b3ca015fc3b" />

Tunggu sampai prosesnya selesai, dan MariaDB sudah ter-install.
## Step 3: Amankan Instalasi MariaDB
MariaDB yang baru di-install butuh sedikit pengamanan tambahan agar database tidak mudah diakses oleh orang lain. Ketik:
```
sudo mysql_secure_installation
```
<img width="646" height="489" alt="image" src="https://github.com/user-attachments/assets/718fce98-3a0a-4cb0-993a-c1657f0654a6" />

Setelah command di atas dijalankan, akan muncul beberapa pertanyaan. Ikuti panduan berikut:
* Enter current password for root (enter for none): Tekan Enter.
 * Switch to unix_socket authentication? [Y/n]: Pilih n.
 * Set root password? [Y/n]: Pilih Y buat bikin password baru.
 * Remove anonymous users? [Y/n]: Pilih Y.
 * Disallow root login remotely? [Y/n]: Pilih Y.
 * Remove test database and access to it? [Y/n]: Pilih Y.
 * Reload privilege tables now? [Y/n]: Pilih Y.
<img width="404" height="621" alt="image" src="https://github.com/user-attachments/assets/946df04e-e734-4724-95ee-73e65268b029" />

## Step 4: Cek Status MariaDB
Ketik:
```
sudo apt systemctl status mariadb
```
Jika hasilnya menunjukkan active (running), itu artinya MariaDB sudah ter-install dan siap digunakan.
<img width="738" height="98" alt="image" src="https://github.com/user-attachments/assets/353d250a-a758-40e9-9429-0a7adc15a575" />
