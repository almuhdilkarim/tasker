## Konsep Database dan Tabel
### Definisi Database
Database adalah kumpulan data yang terorganisasi dan dikelola secara sistematis. Berbeda dengan file biasa, database memiliki struktur yang memungkinkan data dapat diakses, diperbarui, dan dianalisis dengan lebih mudah. Dalam konteks perpustakaan, database menyimpan data anggota, koleksi buku, serta transaksi peminjaman. Semua informasi ini saling terhubung sehingga menciptakan sistem yang terpadu. Tanpa database, pengelolaan data berskala besar akan sulit dilakukan.

### Pengertian Tabel
Tabel adalah struktur dasar dalam database relasional. Data disimpan dalam bentuk baris dan kolom dengan aturan tertentu. Setiap tabel biasanya merepresentasikan satu entitas dunia nyata. Misalnya, tabel anggota merepresentasikan semua pengguna perpustakaan. Tabel memberikan kerangka teratur untuk pengelolaan data.

### Baris Sebagai Record Data
Baris dalam tabel disebut record, yaitu kumpulan informasi tentang satu entitas. Dalam tabel anggota, satu baris berisi nama, alamat, dan nomor telepon seorang anggota. Baris ini unik karena memiliki ID khusus. ID tersebut membedakan satu anggota dari yang lain. Setiap baris adalah representasi digital dari entitas nyata.

Baris memberikan granularitas data yang sangat penting. Misalnya, perpustakaan dapat menelusuri riwayat peminjaman seorang anggota berdasarkan baris transaksi. Tanpa baris, data akan bercampur dan sulit dianalisis. Baris memastikan informasi tetap terstruktur. Hal ini membuat database lebih berguna dalam praktik sehari-hari.

### Kolom sebagai Atribut Data
Kolom dalam tabel menyimpan atribut spesifik dari entitas. Misalnya, kolom “nama” menyimpan nama anggota, sementara kolom “alamat” menyimpan alamat anggota. Setiap kolom memiliki tipe data tertentu yang sesuai dengan informasi yang disimpan. Hal ini menjaga konsistensi dan keakuratan data. Kolom adalah penjelas detail dari entitas.

Kolom membantu dalam pemisahan informasi yang berbeda. Dengan pemisahan, data lebih mudah dianalisis dan diproses. Kolom juga memungkinkan validasi data secara otomatis. Misalnya, kolom tahun terbit hanya menerima tipe data YEAR. Jika ada data tidak sesuai, sistem akan menolak input tersebut.

Selain itu, kolom mempermudah pengembangan laporan. Perpustakaan bisa menampilkan daftar buku berdasarkan penulis hanya dengan mengambil kolom yang relevan. Data yang terpisah dalam kolom memberikan fleksibilitas tinggi. Inilah yang menjadikan kolom sebagai elemen fundamental dalam tabel. Database tanpa kolom tidak akan terstruktur dengan baik.

### Relasi Antar Tabel
Relasi antar tabel adalah keunggulan utama database relasional. Relasi memungkinkan data dari tabel berbeda saling terhubung. Misalnya, tabel peminjaman menghubungkan tabel anggota dengan tabel buku. Dengan cara ini, sistem dapat mengetahui siapa meminjam buku tertentu. Relasi memberikan gambaran utuh tentang data.

Relasi biasanya diwujudkan melalui penggunaan foreign key. Foreign key adalah kolom dalam suatu tabel yang merujuk ke primary key tabel lain. Misalnya, `id_anggota` dalam tabel peminjaman merujuk ke tabel anggota. Relasi ini memastikan integritas antar data. Tanpa relasi, data akan terisolasi dan sulit digabungkan.

Relasi juga mendukung analisis yang lebih kompleks. Perpustakaan bisa mengetahui jumlah peminjaman per anggota dengan menggabungkan tabel anggota dan peminjaman.

Selain itu, relasi meningkatkan efisiensi pengelolaan data. Informasi anggota hanya dicatat sekali di tabel anggota. Tabel peminjaman cukup merujuk ke ID anggota. Hal ini mengurangi redundansi dan menjaga konsistensi.

