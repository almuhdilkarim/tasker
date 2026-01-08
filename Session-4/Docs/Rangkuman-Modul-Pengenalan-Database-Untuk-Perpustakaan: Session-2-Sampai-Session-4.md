# Rangkuman Modul Pengenalan Database Untuk Perpustakaan: Session-2 Sampai Session-4
## 1. Modul Session-2: Pengantar
### Part-2: Data
Data adalah representasi fakta, angka, atau simbol yang disimpan dalam bentuk tertentu sehingga dapat diproses menjadi informasi. Dalam konteks sistem informasi, data menjadi pondasi yang memungkinkan organisasi melakukan pencatatan dan analisis. Perpustakaan, misalnya, menyimpan data berupa judul buku, nama penulis, atau tahun terbit yang nantinya digunakan untuk kebutuhan pencarian koleksi. Tanpa data yang terdefinisi, aktivitas peminjaman maupun pengelolaan koleksi akan sulit dilaksanakan.

**Perbedaan Data dan Informasi:**
Data adalah input, sedangkan informasi adalah output setelah dilakukan pemrosesan. Pada perpustakaan, data berupa daftar buku yang dipinjam setiap hari. Namun, jumlah total peminjaman per minggu adalah informasi yang berguna bagi manajemen perpustakaan. 

**Jenis-Jenis Data:**
Menurut Han, Kamber, & Pei (2012), data dapat diklasifikasikan menjadi data terstruktur, semi-terstruktur, dan tidak terstruktur. Data terstruktur adalah data yang disimpan dalam format tabel dengan baris dan kolom jelas, seperti daftar anggota perpustakaan. Semi-terstruktur mencakup data dengan elemen fleksibel seperti JSON atau XML, contohnya metadata katalog buku. Data tidak terstruktur meliputi dokumen teks panjang atau catatan resensi pembaca. Klasifikasi ini memengaruhi cara pengolahan data dalam sistem.

**Kualitas Data:**
Kualitas data menentukan keandalan informasi yang dihasilkan. Dimensi kualitas mencakup akurasi, kelengkapan, konsistensi, dan relevansi. Akurasi berarti data sesuai dengan kondisi sebenarnya. Kelengkapan mencegah kehilangan informasi penting. Konsistensi berarti data disimpan dengan format seragam. Relevansi berarti data sesuai dengan kebutuhan pengguna. 

### Part-3: Database

**Konsistensi dan Integritas Data:**
Konsistensi dan integritas adalah dua aspek penting dalam pengelolaan data. Konsistensi berarti data selalu sesuai dengan aturan yang telah ditentukan. integritas memastikan bahwa hubungan antar data tetap terjaga dengan benar. Kedua aspek ini sulit diwujudkan dalam sistem manual.

Menurut Silberschatz et al. (2020), database memiliki mekanisme untuk menjaga integritas. Salah satunya adalah primary key yang memastikan setiap entitas unik. Dalam perpustakaan, ID anggota mencegah duplikasi data pengguna. Foreign key memastikan bahwa data peminjaman selalu terkait dengan data buku dan anggota. Mekanisme ini menjaga konsistensi yang tidak mungkin dilakukan manual.

**Skalabilitas dan Adaptabilitas:**
Skalabilitas berarti kemampuan sistem menangani pertumbuhan data, sedangkan adaptabilitas adalah kemampuan menyesuaikan dengan kebutuhan baru. Dengan skalabilitas, database tidak hanya relevan untuk saat ini tetapi juga masa depan. Perpustakaan yang berinvestasi dalam database dapat tumbuh tanpa hambatan. Adaptabilitas memastikan sistem selalu sesuai dengan kebutuhan.

### Part-4: DBMS

**Konsep Database Management System (DBMS):**
Database Management System (DBMS) adalah perangkat lunak yang dirancang untuk mengelola data secara sistematis. DBMS memungkinkan penyimpanan, pengolahan, dan pengaksesan data dengan lebih efisien. Dalam perpustakaan, DBMS digunakan untuk mencatat anggota, koleksi buku, dan transaksi peminjaman. Semua data terintegrasi dalam satu sistem yang terstruktur.

