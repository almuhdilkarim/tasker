# Review Modul
## Pertemuan 2 - Pengantar
### Modul 2: Data
Modul ini membahas mengenai **Data dan Konsep Dasar Data**. Data didefinisikan sebagai fakta, catatan, atau observasi yang belum diolah dan bisa berupa apa saja, seperti angka, teks, gambar, atau audio. Data penting karena menjadi dasar dari informasi, wawasan, dan pengambilan keputusan di berbagai bidang, terutama dalam dunia digital.

Modul ini juga menjelaskan tentang **Siklus Hidup Data** (mulai dari pembuatan/pengumpulan, penyimpanan, pemrosesan, hingga penghancuran), **Karakteristik Data yang Baik** (seperti akurat, relevan, lengkap, terstruktur, dan terpercaya), dan **Peran Penting Data dalam Karier** (di mana data merupakan aset vital yang memengaruhi setiap aspek pekerjaan dan pengambilan keputusan bisnis, serta penting untuk berbagai profesi). Selain itu, dibahas juga mengenai **Kualitas Data** yang menekankan pentingnya data yang valid, akurat, dan dapat dipercaya untuk menghasilkan informasi dan wawasan yang tepat.


### Modul 3: Database
Modul ini membahas kebutuhan akan *database* muncul karena adanya **Keterbatasan Penyimpanan Manual**, di mana metode manual lambat, tidak efisien, dan rentan terhadap kesalahan. *Database* menawarkan **Akses Cepat ke Data**, memungkinkan pengambilan keputusan yang cepat dan tepat. Selain itu, *database* menjamin **Konsistensi dan Integritas Data**, memastikan data akurat, valid, dan terpercaya.

Fungsi vital lain dari *database* adalah menyediakan **Keamanan Data** yang lebih terjamin dan unggul. *Database* juga menghasilkan **Efisiensi dan Penghematan Sumber Daya** melalui pengurangan biaya operasional dan waktu. Terakhir, *database* memiliki kemampuan **Skalabilitas dan Adaptabilitas** yang tinggi, sehingga dapat menampung pertumbuhan volume data dan beradaptasi dengan kebutuhan sistem yang berubah-ubah. Secara keseluruhan, *database* merupakan solusi modern yang efisien, aman, dan esensial dalam pengelolaan data di berbagai sektor, termasuk **Dampak Database pada Perpustakaan** yang sangat membantu dalam pengarsipan, pengelolaan koleksi, dan pelayanan.

### Modul 4: DBMS
Modul ini membahas perbandingan antara **File Biasa (File System)** dengan **Database Management System (DBMS)** dalam pengelolaan data. Secara umum, **File Biasa** menyimpan data secara terpisah dalam *file* individu tanpa relasi dan memiliki banyak kekurangan, seperti redundansi data, kesulitan mencari dan mengolah data, serta keamanan yang rendah.

Sebaliknya, **DBMS** hadir sebagai solusi unggul yang mengatasi kelemahan tersebut. Secara **Struktural**, DBMS menyimpan data secara terelasi, terstruktur, dan terintegrasi. Secara **Operasional**, DBMS menggunakan bahasa query seperti SQL untuk pengelolaan dan manipulasi data yang canggih, menawarkan **Efisiensi Penyimpanan** yang lebih baik, menjamin **Keamanan dan Perlindungan Data** melalui kontrol akses, serta memastikan **Konsistensi dan Integritas Data** yang tinggi melalui mekanisme seperti transaksi ACID. Studi kasus perpustakaan menegaskan bahwa DBMS, meskipun lebih kompleks, jauh lebih unggul dalam skalabilitas, efisiensi, dan kualitas layanan dibandingkan sistem *file* biasa.

### Modul 5: MariaDB
Modul ini memperkenalkan dan menjelaskan **MariaDB**, sebuah sistem manajemen basis data relasional (*Relational Database Management System - RDBMS*) sumber terbuka (*open source*) yang populer.

MariaDB adalah *fork* dari MySQL yang dikembangkan oleh pendiri asli MySQL. Keunggulan utamanya terletak pada **Lisensi *Open Source***-nya, yang menjamin ketersediaan fitur gratis dan perlindungan dari pengambilalihan perusahaan. MariaDB dikenal menawarkan **Performa Optimal** dengan kecepatan tinggi dalam pemrosesan data, serta memiliki **Fitur Keamanan Unggulan** yang komprehensif untuk melindungi data penting. Selain itu, MariaDB menawarkan **Skalabilitas dan Adaptabilitas** yang baik untuk menangani beban kerja tinggi, serta memiliki **Kompatibilitas** yang kuat dengan berbagai sistem operasi dan perangkat lunak lain, terutama dengan MySQL. MariaDB secara keseluruhan menjadi pilihan yang andal dan kuat untuk pengelolaan data di berbagai skala.