### Peran Primary Key
Primary key adalah pengenal unik untuk setiap baris dalam tabel. Tanpa primary key, data bisa duplikat dan sulit dibedakan. Misalnya, dua anggota dengan nama sama dapat dibedakan melalui ID unik. Primary key menjamin keunikan dan konsistensi data. Database modern selalu membutuhkan primary key.

Primary key biasanya berupa angka yang bertambah otomatis. Dalam tabel anggota, kolom `id_anggota` menjadi primary key. Sistem akan otomatis menambahkan nilai baru setiap kali ada anggota baru. Hal ini mencegah duplikasi yang tidak diinginkan. Primary key adalah fondasi integritas data.primary key juga mempermudah pembuatan relasi. Tabel peminjaman bisa merujuk ke primary key tabel anggota. Dengan cara ini, data antar tabel saling terhubung. Primary key juga mempermudah proses pencarian data. Sistem dapat langsung mencari data berdasarkan ID unik. Hal ini jauh lebih cepat dibanding mencari berdasarkan nama atau atribut lain.

### Kolaborasi Database, Tabel, Baris, dan Kolom
Database, tabel, baris, dan kolom adalah komponen yang saling melengkapi. Database menjadi wadah utama, tabel sebagai struktur, baris sebagai entitas, dan kolom sebagai atribut. Semua elemen ini bekerja sama untuk menyusun sistem informasi. Tanpa salah satunya, database tidak dapat berfungsi optimal. Konsep ini mencerminkan integrasi.

Kolaborasi ini juga memudahkan analisis data. Misalnya, laporan bulanan dapat dibuat dengan menggabungkan tabel peminjaman dan buku. Setiap baris dan kolom memberikan informasi yang berbeda. Database memungkinkan penggabungan ini dengan efisien. Sistem manual tidak mampu memberikan hasil secepat itu.

Selain itu, kolaborasi ini meningkatkan akurasi dan transparansi. Semua data tersimpan dalam struktur yang jelas. Sehingga Relasi antar tabel memastikan informasi tetap konsisten. 

## Tipe Data Sederhana
### Definisi Tipe Data
Tipe data adalah aturan yang menentukan bentuk dan sifat data yang disimpan dalam kolom tabel. Dengan tipe data, sistem database dapat membedakan antara angka, teks, tanggal, atau format lain. Dalam MariaDB, pemilihan tipe data sangat penting untuk menjaga keakuratan dan konsistensi. Misalnya, kolom nomor telepon harus disimpan dalam teks, bukan angka. Tipe data membantu sistem mengenali batasan setiap informasi.

### Tipe Data Angka (Numeric)
Tipe data angka digunakan untuk menyimpan bilangan bulat maupun desimal. Dalam MariaDB, tipe angka sederhana mencakup INT, BIGINT, dan DECIMAL. 
* INT digunakan untuk angka bulat
* DECIMAL untuk angka dengan koma.
Dalam perpustakaan, tipe data angka banyak digunakan. ID anggota biasanya menggunakan tipe INT dengan AUTO_INCREMENT. Tahun terbit buku bisa disimpan menggunakan YEAR, yang juga termasuk kategori angka. Dengan angka, database dapat melakukan operasi perhitungan. Misalnya, menghitung total buku yang tersedia.

### Tipe Data Teks (String)
Tipe data teks digunakan untuk menyimpan karakter, kata, atau kalimat. Dalam MariaDB, tipe teks umum adalah CHAR dan VARCHAR. 
* CHAR digunakan untuk data dengan panjang tetap,
* sedangkan VARCHAR untuk panjang bervariasi.
Misalnya, nama anggota lebih cocok menggunakan VARCHAR(100). Dengan tipe ini, teks disimpan secara fleksibel.

Namun, penggunaan teks harus disesuaikan dengan kebutuhan. Jangan memberikan panjang kolom terlalu besar karena boros penyimpanan. Sebaliknya, panjang terlalu kecil bisa memotong data. Dalam desain tabel, pemilihan panjang VARCHAR harus proporsional.

