# Install MongoDB di Arch Linux & Penggunaan Dasarnya (Step-by-Step)

Ringkasan: MongoDB dikeluarkan dari repos resmi Arch karena lisensi. instalasi umum di Arch dilakukan lewat AUR, bisa membangun dari source atau memakai paket prebuilt (`mongodb-bin`). kalo untuk shell, bisa pakai `mongosh` (bukan `mongo`).

## Prasyarat

1. Koneksi ke jaringan internet.  
2. Akun dengan hak `sudo`.  
3. Sistem ter update `sudo pacman -Syu`.

# Install Yay

1. `git clone https://aur.archlinux.org/yay.git`
2. `cd yay`
3. `makepkg -si`

# Install MongoDB

`yay -S mongodb-bin`

# Install MongoCompass (Opsional)

`yay -S mongosh-bin mongodb-tools-bin mongodb-compass`

# Pastikan Direktorinya ada dan benar kepemilikannya

1. `sudo mkdir -p /var/lib/mongodb /var/log/mongodb`
2. `sudo chown -R mongodb:mongodb /var/lib/mongodb /var/log/mongodb`
3. `sudo chmod 700 /var/lib/mongodb`

# Baru jalankan Service MongoDB nya

1. `sudo systemctl enable --now mongodb`
2. `sudo systemctl status mongodb`

# Verifikasi MongoDB dan untuk masuk ke Shell MongoDB

1. `mongosh`
2. `show dbs` 
(untuk melihat daftar Database apa saja yang telah ada)
3. `use nama_database` 
(Untuk menggunakan Database yang dinginkan)
4. `show collections` 
(Untuk melihat ada koleksi apa saja pada Databse yang telah digunakan)

# Contoh Membuat User Admin

1. `use admin` 
(Menggunakan/Membuat Database)
2. `db.createUser({user: "admin", pwd: "password_kuat", roles: [{ role: "userAdminAnyDatabase", db: "admin" }"readWriteAnyDatabase"]})` (Membuat Koleksi dalam Database tersebut) 
3. `mongosh -u admin -p --authenticationDatabase admin`

# Test membuat Database baru dan Koleksi didalamnya

1. `use PerpustakaanUINJKT`
2. `db.PerpustakaanUINJKT.insertOne({nama: "Yusuf", umur: 21 })` (Untuk membuat satu entri data didalam sebuah koleksi)
3. `db.PerpustakaanUINJKT.insertMany([{ nama: "Ayu", umur: 20 }, { nama: "Budi", umur: 22 }])` 
(Untuk membuat banyak entri data sekaligus dalam sebuah koleksi)
3. `db.PerpustakaanUINJKT.find()` 
(Untuk melihat daftar koleksi pada Database yang digunakan)

# Menemukan Koleksi didalam Database

1. `db.namaKoleksi.find()` 
(Menampilkan semua data)
2. `db.namaKoleksi.find().pretty()` 
(Menampilkan data secara rapi *tidak diperlukan jika versi MongoDB terbaru)
3. `db.namaKoleksi.find({ umur: 21 })` 
(Filter pencarian koleksi berdasarkan field data)

# Update sebuah koleksi/field

1. `db.namaKoleksi.updateOne({ nama: "Yusuf" },{ $set: { umur: 22 } })`
(Untuk update hanya satu field)

2. `db.namaKoleksi.updateMany({ umur: { $lt: 21 } }, { $set: { status: "mahasiswa baru" }})`
(Untuk update banyak filed sekaligus)

# Delete/Hapus koleksi

1. `db.namaKoleksi.deleteOne({ nama: "Ayu" })`
(Untuk hapus satu koleksi)
2. `db.namaKoleksi.deleteMany({ umur: { $gt: 25 }})`
(Untuk hapus banyak koleksi sekaligus)

# Command Tambahan 
1. `db.stats()`            (statistik database)
2. `db.serverStatus()`     (status server MongoDB)
3. `db.help()`             (bantuan umum)
4. `db.namaKoleksi.help()` (bantuan khusus koleksi)