### Modul 6: Potensi
Modul ini membahas **Potensi Penggunaan Database** dan aplikasinya di berbagai sektor.

**Database** adalah elemen kunci dalam revolusi digital karena kemampuannya mengelola, menyimpan, dan menyajikan data dalam jumlah besar dengan cepat dan akurat. Penerapan *database* memiliki dampak signifikan di berbagai bidang:

* **Bidang Pendidikan**: *Database* digunakan untuk pengelolaan data siswa/mahasiswa, sistem akademik, perpustakaan digital, dan memfasilitasi penelitian dengan cepat dan mudah.
* **Dunia Bisnis**: *Database* sangat penting untuk pengelolaan data pelanggan (*Customer Relationship Management - CRM*), inventaris, keuangan, dan analisis pasar, memungkinkan pengambilan keputusan strategis dan peningkatan efisiensi operasional.
* **Pemerintahan & Publik**: *Database* digunakan untuk layanan publik, pengarsipan dokumen negara, pengelolaan data kependudukan, pajak, dan keamanan, yang bertujuan meningkatkan akuntabilitas dan efisiensi layanan.
* **Peran Data dalam Era Digital**: Secara umum, *database* bertindak sebagai "jantung" yang menampung semua data yang dihasilkan, membuatnya siap diolah menjadi informasi berharga, mendukung sistem *Big Data* dan kecerdasan buatan (*Artificial Intelligence - AI*).

Singkatnya, *database* adalah fondasi penting yang memungkinkan pengolahan data masif menjadi wawasan yang berguna, serta menjadi kunci untuk adaptasi, inovasi, dan peningkatan efisiensi di era digital.


## Pertemuan 3 - Struktur Database
### Modul 1: Tabel
Modul ini menjelaskan secara fundamental mengenai **Konsep Database dan Tabel** dalam konteks MariaDB.

**Database** didefinisikan sebagai wadah data terstruktur yang dikelola oleh DBMS untuk mendukung berbagai aplikasi. Inti dari database relasional adalah **Tabel**, yang berfungsi sebagai struktur dasar untuk menyimpan data secara terorganisir dalam bentuk baris dan kolom.

* **Baris** merepresentasikan satu *record* data atau entitas (misalnya, satu anggota), memberikan granularitas data yang rinci.
* **Kolom** merepresentasikan atribut spesifik dari entitas tersebut (misalnya, "nama" atau "alamat"), dengan tipe data yang sudah ditentukan untuk memastikan validitas dan konsistensi data.

Konsep kunci dalam tabel adalah **Primary Key (Kunci Utama)**, yang merupakan kolom unik (tidak boleh ada duplikasi) untuk mengidentifikasi setiap baris secara mutlak. **Relasi Antar Tabel** dibangun melalui **Foreign Key (Kunci Asing)**, yang merupakan *Primary Key* dari satu tabel yang diletakkan di tabel lain untuk menciptakan hubungan logis antar data. Relasi ini penting untuk menghindari redundansi data dan menjaga integritas serta konsistensi data di seluruh *database*.


### Modul 2: TipeData
Modul ini menjelaskan secara rinci mengenai **Tipe Data Sederhana** dalam konteks *database* MariaDB dan pentingnya memilih tipe data yang tepat.

Tipe data dasar yang dibahas meliputi:
1.  **Tipe Data Angka/Numerik**: Digunakan untuk menyimpan nilai numerik, dibagi menjadi bilangan bulat (*integer*) dan bilangan desimal (*float* atau *decimal*).
2.  **Tipe Data Teks/String**: Digunakan untuk menyimpan karakter, seperti nama atau alamat, dengan tipe umum seperti **VARCHAR** (panjang variabel) dan **CHAR** (panjang tetap).
3.  **Tipe Data Boolean/Logikal**: Digunakan untuk merepresentasikan dua nilai logis, yaitu *True* (1) atau *False* (0), yang sering diwakili oleh tipe data **TINYINT** dalam MariaDB.
4.  **Tipe Data Tanggal dan Waktu**: Digunakan untuk merekam informasi waktu (*DATE*, *TIME*, *DATETIME*).

Pemilihan Tipe Data yang Tepat sangat krusial karena memengaruhi konsistensi, efisiensi penyimpanan, dan akurasi informasi yang diolah. Kesalahan dalam pemilihan, seperti menggunakan tipe data yang terlalu besar atau tidak sesuai, dapat menyebabkan pemborosan ruang dan menghambat integrasi data. Studi kasus perpustakaan menunjukkan bagaimana kombinasi tipe data seperti **INT**, **VARCHAR**, **YEAR**, dan **DATE** digunakan untuk mendesain tabel buku dan peminjaman secara efisien.