DBMS menyediakan mekanisme untuk menjaga integritas data. Misalnya, primary key memastikan bahwa setiap anggota memiliki ID unik. Foreign key menghubungkan data peminjaman dengan anggota dan koleksi buku. 

**Perbedaan Struktural File vs DBMS:**
1. File biasa menyimpan data dalam bentuk datar tanpa relasi. Sebaliknya, DBMS menyimpan data dalam tabel dengan relasi antar entitas. Dalam perpustakaan, file biasa menyimpan data peminjaman dan anggota secara terpisah tanpa keterkaitan. DBMS menghubungkan kedua data melalui foreign key.
2. Struktur DBMS lebih fleksibel. Perubahan atribut dapat dilakukan tanpa mengganggu keseluruhan sistem. Dalam file biasa, menambah kolom baru seringkali memerlukan modifikasi besar.
3. DBMS menggunakan model relasional. Model ini menyederhanakan hubungan antar data dengan konsep tabel. Misalnya, tabel anggota, tabel buku, dan tabel peminjaman dapat saling terhubung. File biasa tidak mampu merepresentasikan hubungan ini secara alami.
4. DBMS mendukung normalisasi data. Normalisasi mengurangi redundansi dan meningkatkan konsistensi. Dalam file biasa, redundansi sulit dihindari karena data disimpan berulang-ulang. 

**Perbedaan Operasional File vs DBMS:**
1. Operasi pada file biasa terbatas pada pembacaan, penulisan, dan pengeditan. DBMS menyediakan operasi lebih canggih melalui SQL. Dengan SQL, pengguna dapat melakukan pencarian kompleks, agregasi, dan analisis.
2. DBMS memiliki transaction management. Fitur ini memastikan bahwa operasi dilakukan secara atomik, konsisten, terisolasi, dan tahan lama (ACID). File biasa tidak memiliki konsep transaksi.
3. DBMS mendukung concurrency control. Banyak pengguna dapat bekerja secara bersamaan tanpa mengganggu data. File biasa tidak mampu mengelola akses simultan.
4. DBMS mendukung backup dan recovery otomatis. File biasa memerlukan salinan manual yang rentan hilang. DBMS memungkinkan pemulihan cepat setelah kegagalan sistem.

### Part-5: MariaDB
MariaDB lahir sebagai turunan dari MySQL. Monty Widenius, salah satu pencipta MySQL, memimpin pengembangan MariaDB. Nama MariaDB diambil dari nama anaknya, Maria.

**Fitur Utama MariaDB:**
1. Dukungan penuh terhadap SQL standar. Dengan SQL, pengguna dapat menulis query universal yang dipahami di banyak DBMS. Dalam perpustakaan, SQL memudahkan pembuatan laporan peminjaman.
2. MariaDB menyediakan engine penyimpanan fleksibel. Engine seperti InnoDB mendukung transaksi dengan jaminan ACID. Dalam perpustakaan, ini memastikan pencatatan peminjaman tetap konsisten. 
3. MariaDB memiliki kemampuan replikasi. Replikasi memungkinkan salinan database di server lain sebagai backup.
4. MariaDB juga mendukung keamanan canggih. Sistem autentikasi, otorisasi, dan enkripsi memperkuat perlindungan data.

**Perbedaan MariaDB dengan MySQL:**
1. MariaDB menawarkan keunggulan biaya karena bersifat open-source. Organisasi tidak perlu membayar lisensi mahal.
2. MariaDB mendukung skalabilitas tinggi. Sistem dapat tumbuh seiring bertambahnya data.
3. MariaDB mudah diintegrasikan dengan aplikasi lain.
4. MariaDB memiliki ekosistem alat pendukung. Alat seperti phpMyAdmin memudahkan administrasi database.

