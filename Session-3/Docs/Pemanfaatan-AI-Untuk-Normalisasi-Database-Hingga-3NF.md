# Pemanfaatan AI Untuk Normalisasi Database Hingga 3NF
## 1. Pendahuluan
Dalam perancangan sistem basis data, normalisasi adalah proses sistematis untuk mengorganisasi data guna mengurangi redundansi (pengulangan data) dan ketergantungan yang tidak diinginkan. Studi kasus ini berfokus pada sebuah sistem perpustakaan sederhana, yaitu Perpustakaan Bagas.

Awalnya, data disimpan dalam sebuah tabel yang belum dinormalisasi (unnormalized), dan kemudian kita akan menormalisasinya hingga bentuk normal ketiga (3NF).
## 2. Tujuan
Tujuan dari normalisasi ini adalah:

1. Menghilangkan duplikasi data.

2. Memastikan integritas dan konsistensi data.

3. Membuat struktur tabel yang efisien dan optimal.

4. Memudahkan pengembangan sistem basis data Perpustakaan Bagas.
## 3. Isi
### A. Tabel Belum Dinormalisasi
```
| ID_Peminjaman          | Nama_Peminjam | Alamat  | ID_Buku    | Judul_Buku                       | Pengarang                | Tanggal_Pinjam | Tanggal_Kembali |
| ---------------------- | ------------- | ------- | ---------- | -------------------------------- | ------------------------ | -------------- | --------------- |
| 1                      | Andi          | Jakarta | B001, B002 | Pemrogragam Web, Database Lanjut | Agus Salim, Budi Santoso | 2024-01-01     | 2024-01-07      |
| 2                      | Sinta         | Bandung | B003       | Jaringan Komputer                | Agus Salim               | 2024-01-02     | 2024-01-08      |
```
Ciri-Ciri Belum Dinormalisasi (UNF):

1. Kolom ```ID_Buku```, ```Judul_Buku```, dan ```Pengarang``` mengandung multiple values "Baris 1 menyimpan dua buku sekaligus".

2. Bentuk ini tidak sesuai dengan prinsip atomicitas (1NF) karena satu sel berisi lebih dari satu nilai.

3. Menyulitkan proses:

- Filtering buku tertentu (```WHERE Judul_Buku = ...```)

- Perhitungan statistik (jumlah peminjaman buku tertentu)

- Pemeliharaan data buku/pengarang

### B. Normalisasi 1NF (First Normal Form)
**Tujuan:**
Menghilangkan repeating group (pengulangan kolom) dengan cara memisahkan data menjadi baris individual.
```
| ID_Peminjaman          | Nama_Peminjam | Alamat  | ID_Buku | Judul_Buku        | Pengarang    | Tanggal_Pinjam | Tanggal_Kembali |
| ---------------------- | ------------- | ------- | ------- | ----------------- | ------------ | -------------- | --------------- |
| 1                      | Andi          | Jakarta | B001    | Pemrogragam Web   | Agus Salim   | 2024-01-01     | 2024-01-07      |
| 1                      | Andi          | Jakarta | B002    | Database Lanjut   | Budi Santoso | 2024-01-01     | 2024-01-07      |
| 2                      | Sinta         | Bandung | B003    | Jaringan Komputer | Agus Salim   | 2024-01-02     | 2024-01-08      |
```
Tabel yang telah dinormalisasi 1NF memiliki ciri-ciri:

1. Setiap sel hanya memiliki **satu nilai (atomic)**.

2. Multi-buku dipisah menjadi **baris terpisah**, walaupun ID peminjaman tetap sama (karena satu peminjaman bisa melibatkan lebih dari satu buku).

**Query MariaDB Untuk Membuat Tabel 1NF:**
```
CREATE TABLE Peminjaman_1NF (
    ID_Peminjaman INT,
    Nama_Peminjam VARCHAR(100),
    Alamat VARCHAR(100),
    ID_Buku VARCHAR(10),
    Judul_Buku VARCHAR(100),
    Pengarang VARCHAR(100),
    Tanggal_Pinjam DATE,
    Tanggal_Kembali DATE
);
```
### C. Normalisasi 2NF (Second Normal Form)
**Tujuan:**
Menghilangkan partial dependency (ketergantungan sebagian), yaitu atribut non-primer tidak boleh bergantung hanya pada sebagian dari primary key.