### Modul 3: Database
Modul ini menjelaskan langkah-langkah dan sintaks dasar untuk **Membuat Database Baru** menggunakan perintah **CREATE DATABASE** di MariaDB.

#### Membuat Database dengan `CREATE DATABASE`
Prosesnya dimulai dengan *login* ke MariaDB dan menggunakan perintah dasar `CREATE DATABASE` diikuti dengan nama *database* yang diinginkan, seperti `CREATE DATABASE perpustakaan;`. Teks juga menyajikan opsi tambahan (**Optional Parameter**) yang penting, yaitu:
* **DEFAULT CHARACTER SET utf8mb4**: Menetapkan karakter *encoding* universal untuk mendukung berbagai bahasa.
* **COLLATE**: Menentukan aturan penyortiran karakter.

#### Verifikasi dan Praktik Terbaik
Setelah pembuatan, *database* dapat diverifikasi menggunakan perintah `SHOW DATABASES;` untuk melihat daftar *database* yang ada, atau `SELECT DATABASE();`untuk melihat *database* yang sedang aktif.

Teks ini menekankan **Best Practice** penting, yaitu:
1.  Menggunakan nama *database* yang jelas (misalnya `perpustakaan` daripada `db1`).
2.  Selalu menambahkan klausa **IF NOT EXISTS** pada perintah *CREATE* (`CREATE DATABASE IF NOT EXISTS perpustakaan;`) untuk mencegah kesalahan jika *database* dengan nama yang sama sudah ada.
3.  Menetapkan **UTF-8** untuk menjaga kompatibilitas data.

Dalam Studi Kasus Perpustakaan, *database* bernama **perpustakaan** dibuat sebagai wadah terpusat untuk menampung tabel-tabel seperti anggota, buku, dan peminjaman, yang kemudian diaktifkan menggunakan perintah `USE perpustakaan;`. Proses ini adalah fondasi penting untuk mengelola semua informasi secara teratur dan konsisten.

### Modul 4: Tabel
Mdoul ini membahas langkah-langkah dan *syntax* **CREATE TABLE** untuk **Membuat Tabel Sederhana** di MariaDB, serta praktik terbaik yang harus diikuti.

#### Persiapan dan Sintaks Dasar
Sebelum membuat tabel, penting untuk memilih *database* yang akan digunakan dengan perintah `USE namadatabase;`. Sintaks dasar untuk membuat tabel adalah `CREATE TABLE nama_tabel (definisi_kolom);`, di mana setiap definisi kolom mencakup `Nama Kolom`, `Tipe Data`, dan `Batasan (Constraint)`

#### Contoh Tabel Anggota dan Buku
Teks memberikan contoh pembuatan dua tabel utama:
1.  **Tabel Anggota**: Dirancang untuk menyimpan data pribadi anggota perpustakaan, menggunakan `id_anggota` sebagai **PRIMARY KEY** dengan opsi **AUTO_INCREMENT** (nilai otomatis bertambah). Kolom lain seperti `nama`, `alamat`, dan `no_telepon` menggunakan tipe data **VARCHAR**.
2.  **Tabel Buku**: Dirancang untuk koleksi buku, menggunakan `id_buku` sebagai **PRIMARY KEY**. Kolom seperti `judul`, `penulis`, `tahun_terbit` (*YEAR*), dan `isbn` (**UNIQUE KEY**) juga didefinisikan.

#### Kesalahan Umum dan Praktik Terbaik
Modul ini juga menggarisbawahi beberapa kesalahan umum dan **Best Practice**:
* **Kesalahan Umum**: Lupa menggunakan `USE`, tidak menentukan **PRIMARY KEY**, salah memilih tipe data, atau menentukan panjang kolom yang tidak memadai.
* **Best Practice**: Selalu menggunakan **AUTO\_INCREMENT** untuk *Primary Key* numerik untuk memastikan keunikan, dan memilih tipe data yang tepat serta batasan **NOT NULL** untuk menjaga integritas data.

Secara keseluruhan, modul ini memandu pengguna dalam membangun fondasi *database* dengan mendefinisikan tabel dan kolom secara efisien dan akurat.

### Modul 5: Praktik
Modul ini menjelaskan praktik lengkap **Membuat Tabel Buku** di MariaDB, mulai dari pembuatan struktur hingga penambahan data, sekaligus menyoroti kesalahan umum dan praktik terbaik.

#### Praktik Membuat Tabel Buku