**Peran MariaDB dalam Perpustakaan:**
1. MariaDB membantu perpustakaan mengelola data anggota, koleksi, dan peminjaman.Semua data terintegrasi dalam satu sistem.
2. MariaDB mendukung fungsi transaksi yang sangat penting. Peminjaman dan pengembalian buku dicatat secara konsisten.
3. MariaDB mendukung multiuser access. Banyak staf dapat bekerja secara bersamaan.
4. MariaDB mendukung keamanan data. Informasi anggota perpustakaan harus dijaga kerahasiaannya.

## 2. Modul Session-3: Struktur Database
### Part-1: Tabel

**Definisi Database:**
Database adalah kumpulan data yang terorganisasi dan dikelola secara sistematis. Berbeda dengan file biasa, database memiliki struktur yang memungkinkan data dapat diakses, diperbarui, dan dianalisis dengan lebih mudah.

**Pengertian Tabel:**
Tabel adalah struktur dasar dalam database relasional. Data disimpan dalam bentuk baris dan kolom dengan aturan tertentu. Setiap tabel biasanya merepresentasikan satu entitas dunia nyata. 

**Baris sebagai Record Data:**
Baris dalam tabel disebut record, yaitu kumpulan informasi tentang satu entitas. 
1. Dalam tabel anggota, satu baris berisi nama, alamat, dan nomor telepon seorang anggota. Baris ini unik karena memiliki ID khusus. ID tersebut membedakan satu anggota dari yang lain.
2. Baris memberikan granularitas data yang sangat penting. Perpustakaan dapat menelusuri riwayat peminjaman seorang anggota berdasarkan baris transaksi.
3. Dalam tabel buku, setiap baris merepresentasikan sebuah koleksi. Baris tersebut mencakup judul, penulis, tahun terbit, dan ISBN. Dengan struktur ini, setiap koleksi bisa dikenali dengan jelas.
4. Baris juga memungkinkan analisis yang lebih detail. Perpustakaan bisa menghitung jumlah anggota aktif hanya dengan menghitung jumlah baris pada tabel tertentu.

**Kolom sebagai Atribut Data:**
1. Kolom dalam tabel menyimpan atribut spesifik dari entitas.
2. Kolom membantu dalam pemisahan informasi yang berbeda.
3. Kolom juga memungkinkan validasi data secara otomatis.
4. kolom mempermudah pengembangan laporan.

**Relasi Antar Tabel:**
Relasi antar tabel adalah keunggulan utama database relasional. Relasi memungkinkan data dari tabel berbeda saling terhubung. Relasi biasanya diwujudkan melalui penggunaan foreign key. Foreign key adalah kolom dalam suatu tabel yang merujuk ke primary key tabel lain. Misalnya, ```id_anggota``` dalam tabel peminjaman merujuk ke tabel anggota.

**Peran Primary Key:**
1. Primary key adalah pengenal unik untuk setiap baris dalam tabel. Tanpa primary key, data bisa duplikat dan sulit dibedakan.
2. Primary key biasanya berupa angka yang bertambah otomatis. Dalam tabel anggota, kolom ```id_anggota``` menjadi primary key. Sistem akan otomatis menambahkan nilai baru setiap kali ada anggota baru.
3. Primary key juga mempermudah pembuatan relasi.
4. Primary key juga mempermudah proses pencarian data.

### Part-2: Tipe Data
**Definisi Tipe Data:**
Tipe data adalah aturan yang menentukan bentuk dan sifat data yang disimpan dalam kolom tabel. Dengan tipe data, sistem database dapat membedakan antara angka, teks, tanggal, atau format lain.

**Tipe Data Angka (Numeric):**
Tipe data angka digunakan untuk menyimpan bilangan bulat maupun desimal. Dalam MariaDB, tipe angka sederhana mencakup ```INT```, ```BIGINT```, dan ```DECIMAL```. INT digunakan untuk angka bulat, sementara DECIMAL untuk angka dengan koma. Sedangkan BIGINT untuk angka besar. Dalam perpustakaan, tipe data angka banyak digunakan. ID anggota biasanya menggunakan tipe INT dengan ```AUTO_INCREMENT```.