### Tipe Data Tanggal dan Waktu
Tipe data tanggal menyimpan informasi waktu dalam format khusus. MariaDB menyediakan tipe DATE, TIME, DATETIME, dan TIMESTAMP.
* DATE menyimpan tanggal
* TIME menyimpan jam
* dan DATETIME menyimpan keduanya.
Dengan format ini, sistem dapat mengolah data kronologis. Selain itu, MariaDB memungkinkan perbandingan waktu. Query dapat mencari semua transaksi setelah tanggal tertentu. Dengan cara ini, data bisa difilter sesuai kebutuhan.

### Pentingnya Pemilihan Tipe Data
Pemilihan tipe data yang tepat sangat memengaruhi kualitas database. Tipe data menentukan validitas, efisiensi, dan kecepatan akses. Jika salah memilih, data bisa tidak konsisten atau boros penyimpanan. Misalnya, menyimpan nomor telepon dengan tipe INT akan salah karena bisa mengabaikan angka nol di depan. Oleh karena itu, pemilihan harus hati-hati.

Selain itu, tipe data berperan dalam validasi input. Database akan menolak data yang tidak sesuai tipe. Hal ini mencegah kesalahan manusia saat menginput data. Validasi otomatis ini meningkatkan kualitas informasi. Dengan demikian, tipe data menjadi alat penjaga integritas. Sehingga Keputusan pemilihan tipe data harus dipertimbangkan sejak awal desain. Perubahan setelah tabel berisi data bisa sulit dilakukan.

### Konsekuensi Kesalahan Tipe Data
Kesalahan dalam memilih tipe data bisa berakibat fatal. Misalnya :
* mengurangi kegunaan database.
* Kesalahan tipe data merusak analisis.
* membingungkan pengguna
* menyebabkan pemborosan
* Efisiensi dan akurasi hilang karena kesalahan desain
* Kesalahan juga berdampak pada integrasi sistem.

## Membuat DataBase
### Persiapan
* pastikan MariaDB sudah berjalan di komputer Anda.
Bukalah terminal atau command prompt lalu login dengan akun root menggunakan perintah `mysql -u root -p`. Khusus pengguna archlinux, jika sudah selesai meng-install MariaDB di Arch Linux, langkah penting berikutnya adalah menginisialisasi database system. Inilah yang dilakukan dengan perintah: `mariadb-install-db --user=mysql --basedir=/usr --datadir=/var/lib/mysql`
* cek apakah MariaDB service aktif. Di Linux, Anda bisa menggunakan `systemctl status mariadb` untuk memastikannya. Jika layanan mati, hidupkan dengan `systemctl start mariadb`.
* Setelah login, mari kita buat database baru. Database ini akan menjadi rumah bagi tabel-tabel perpustakaan. Gunakan perintah:
```
CREATE DATABASE perpustakaan;
```
atau
```
CREATE DATABASE perpus
DEFAULT CHARACTER SET utf8mb4
COLLATE utf8mb4_general_ci;
```
Dengan perintah ini, MariaDB akan membuat database kosong bernama perpustakaan. Database ini belum memiliki tabel, tetapi sudah siap menampung data. Setelah membuat database, jangan lupa untuk memilihnya dengan perintah:
```
USE perpustakaan;
```
* Verifikasi
Setelah membuat database, mari pastikan database sudah ada. Gunakan perintah:
```
SHOW DATABASES;
```
Selain itu, Anda juga bisa memeriksa database aktif dengan:
```
SELECT DATABASE();
```
### Kesalahan Umum
1. Lupa memilih database dengan `USE`. Akibatnya, tabel yang dibuat tidak tersimpan di tempat yang benar.
2. membuat database dengan nama yang sudah ada. MariaDB akan menolak perintah tersebut. Untuk menghindarinya, gunakan `CREATE DATABASE IF NOT EXISTS perpustakaan;`.
3. tidak memperhatikan karakter set. Akibatnya, data teks bisa rusak saat menyimpan karakter khusus. Perpustakaan yang menyimpan judul asing bisa terganggu. Solusi terbaik adalah selalu menggunakan UTF-8.
4. salah ketik nama database. Misalnya, menulis perpustakan tanpa huruf “a”. Kesalahan kecil bisa membuat data tersimpan di tempat yang berbeda. Oleh karena itu, ketelitian sangat penting. Biasakan memeriksa nama database dengan teliti.