1.  **Pembuatan Struktur (CREATE TABLE)**:
    Tabel `buku` dibuat dengan perintah **`CREATE TABLE`** yang mendefinisikan kolom-kolom:

      * `id_buku`: **`INT PRIMARY KEY AUTO_INCREMENT`** (kunci unik yang otomatis bertambah).
      * `judul`: **`VARCHAR(150) NOT NULL`** (teks wajib diisi).
      * `penulis`: **`VARCHAR(100)`**.
      * `tahun_terbit`: **`YEAR`** (tipe data khusus tahun).
      * `isbn`: **`VARCHAR(20) UNIQUE`** (nomor unik yang tidak boleh terulang).

2.  **Penambahan Data (INSERT INTO)**:
    Data buku dimasukkan ke dalam tabel menggunakan perintah **`INSERT INTO`**.

    ```bash
    INSERT INTO buku (judul, penulis, tahun_terbit, isbn) 
    VALUES ('Dasar-Dasar Basis Data', 'Ani Rahmadani', 2023, '978-602-03-3456-7');
    ```

3.  **Verifikasi Data (SELECT)**:
    Isi tabel diperiksa menggunakan perintah **`SELECT * FROM buku;`** untuk memastikan data berhasil dimasukkan dan `id_buku` otomatis terisi.

#### Kesalahan Umum & Best Practice

Modul ini menekankan pentingnya **Integritas Data** melalui:

  * **Kesalahan**: Tidak memberi *constraint* **`NOT NULL`** pada kolom penting (`judul`), tidak memberi *constraint* **`UNIQUE`** pada kolom yang harus unik (`isbn`), dan salah memilih tipe data (misalnya, menggunakan `VARCHAR` untuk `tahun_terbit` padahal harusnya **`YEAR`**).
  * **Best Practice**: Selalu gunakan **`AUTO_INCREMENT`** pada *Primary Key* numerik dan terapkan *constraint* **`NOT NULL`** serta **`UNIQUE`** yang sesuai untuk menjamin kualitas data.

  ## Pertemuan 4 - Mengisi dan Mengelola Data
  ### Modul 1: Insert
  Modul ini menjelaskan proses **Menambahkan Data ke Tabel** menggunakan perintah **INSERT** di MariaDB.

#### Menambahkan Data dengan INSERT

Perintah utama yang digunakan adalah **`INSERT INTO`**, yang memasukkan baris data baru ke dalam tabel yang sudah ada.

#### Sintaks Dasar

Data harus dimasukkan sesuai dengan urutan kolom yang ditentukan, dan tipe datanya harus cocok. Teks ini menganjurkan untuk selalu menyebutkan nama-nama kolom secara eksplisit, meskipun kolom *Primary Key* dengan **`AUTO_INCREMENT`** (seperti `id_buku`) dapat diabaikan, karena nilainya akan diisi otomatis oleh sistem.

```bash
# Sintaks INSERT ke satu baris data
INSERT INTO buku (judul, penulis, tahun_terbit, isbn) 
VALUES ('Nilai Judul', 'Nilai Penulis', 2024, '978-X-XXX-XXXX-X');
```

#### Praktik Terbaik (Best Practice)

1.  **Gunakan Multi-Row Insert**: Jika ada banyak data yang ingin dimasukkan, menggunakan *multi-row insert* lebih efisien.
    ```bash
    # Sintaks INSERT untuk beberapa baris data sekaligus
    INSERT INTO buku (judul, penulis, tahun_terbit, isbn) 
    VALUES 
    ('Buku Satu', 'Penulis A', 2023, '111-222'), 
    ('Buku Dua', 'Penulis B', 2024, '333-444');
    ```
2.  **Perhatikan Integritas Data**: Penting untuk memastikan data yang dimasukkan mematuhi aturan tabel (misalnya, `isbn` harus **`UNIQUE`** dan kolom yang `NOT NULL` tidak boleh kosong) untuk mencegah kesalahan dan menjaga akurasi sistem.

Setelah data dimasukkan, isinya dapat diperiksa menggunakan perintah **`SELECT * FROM buku;`**. Modul ini juga menekankan kesalahan umum seperti tidak menyertakan kolom yang wajib diisi (**`NOT NULL`**), jumlah nilai yang tidak sesuai dengan jumlah kolom, dan format data yang tidak tepat.

### Modul 2: Select
Modul ini menjelaskan cara **Menampilkan Isi Tabel** menggunakan perintah `SELECT` di MariaDB.

#### Menampilkan Data dengan SELECT

`SELECT`adalah perintah SQL paling penting yang berfungsi untuk mengambil dan menampilkan data dari tabel. Tujuannya adalah untuk mendapatkan informasi yang dibutuhkan untuk analisis dan pengambilan keputusan.

#### Perintah Dasar

1.  **Menampilkan Semua Data**: Perintah **`SELECT * FROM [nama_tabel];`** digunakan untuk menampilkan **semua kolom** dan **semua baris** yang ada dalam tabel (misalnya, `SELECT * FROM buku;`).
2.  **Menampilkan Kolom Tertentu**: Untuk efisiensi, sebaiknya hanya sebutkan kolom yang dibutuhkan.
    ```bash
    # Contoh hanya menampilkan kolom judul dan penulis
    SELECT judul, penulis FROM buku; 
    ```

