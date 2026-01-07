# Tutorial install Mariadb
MariaDB adalah fork dari MySQL yang bersifat open source dan kompatibel penuh. Di Arch Linux, paket resminya bernama mariadb, dan tersedia langsung di repositori resmi, jadi tidak perlu dari AUR. Tapi kalau kamu ingin menggunakan versi dari AUR (misalnya versi tertentu atau yang dikompilasi dengan opsi khusus), kamu bisa pakai mariadb dari AUR juga.

## 📦 1. Instal MariaDB
`sudo pacman -Syu mariadb`
jika sudah ter instal tahap selanjutnya ialah mengintal dat base

## ⚙️ 2. Inisialisasi Database
`sudo mariadb-install-db --user=mysql --basedir=/usr --datadir=/var/lib/mysql`

## 🔥 3. Menjalankan MariaDB
tahap selanjut nya yakni menjalankan mariadb
`sudo systemctl enable mariadb`

mulai layana mariadb `sudo systemctl start mariadb`
untuk mngecek status mariadb kalian biasa mnggunakan 
`sudo systemctl status mariadb`
dan untuk menggunakan mariadb cukup ketik `mariadb`

di tahap ini mariadb sudah bisa di gunakan  tapi untu keamanan mariadb menyediakan kongfigurasi keamanan

## 🔒 4. Konfigurasi Keamanan Awal
MariaDB menyediakan skrip untuk menghapus pengguna dan database default yang tidak aman 
`sudo mysql_secure_installation`
Selama proses ini, kamu akan diminta untuk: dan kalian hanya tinggal ikuti instrusi di terminal


### Mengatur password root (jika belum ada)
#### Menghapus user anonim
### Menonaktifkan login root dari remote
### Menghapus test database
### Reload privilege tables