**Tipe Data Teks (String):**
Tipe data teks digunakan untuk menyimpan karakter, kata, atau kalimat. Dalam MariaDB, tipe teks umum adalah ```CHAR``` dan ```VARCHAR```. CHAR digunakan untuk data dengan panjang tetap, sedangkan VARCHAR untuk panjang bervariasi. 

**Tipe Data Tanggal dan Waktu:**
Tipe data tanggal menyimpan informasi waktu dalam format khusus. MariaDB menyediakan tipe ```DATE```, ```TIME```, ```DATETIME```, dan TIMESTAMP. DATE menyimpan tanggal, TIME menyimpan jam, dan DATETIME menyimpan keduanya.

### Part-3: Membuat Database
**Persiapan:**
Sebelum membuat database, pastikan MariaDB sudah berjalan di komputer Anda. Bukalah terminal atau command prompt lalu login dengan akun root menggunakan perintah:
```
mysql -u root -p.
```
Khusus pengguna archlinux, menggunakan perintah:
```
mariadb-install-db --user=mysql --basedir=/usr --datadir=/var/lib/mysql
```
Di Linux, cara mengecek apakah MariaDB srvice aktif dengan perintah:
```
systemctl status mariadb
```
Jika layanan mati, hidupkan dengan perintah:
```
systemctl start mariadb
```
**Perintah Dasar ```CREATE DATABASE```:**
Setelah masuk ke MariaDB, buat database baru dengan perintah:
```
CREATE DATABASE "nama database"
```
Setelah membuat database, jangan lupa untuk memilihnya dengan perintah:
```
USE "nama database"
```
MariaDB menyediakan beberapa opsi tambahan untuk ```CREATE DATABASE```. Salah satunya adalah menentukan karakter set dengan perintah:
```
DEFAULT CHARACTER SET utf8mb4
```
Perintah ini memastikan teks disimpan dengan format standar yang mendukung banyak bahasa. 

**Verifikasi Database yang Dibuat:**
Setelah membuat database, pastikan database sudah ada. Gunakan perintah:
```
SHOW DATABASES;
```
Selain itu, Anda juga bisa memeriksa database aktif dengan:
```
SELECT DATABASE();
```
Jika membuat database dengan nama yang sudah ada. MariaDB akan menolak perintah tersebut. Untuk menghindarinya, gunakan:
```
CREATE DATABASE IF NOT EXISTS perpustakaan;
```
Dengan cara ini, error bisa dihindari.

### Part-4: Membuat Tabel
**Perintah Dasar ```CREATE TABLE```:**
Contoh sederhana adalah pembuatan tabel anggota:
```
CREATE TABLE anggota (
    id_anggota INT PRIMARY KEY AUTO_INCREMENT,
    nama VARCHAR(100),
    alamat VARCHAR(150),
    no_telepon VARCHAR(20)
);
```
**Membuat Tabel Buku:**
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

**Kesalahan Umum:**
1. Lupa menggunakan ```USE```
2. Tidak menentukan Primary Key
3. Salah memilih tipe data
4. Panjang kolom tidak memadai

**Best Practice:**
1. Menentukan Primary Key dengan ```AUTO_INCREMENT```
2. Penggunaan Constraint ```NOT NULL``` dan ```UNIQUE```. Constraint ini membantu menjaga integritas data. Misalnya Judul menggunakan **NOT NULL** dan ISBN memakai **UNIQUE** agar tidak ada buku tercatat ganda.

## 3. Modul Session-4: Mengisi dan Mengolah Data
### Part-1: INSERT
**Perintah Dasar ```INSERT```:**
Perintah INSERT digunakan untuk menambahkan baris data baru ke dalam tabel. Sintaks dasarnya adalah:
```
INSERT INTO nama_tabel (kolom1, kolom2, ...) VALUES (nilai1, nilai2, ...);
```
Dengan sintaks ini, setiap nilai dipetakan langsung ke kolom yang sesuai. Pengguna tidak perlu menuliskan kolom dengan AUTO_INCREMENT seperti ```id_buku```, karena MariaDB akan mengisinya otomatis.