#### Praktik Terbaik (Best Practice)

  * **Aliasing (Memberi Nama Lain)**: Gunakan **`AS`** untuk memberi nama sementara yang lebih jelas pada kolom hasil *query* (misalnya, `SELECT judul AS "Judul Buku", penulis FROM buku;`).
  * **Batasi Hasil dengan LIMIT**: Untuk tabel besar, gunakan **`LIMIT`** untuk membatasi jumlah baris yang ditampilkan, membantu dalam pengujian data tanpa membebani sistem (misalnya, `SELECT * FROM buku LIMIT 5;`).
  * **Verifikasi Struktur**: Gunakan perintah **`DESCRIBE [nama_tabel];`** terlebih dahulu untuk melihat struktur kolom (nama dan tipe data) guna menghindari kesalahan penulisan (*typo*) dalam *query* **`SELECT`**.

Secara keseluruhan, `SELECT`memungkinkan pengguna untuk mengambil data dari *database* secara fleksibel dan efisien, menjadikannya alat penting dalam manajemen informasi.

### Modul 3: Update
Modul ini membahas cara **Mengubah Data** di dalam tabel menggunakan perintah `UPDATE` di MariaDB.

#### Mengubah Data dengan `UPDATE`

`UPDATE` adalah perintah DML yang digunakan untuk memodifikasi nilai di satu atau lebih kolom pada baris data yang sudah ada di dalam tabel.

#### Perintah Dasar

Perintahnya menggunakan sintaks **`UPDATE [nama_tabel] SET [kolom] = [nilai_baru] WHERE [kondisi];`**. Kunci sukses dari perintah ini adalah klausa **`WHERE`**, yang berfungsi sebagai filter untuk memastikan hanya data yang ditargetkan yang diubah. Jika klausa `WHERE` diabaikan, **SEMUA** baris dalam tabel akan terubah, yang merupakan kesalahan fatal.

```bash
# Contoh UPDATE untuk mengubah judul buku dengan ID 3
UPDATE buku 
SET judul = 'Dasar Pemrograman Web' 
WHERE id_buku = 3;

# Contoh UPDATE untuk mengubah beberapa kolom sekaligus pada ID yang sama
UPDATE buku 
SET penulis = 'Joko Purnomo', tahun_terbit = 2022 
WHERE id_buku = 1;
```

#### Praktik Terbaik (Best Practice)

1.  **Selalu Gunakan `WHERE`**: Ini adalah aturan wajib untuk menghindari perubahan data massal yang tidak disengaja.
2.  **Uji Kondisi dengan `SELECT`**: Sebelum menjalankan `UPDATE`, selalu uji dulu klausa `WHERE` menggunakan perintah **`SELECT * FROM [nama_tabel] WHERE [kondisi];`** untuk memverifikasi baris mana saja yang akan terpengaruh.
3.  **Gunakan Transaksi**: Untuk perubahan besar, gunakan **`START TRANSACTION;`** dan `COMMIT` atau `ROLLBACK` untuk menyediakan mekanisme pembatalan (*undo*) jika terjadi kesalahan.

Secara keseluruhan, perintah **UPDATE** harus digunakan dengan hati-hati dan didukung oleh klausa **`WHERE`** yang tepat untuk menjaga integritas dan akurasi data.

### Modul 4: Delete
Modul ini menjelaskan perintah **`DELETE`** di MariaDB, yang digunakan untuk **Menghapus Data** dari tabel, serta praktik terbaik untuk menghindari kehilangan data yang tidak disengaja.

#### Menghapus Data dengan DELETE

Perintah **`DELETE`** adalah operasi fundamental dalam manajemen basis data yang berfungsi untuk menghapus satu atau beberapa baris (*record*) dari sebuah tabel.

#### Perintah Dasar

Sintaksnya mirip dengan `UPDATE` dan sangat bergantung pada klausa **`WHERE`** untuk menentukan baris mana yang akan dihapus.

```bash
# Sintaks DELETE untuk menghapus baris data berdasarkan kondisi tertentu
DELETE FROM [nama_tabel] WHERE [kondisi];

# Contoh menghapus buku dengan ID 3
DELETE FROM buku WHERE id_buku = 3;
```

#### Kesalahan Umum