## Membuat Table
### Perintah Dasar
Perintah `CREATE TABLE` digunakan untuk membuat struktur penyimpanan data. Struktur tabel terdiri dari kolom yang merepresentasikan atribut dan baris untuk entitas. Contoh sederhana adalah pembuatan tabel anggota:
```
CREATE TABLE anggota (
    id_anggota INT PRIMARY KEY AUTO_INCREMENT,
    nama VARCHAR(100),
    alamat VARCHAR(150),
    no_telepon VARCHAR(20)
);
```
Dengan perintah ini, sistem membuat tabel kosong bernama anggota. Tabel sudah siap menampung data baru. Struktur ini akan menjadi kerangka utama dalam manajemen keanggotaan. Setiap kolom harus dipilih tipe data yang sesuai. `id_anggota` menggunakan INT dengan AUTO_INCREMENT agar setiap baris unik. Kolom nama dan alamat menggunakan VARCHAR untuk fleksibilitas teks. Sementara nomor telepon disimpan sebagai VARCHAR agar tidak kehilangan angka nol di depan. Pemilihan ini menegaskan pentingnya tipe data.

### Membuat Table Buku
Tabel buku dirancang untuk menyimpan informasi koleksi perpustakaan. Kolom yang dipakai mencakup ID, judul, penulis, tahun terbit, dan ISBN. ID buku menjadi primary key agar setiap koleksi unik. ISBN diberi constraint UNIQUE untuk mencegah duplikasi. Struktur ini menjaga keakuratan data.

Contoh struktur tabel buku adalah:
```
CREATE TABLE buku (
    id_buku INT PRIMARY KEY AUTO_INCREMENT,
    judul VARCHAR(150) NOT NULL,
    penulis VARCHAR(100),
    tahun_terbit YEAR,
    isbn VARCHAR(20) UNIQUE
);
```
Judul buku diberi constraint NOT NULL karena setiap koleksi harus memiliki nama. Penulis dan tahun terbit memberikan detail tambahan. ISBN mempermudah integrasi dengan katalog internasional. Struktur ini sudah cukup untuk koleksi dasar. Dengan tabel ini, perpustakaan dapat melacak semua buku yang dimiliki. Setiap koleksi tercatat dengan jelas dan bisa dicari dengan cepat. Data ini juga memudahkan pembuatan laporan jumlah koleksi.

### Kesalahan Umum
1. Lupa Menggunakan `USE`.
   Kesalahan pertama adalah lupa menggunakan perintah `USE` sebelum membuat tabel. Akibatnya, tabel tersimpan di database yang salah. Hal ini menimbulkan kebingungan saat mengelola data. Kesalahan ini mudah dicegah dengan kebiasaan memeriksa database aktif.
2. Tidak Menentukan Primary Key
Kesalahan kedua adalah tidak menentukan primary key. Tanpa primary key, data duplikat mudah terjadi. Dalam tabel anggota, dua orang bisa memiliki data identik tanpa cara membedakan. Hal ini merusak integritas sistem. Primary key selalu wajib.
3. Salah Memilih Tipe Data
Kesalahan ketiga adalah salah memilih tipe data. Nomor telepon misalnya sering disimpan sebagai INT. Akibatnya angka nol di awal hilang. Data menjadi tidak valid. Pemilihan tipe VARCHAR lebih sesuai.
4. Panjang Kolom Tidak Memadai
Kesalahan keempat adalah kolom dengan panjang tidak memadai. Judul buku panjang bisa terpotong jika VARCHAR terlalu kecil. Informasi menjadi tidak lengkap. Panjang kolom harus mempertimbangkan variasi data yang realistis.

