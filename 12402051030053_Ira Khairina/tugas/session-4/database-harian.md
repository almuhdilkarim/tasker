# Tutorial Membuat Database Tugas Harian dengan MariaDB
## 1. Membuat Database 
Setelah masuk ke MariaDB, buatlah database baru. Database ini akan menjadi 'akun' kamu bagi tabel di tugas harian kamu. Misalnya, kita buat database dengan nama database: irakassignments.

`CREATE DATABASE irakassignments;`

Setelah membuat database, cek terlebih dahulu apakah database berhasil dibuat dengan menggunakan:

`SHOW DATABASES;`

## 2. Menggunakan Database
Pilih database yang akan dipakai dengan menggunakan syntax:

`USE irakassginments;`

Perlu diingat bahwa command ini penting untuk digunakan, bila tidak maka data yang sudah dibuat akan tersimpan di tempat lain.

## 3. Membuat Tabel
Untuk membuat tabel, kamu perlu menggunakan command `CREATE TABLE`. Command ini digunakan untuk membuat struktur tabel di dalam database. Jadi, sebelum menyimpan data, kita perlu membuat "wadah" -nya dulu. 

`CREATE TABLE tugas (
    id_tugas INT AUTO_INCREMENT PRIMARY KEY,
    nama_mata_kuliah VARCHAR(100) NOT NULL,
    tanggal_deadline DATE NOT NULL,
    keterangan ENUM('belum selesai', 'selesai') NOT NULL
);`

## 4. Mengecek Struktur Tabel
Untuk melihat struktur tabel sudah benar, gunakan syntax `DESCRIBE tugas;`

## 5. Mengisi Data (INSERT INTO)
Untuk mengisi data tabel, kita perlu menggunakan command `INSERT INTO` untuk memasukkan data ke dalam tabel. 
Diibaratkan Tabel adalah botol minum dan INSERT INTO adalah air yang mengisi botol tersebut.

`INSERT INTO tugas (nama_mata_kuliah, tanggal_deadline, keterangan) VALUES
('teknologi basis data', '2025-10-13', 'belum selesai'),
('bahasa inggris', '2025-10-14', 'selesai'),
('komunikasi', '2025-10-02', 'selesai'),
('deskripsi bibliografi', '2025-10-14', 'belum selesai'),
('literasi informasi', '2025-10-24', 'belum selesai'),
('sarana tata ruang perpus', '2025-10-09', 'selesai');`

id_tugas AUTO_INCREMENT, tidak perlu diisi manual.

## 6. Menampilkan Data 
Bila kamu ingin melihat hasil isi database yang baru saja kamu buat, kamu bisa menggunakan `SELECT * FROM tugas;`
Ini akan menampilkan isi tabel yang sudah diisi.