Kesalahan paling fatal adalah menjalankan perintah **`DELETE`** tanpa klausa **`WHERE`**.

  * **Tidak Menyertakan Klausa `WHERE`**: Jika `WHERE` tidak ada, **semua data** dalam tabel akan terhapus seketika, dan data tersebut tidak dapat dikembalikan.
    ```bash
    # SALAH: Akan menghapus SEMUA data dari tabel buku!
    DELETE FROM buku; 
    ```
  * **Kondisi `WHERE` Terlalu Umum**: Menggunakan kondisi yang terlalu luas juga berbahaya karena bisa menghapus lebih banyak data dari yang diinginkan.

#### Praktik Terbaik (Best Practice)

Kehati-hatian sangat ditekankan saat menggunakan **`DELETE`** karena operasi ini permanen.

1.  **Selalu Gunakan Klausa `WHERE`**: Ini adalah pelindung utama untuk menargetkan hanya baris yang tepat.
2.  **Gunakan `SELECT` untuk Verifikasi**: Sebelum menjalankan `DELETE`, uji kondisinya terlebih dahulu dengan **`SELECT`** untuk memastikan data yang akan terhapus sudah benar. Gunakan kondisi `WHERE` yang sama untuk kedua perintah.
    ```bash
    # Verifikasi data yang akan terhapus
    SELECT * FROM buku WHERE tahun_terbit < 2010;

    # Setelah yakin, eksekusi DELETE
    DELETE FROM buku WHERE tahun_terbit < 2010; 
    ```
3.  **Gunakan Transaksi**: Untuk penghapusan massal, gunakan **`START TRANSACTION`** dan **`ROLLBACK`** untuk memberi kesempatan membatalkan penghapusan jika terjadi kesalahan.
4.  **Lakukan *Backup***: Sebelum menghapus data penting, buatlah cadangan data (*backup*) terlebih dahulu, misalnya dengan membuat tabel *backup* baru.
    ```bash
    CREATE TABLE buku_backup AS SELECT * FROM buku;
    ```

### Modul 5: Praktik
Modul ini berisi proses **Mengisi Data ke Tabel Buku** menggunakan perintah **`INSERT`** di MariaDB, berfokus pada langkah-langkah, kesalahan umum, dan praktik terbaik.

#### Rangkuman Mengisi Data (INSERT INTO)

Modul ini mempraktikkan pengisian data ke dalam tabel `buku` menggunakan perintah **`INSERT INTO`**.

#### Langkah Dasar Mengisi Data

  * **Perintah Utama**: Gunakan `INSERT INTO buku (judul, penulis, tahun_terbit, isbn) VALUES (...)`.
  * **Verifikasi**: Setelah memasukkan data, pastikan data berhasil tersimpan dengan perintah `SELECT * FROM buku;`.

#### Kesalahan Umum (Yang Harus Dihindari)

Kesalahan-kesalahan ini sering terjadi dan dapat merusak integritas data:

  * **ISBN Duplikat**: Mencoba memasukkan ISBN yang sudah ada. Query akan gagal jika kolom ISBN diberi *constraint* **`UNIQUE`**.
  * **Format Tahun Salah**: Mengisi kolom `tahun_terbit` (yang bertipe `YEAR`) dengan format yang tidak tepat, misalnya teks, bukan angka empat digit.
  * **Lupa Menyebutkan Kolom**: Tidak menyebutkan nama-nama kolom secara eksplisit dapat menyebabkan MariaDB salah menempatkan nilai data.
  * **Jumlah Nilai Tidak Sesuai Kolom**: Jumlah nilai yang dimasukkan tidak sama dengan jumlah kolom yang disebutkan.

#### Praktik Terbaik (Best Practice)

Untuk proses pengisian data yang lebih efisien dan aman:

  * **Gunakan Multi-Row Insert**: Memasukkan beberapa baris data sekaligus dalam satu perintah `INSERT` lebih efisien dan cepat.
    ```bash
    INSERT INTO buku (judul, penulis, tahun_terbit, isbn) 
    VALUES 
    ('Buku Satu', 'Penulis A', 2023, '...'), 
    ('Buku Dua', 'Penulis B', 2024, '...'); 
    ```
  * **Gunakan Kolom Secara Eksplisit**: Selalu sebutkan nama-nama kolom yang ingin diisi untuk menghindari kesalahan urutan.
  * **Validasi ISBN Sebelum Insert**: Lakukan pemeriksaan terlebih dahulu (misalnya dengan `SELECT`) untuk memastikan ISBN belum ada di *database*.
  * **Periksa Data dengan `SELECT`**: Setelah *insert* dilakukan, selalu gunakan `SELECT` untuk memverifikasi data baru sudah tersimpan sesuai harapan.

  ## Pertemuan 5 - Mencari Data
  ### Modul 1: Kolom
  Modul ini membahas tentang **Cara Menampilkan Kolom Tertentu**.

  Menampilkan kolom tertentu dari sebuah tabel menggunakan perintah SELECT adalah langkah penting agar data yang dihasilkan lebih efisien dan relevan. Ketimbang menampilkan semua kolom dengan `SELECT *`, memilih hanya kolom yang benar-benar dibutuhkan seperti judul dan penulis dari tabel buku akan membuat hasil query lebih ringkas dan mudah dipahami. Hal ini sangat berguna terutama ketika tabel berisi banyak kolom dan data, sehingga mengurangi beban sistem dan memudahkan pengguna dalam mengambil keputusan.