### Best Practice
1. Menentukan Primary Key dengan AUTO_INCREMENT
2. Pemilihan Tipe Data yang Tepat
3. Penggunaan Constraint NOT NULL dan UNIQUE
4. Dokumentasi Struktur Tabel

### Menambahkan Table Buku
```
CREATE TABLE buku (
    id_buku INT PRIMARY KEY AUTO_INCREMENT,
    judul VARCHAR(150) NOT NULL,
    penulis VARCHAR(100),
    tahun_terbit YEAR,
    isbn VARCHAR(20) UNIQUE
);
```
Setelah tabel dibuat, data dapat dimasukkan menggunakan perintah `INSERT`. Berikut adalah contoh menambahkan tiga buku:
```
INSERT INTO buku (judul, penulis, tahun_terbit, isbn) VALUES
('Dasar-Dasar Basis Data', 'Ani Rahmawati', 2020, '9786021112223'),
('Pemrograman SQL untuk Pemula', 'Dedi Kurniawan', 2018, '9786023344556'),
('Manajemen Perpustakaan Digital', 'Rina Sari', 2022, '9786029988775');
```
Data yang sudah dimasukkan dapat diperiksa dengan perintah:
```
SELECT * FROM buku;
```

### kesalahan Umum
1. Tidak Menentukan Constraint NOT NULL
Kesalahan pertama adalah tidak memberikan constraint NOT NULL pada kolom judul. Tanpa aturan ini, buku dapat tercatat tanpa nama. Hal ini akan menyulitkan identifikasi koleksi.
2. ISBN Tidak Diberi UNIQUE
Kesalahan kedua adalah tidak memberikan constraint UNIQUE pada ISBN. Akibatnya, buku dengan ISBN sama bisa tercatat berulang. Hal ini akan menyebabkan kebingungan saat pencarian. ISBN harus unik agar koleksi valid.
3. Tahun Terbit Salah Tipe Data
Kesalahan ketiga adalah menggunakan VARCHAR untuk menyimpan tahun terbit. Data akan tersimpan, tetapi tidak bisa dibandingkan secara numerik. Query seperti pencarian buku setelah tahun tertentu akan gagal. Tipe YEAR adalah pilihan terbaik.
4. Panjang Kolom Judul Tidak Sesuai
Kesalahan keempat adalah menetapkan panjang VARCHAR terlalu pendek. Judul panjang akan terpotong dan kehilangan informasi. Database harus mempertimbangkan variasi data nyata. Panjang kolom harus cukup fleksibel.

### Best Practice
1. Gunakan Primary Key dengan AUTO_INCREMENT
Primary key dengan AUTO_INCREMENT menjamin keunikan setiap baris. Database mengelola ID secara otomatis sehingga admin tidak perlu menginput manual. Hal ini mencegah terjadinya duplikasi data. Struktur tabel menjadi lebih aman dan konsisten.
2. Gunakan Constraint untuk Menjaga Integritas
Constraint seperti NOT NULL dan UNIQUE menjaga validitas data. Judul tidak boleh kosong dan ISBN harus unik. Dengan aturan ini, database menolak input yang salah. Integritas data tetap terjaga sepanjang waktu.
3. Pilih Tipe Data yang Tepat
Pemilihan tipe data harus sesuai dengan karakteristik informasi. YEAR digunakan untuk tahun, VARCHAR untuk teks, dan INT untuk angka. Dengan tipe data yang benar, query dapat dijalankan lebih efisien. Penyimpanan juga lebih hemat.
4. Dokumentasikan Struktur Tabel
Dokumentasi desain tabel membantu kolaborasi dan pemeliharaan jangka panjang. Setiap kolom, constraint, dan tipe data harus dicatat. Walaupun tidak berupa kode SQL, dokumentasi ini sangat penting. Dengan dokumentasi, perubahan di masa depan lebih mudah dilakukan.