**Pemecahan menjadi 3 tabel:**
1. Peminjam

2. Buku

3. Peminjaman

**Tabel ```PEMINJAM```:**
```
| ID_Peminjam | Nama_Peminjam | Alamat  |
| ----------- | ------------- | ------- |
| 1           | Andi          | Jakarta |
| 2           | Sinta         | Bandung |
```
**Tabel ```BUKU```:**
```
| ID_Buku | Judul_Buku        | Pengarang    |
| ------- | ----------------- | ------------ |
| B001    | Pemrogragam Web   | Agus Salim   |
| B002    | Database Lanjut   | Budi Santoso |
| B003    | Jaringan Komputer | Agus Salim   |
````
**Tabel ```PEMINJAMAN```:**
```
| ID_Peminjaman | ID_Peminjam | ID_Buku | Tanggal_Pinjam | Tanggal_Kembali |
| ------------- | ----------- | ------- | -------------- | --------------- |
| 1             | 1           | B001    | 2024-01-01     | 2024-01-07      |
| 2             | 1           | B002    | 2024-01-01     | 2024-01-07      |
| 3             | 2           | B003    | 024-01-02      | 2024-01-08      |
```

**Query MariaDB Untuk Membuat Tabel 2NF:**
```
CREATE TABLE Peminjam (
    ID_Peminjam INT PRIMARY KEY,
    Nama_Peminjam VARCHAR(100),
    Alamat VARCHAR(100)
);

CREATE TABLE Buku (
    ID_Buku VARCHAR(10) PRIMARY KEY,
    Judul_Buku VARCHAR(100),
    Pengarang VARCHAR(100)
);

CREATE TABLE Peminjaman (
    ID_Peminjaman INT PRIMARY KEY,
    ID_Peminjam INT,
    ID_Buku VARCHAR(10),
    Tanggal_Pinjam DATE,
    Tanggal_Kembali DATE,
    FOREIGN KEY (ID_Peminjam) REFERENCES Peminjam(ID_Peminjam),
    FOREIGN KEY (ID_Buku) REFERENCES Buku(ID_Buku)
);
```

### D. Normalisasi 3NF (Third Normal Form)
**Tujuan:**
Menghilangkan *transitive dependency*, yaitu atribut non-primer tidak boleh bergantung pada atribut non-primer lainnya.

**Evaluasi:**

Pada Tabel ```Buku```, kolom ```Pengarang``` masih tergantung pada ```Judul_Buku```.
Maka kita buat tabel ```Pengarang``` terpisah.

**Tabel ```PENGARANG (BARU)```:**
```
| ID_Pengarang | Nama_Pengarang |
| ------------ | -------------- |
| P001         | Agus Salim     |
| P002         | Budi Santoso   |
```
**Tabel ```BUKU (REVISI)```:**
```
| ID_Buku | Judul_Buku        | ID_Pengarang |
| ------- | ----------------- | ------------ |
| B001    | Pemrogragam Web   | P001         |
| B002    | Database Lanjut   | P002         |
| B003    | Jaringan Komputer | P001         |
```

**Query MariaDB Untuk Membuat Tabel 3NF:**
```
CREATE TABLE Pengarang (
    ID_Pengarang VARCHAR(10) PRIMARY KEY,
    Nama_Pengarang VARCHAR(100)
);

-- Revisi tabel Buku
CREATE TABLE Buku (
    ID_Buku VARCHAR(10) PRIMARY KEY,
    Judul_Buku VARCHAR(100),
    ID_Pengarang VARCHAR(10),
    FOREIGN KEY (ID_Pengarang) REFERENCES Pengarang(ID_Pengarang)
);
```

## Kesimpulan
Dengan melakukan normalisasi hingga bentuk normal ketiga (3NF), database *Perpustakaan Bagas*:

1. Telah **menghilangkan redundansi** data.

2. Memiliki **struktur yang efisien dan fleksibel.**

3. Memungkinkan **pemeliharaan data yang lebih mudah dan akurat.**

4. Siap untuk diimplementasikan dalam sistem informasi berbasis MariaDB.

#### Absen Bagas Wicaksono 3C
<img width="700" height="700" alt="image" src="https://github.com/user-attachments/assets/4f3503db-9c44-4f47-8c26-52d96ab4ec21" />