Beberapa poin penting dalam praktik ini adalah:  
-  Gunakan sintaks dasar `SELECT kolom1, kolom2 FROM nama_tabel;` untuk menampilkan kolom tertentu sesuai kebutuhan.  
-  Manfaatkan alias dengan kata kunci AS agar nama kolom pada hasil query lebih deskriptif dan ramah pengguna, misalnya S`ELECT judul AS "Judul Buku", penulis AS "Nama Penulis"`.  
-  Selalu verifikasi nama kolom dengan perintah DESCRIBE untuk menghindari kesalahan penulisan yang bisa menyebabkan error saat menjalankan query.  
-  Hindari kebiasaan menggunakan `SELECT *` yang dapat menampilkan data berlebihan dan memperlambat sistem, kecuali memang diperlukan semua data.  
-  Sesuaikan pilihan kolom dengan tujuan laporan atau analisis, misalnya menampilkan judul dan tahun_terbit untuk mengetahui tren penerbitan buku.

Dengan menguasai teknik ini, pengguna database dapat menyusun query yang tepat sasaran, mempercepat proses analisis, dan menghasilkan laporan yang komunikatif bagi berbagai pemangku kepentingan. Selain itu, praktik ini menjadi fondasi penting untuk mempelajari query yang lebih kompleks seperti penyaringan data menggunakan WHERE atau pengurutan dengan ORDER BY. Pendekatan ini tidak hanya mengoptimalkan pemanfaatan data, tetapi juga meningkatkan profesionalisme dalam penyajian informasi dari database perpustakaan.

### Modul 2: Where
Modul ini membahas bagaimana **Cara Menyaring  Data Dengan `WHERE`**

Klausa WHERE dalam SQL sangat penting untuk menyaring data sehingga hanya informasi yang sesuai kondisi tertentu yang ditampilkan, misalnya buku terbit tahun 2020 atau karya penulis tertentu. Langkah awal yang harus dilakukan adalah memastikan database aktif dengan `USE perpustakaan;` lalu memeriksa isi dan struktur tabel menggunakan `SELECT * FROM buku;` dan `DESCRIBE buku;` agar kondisi penyaringan tepat dan sesuai tipe data.

Beberapa poin penting dalam penggunaan WHERE:

-  Sintaks dasar: `SELECT kolom1, kolom2 FROM tabel WHERE kondisi;` untuk memilih data spesifik.
-  Kombinasi kondisi dengan operator logika `AND`, `OR` untuk hasil lebih tepat.
-  Penulisan nilai teks harus diapit tanda kutip tunggal, misalnya `'Sinta Dewi'`.
-  Periksa nilai yang ada di tabel dengan `SELECT DISTINCT` untuk menghindari kondisi yang salah atau kosong.
-  Hindari menulis kondisi terlalu umum agar hasil query relevan.

Dengan mengikuti praktik terbaik seperti selalu mengecek struktur tabel, menulis kondisi yang spesifik dan benar, serta menggunakan tanda kutip untuk nilai teks, pengguna dapat menyaring data secara efektif. Studi kasus perpustakaan menunjukkan bahwa klausa WHERE memberikan kemampuan filter data yang membuat analisis dan pengambilan keputusan menjadi lebih cepat dan tepat sasaran. Penguasaan klausa ini adalah fondasi yang penting sebelum melangkah ke penggunaan operator perbandingan yang lebih kompleks.

### Modul 3: Operator
Modul ini membahas **Operator Perbandingan**.

Operator perbandingan seperti `=`, `>`, `<`, dan `LIKE` merupakan fitur utama dalam klausa WHERE yang memungkinkan penyaringan data lebih presisi sesuai kebutuhan analisis. Misalnya, pustakawan bisa memilih buku yang terbit pada tahun tertentu atau mencari buku dengan judul mengandung kata kunci spesifik. Sebelum menggunakan operator ini, penting memastikan database aktif dengan `USE perpustakaan;` dan memeriksa struktur tabel menggunakan `DESCRIBE buku;` agar operator sesuai dengan tipe data kolom. Selain itu, melihat data dengan `SELECT * FROM buku;` membantu memahami nilai-nilai agar kondisi yang dibuat efektif.

Beberapa poin penting penggunaan operator perbandingan:

-  Gunakan operator `=` untuk pencarian nilai persis, misalnya `tahun_terbit = 2020.`
-  Gunakan `>` atau `<` untuk memilih data dengan nilai lebih besar atau lebih kecil, seperti buku terbit setelah 2018.
-  Gunakan `LIKE` dengan wildcard `%` untuk pencarian pola teks, misalnya `judul LIKE '%Pemrograman%'`.
-  Pastikan nilai teks diapit tanda kutip tunggal dan operator sesuai tipe data, guna menghindari error.
-  Tempatkan wildcard `%` secara tepat pada pola `LIKE` untuk mendapatkan hasil pencarian yang akurat.
-  Hindari perbedaan huruf besar-kecil dengan fungsi L`OWER()` atau `UPPER()` untuk pencarian teks yang konsisten.

Studi kasus perpustakaan menunjukkan bahwa operator ini sangat berguna untuk mencari koleksi yang relevan, seperti buku dengan kata kunci tertentu pada judul atau buku terbaru berdasarkan tahun terbit. Penguasaan operator perbandingan meningkatkan kemampuan analisis data dan mempermudah pengambilan keputusan dalam pengelolaan perpustakaan. Dengan pemahaman ini, peserta bisa melangkah ke modul lanjutan seperti pengurutan data dengan `ORDER BY`.

### Modul 4: Urut
Modul ini membahas tentang **cara mengurutkan data dengan `ORDER BY`**. Klausa `ORDER BY` dalam SQL memungkinkan pengguna untuk mengurutkan hasil query sesuai kebutuhan, seperti urutan abjad berdasarkan judul atau kronologis berdasarkan tahun terbit. Sebelum menggunakan ORDER BY, pastikan database aktif dengan menjalankan `USE perpustakaan;` dan verifikasi dengan `SELECT DATABASE();`. Memahami struktur tabel buku dengan kolom `id_buku`, `judul`, `penulis`, `tahun_terbit`, dan isbn juga penting agar pengurutan sesuai konteks.

Poin penting penggunaan ORDER BY:

-  Gunakan `ORDER BY` kolom `ASC` untuk urutan menaik atau DESC untuk menurun.
-  Pengurutan bisa berdasarkan satu kolom atau lebih, misalnya `ORDER BY penulis ASC`, `tahun_terbit DESC`.
-  Kombinasikan `ORDER BY` dengan klausa `WHERE` agar hasil lebih relevan.
-  Pastikan nama kolom yang dipakai di `ORDER BY` benar dan tampilkan juga kolom tersebut untuk memudahkan interpretasi.
-  Tuliskan arah urutan secara eksplisit walau `ASC` adalah default.
-  Perhatikan indeks pada kolom yang diurutkan untuk menjaga performa pada tabel besar.

Studi kasus perpustakaan memperlihatkan manfaat `ORDER BY` dalam menyusun katalog abjad atau menampilkan koleksi terbaru dengan rapi. Penguasaan klausa ini penting untuk menghasilkan laporan profesional yang mudah dipahami dan mendukung pengambilan keputusan.

### Modul 5: Praktik
Modul ini membahas bagaimana **Cara Mencari Buku Berdasarkan Penulis**.

Mencari buku berdasarkan penulis menggunakan klausa `WHERE` dan operator seperti `=` dan `LIKE` sangat penting dalam manajemen perpustakaan. Langkah awal adalah memastikan database aktif dengan perintah `USE perpustakaan;` dan memeriksa struktur tabel menggunakan `DESCRIBE buku;` serta meninjau data dengan `SELECT * FROM buku;` agar filter yang dibuat tepat dan sesuai tipe data.

Poin penting dalam pencarian buku berdasarkan penulis:

-  Gunakan operator `=` untuk pencarian nama lengkap, misalnya `WHERE penulis = 'Sinta Dewi'`.
-  Gunakan operator `LIKE` dengan wildcard `%` untuk pencarian sebagian nama, misalnya `WHERE penulis LIKE '%Dewi%'`.
-  Kombinasikan dengan `ORDER BY` untuk mengurutkan hasil, contohnya `ORDER BY tahun_terbit DESC`.
-  Pastikan selalu menulis nilai teks di dalam tanda kutip tunggal agar query tidak error.
-  Gunakan `SELECT DISTINCT penulis FROM buku;` untuk memverifikasi nama penulis sebelum membuat query.

Studi kasus perpustakaan menunjukkan bahwa pencarian berbasis penulis membuat layanan menjadi lebih responsif dan efisien bagi anggota yang hanya mengingat nama penulis. Penguasaan teknik ini juga membantu pustakawan dalam memberikan informasi dengan cepat dan akurat. Dengan memahami kesalahan umum dan praktik terbaik, pengguna siap menulis query pencarian yang fleksibel dan profesional.