**Menambahkan Beberapa Data Sekaligus:**
Selain menambahkan satu baris data, MariaDB mendukung input banyak baris dalam satu query. Teknik ini disebut multi-row insert. Contoh penggunaan multi-row insert:
```
INSERT INTO buku (judul, penulis, tahun_terbit, isbn) VALUES
('Belajar MariaDB', 'Siti Lestari', 2021, '9786027788990'),
('Manajemen Basis Data Modern', 'Ahmad Yusuf', 2020, '9786021123456'),
('Pengantar Teknologi Informasi', 'Rudi Hartono', 2017, '9786025566778');
```
### Part-2: ```SELECT *```
**Perintah Dasar ```SELECT```:**
Perintah SELECT adalah instruksi utama untuk menampilkan data dalam SQL. Bentuk paling sederhana dari perintah ini adalah:
```
SELECT * FROM nama_tabel;
```
Tanda bintang (*) berarti semua kolom akan ditampilkan. Walaupun sederhana, perintah ini adalah dasar bagi query-query yang lebih kompleks. Misalnya, perintah SELECT bisa digabungkan dengan klausa lain seperti ```WHERE```, ```ORDER BY```, atau ```LIMIT```.

**Menampilkan Data dengan Format yang Lebih Rapi:**
Contoh perintah:
```
SELECT judul, penulis FROM buku;
```
Selain itu, hasil query bisa dibuat lebih informatif dengan memberikan alias pada kolom. Misalnya:
```
SELECT judul AS "Judul Buku", penulis AS "Nama Penulis" FROM buku;
```
### Part-3: ```UPDATE```
**Perintah Dasar UPDATE:**
Perintah UPDATE digunakan untuk memperbarui nilai pada satu atau lebih kolom dalam tabel. Sintaks umum perintah ini adalah:
```
UPDATE nama_tabel SET kolom1 = nilai_baru WHERE kondisi;
```
Perintah UPDATE juga dapat digunakan untuk memperbarui lebih dari satu kolom dalam satu baris. Misalnya, pengguna ingin mengubah judul sekaligus tahun terbit:
```
UPDATE buku SET judul = 'Algoritma Terapan', tahun_terbit = 2020 WHERE id_buku = 1;
```
**Mengubah Beberapa Baris Data Sekaligus:**
Selain mengubah satu baris, UPDATE juga bisa digunakan untuk memperbarui banyak baris sekaligus. Hal ini dilakukan dengan memperluas kondisi dalam klausa WHERE. Misalnya, jika semua buku yang terbit sebelum tahun 2000 ingin diubah penulisnya menjadi “Anonim”, query yang digunakan adalah:
```
UPDATE buku SET penulis = 'Anonim' WHERE tahun_terbit < 2000;
```
### Part-4: ```DELETE```
**Perintah Dasar DELETE:**
Perintah DELETE digunakan untuk menghapus satu atau lebih baris dari tabel. Sintaks umumnya adalah:
```
DELETE FROM nama_tabel WHERE kondisi;
```
Kata kunci ```WHERE``` sangat penting karena menentukan baris mana yang akan dihapus. Tanpa WHERE, semua baris dalam tabel akan hilang. Misalnya, untuk menghapus satu buku dengan ```id_buku = 5```, query yang digunakan adalah:
```
DELETE FROM buku WHERE id_buku = 5;
```
Selain menghapus satu baris, DELETE juga dapat digunakan untuk menghapus lebih dari satu baris sekaligus. Perintahnya yaitu:
```
DELETE FROM buku WHERE tahun_terbit < 1990;
```
**Menghapus Beberapa Baris Sekaligus:**
Perintah DELETE memungkinkan pengguna menghapus banyak baris sekaligus dengan menggunakan kondisi tertentu. Misalnya, jika perpustakaan ingin menghapus semua buku yang tidak memiliki ISBN (kosong), maka query yang digunakan adalah:
```
DELETE FROM buku WHERE isbn IS NULL;
```
**Lakukan Backup Sebelum Menghapus:**
Sebelum menghapus data penting, lakukan backup terlebih dahulu dengan query:
```
CREATE TABLE buku_backup AS SELECT * FROM buku;
```
