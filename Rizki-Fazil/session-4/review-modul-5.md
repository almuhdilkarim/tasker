## Menampilkan Kolom Tertentu
Menampilkan kolom tertentu dari sebuah tabel adalah langkah penting untuk memahami bagaimana data bisa diolah dengan lebih efektif. 
### Perintah Dasar Menampilkan Kolom Tertentu
Perintah dasar untuk menampilkan kolom tertentu sangat sederhana, tetapi memiliki kegunaan yang luas. Sintaksnya adalah `SELECT kolom1, kolom2 FROM nama_tabel;`. Dengan menuliskan kolom secara eksplisit, sistem hanya akan menampilkan data dari kolom tersebut. Misalnya, jika kita ingin menampilkan judul dan penulis dari tabel buku, maka query-nya adalah 
```
SELECT judul, penulis FROM buku;
```
Anda juga dapat menggunakan alias untuk membuat hasil lebih ramah pengguna. Alias ditulis dengan kata kunci `AS` dan digunakan untuk mengganti nama kolom sementara pada hasil tampilan. Contoh query dengan alias adalah 
```
SELECT judul AS "Judul Buku", penulis AS "Nama Penulis" FROM buku;
```
### kesalahan Umum
1. Salah ketik nama kolom sehingga menyebabkan error.
2. Menggunakan `SELECT *` padahal tidak perlu.
3. Lupa menuliskan nama tabel setelah FROM.
4. Tidak memakai alias, sehingga hasil kurang komunikatif.

### Best Practice
1. Tulis kolom secara spesifik sesuai kebutuhan.
2. Gunakan alias untuk memperjelas tampilan laporan.
3. Periksa struktur tabel dengan `DESCRIBE nama_tabel;`.
4. Pilih kolom berdasarkan tujuan analisis atau laporan.

## Menyaring Data Dengan Where
Klausa `WHERE` dalam SQL adalah salah satu fitur terpenting yang memungkinkan pengguna untuk menyaring data berdasarkan kondisi tertentu. 
### Perintah Dasar WHERE
Sintaks dasar penggunaan klausa `WHERE` adalah sebagai berikut:
```
SELECT kolom1, kolom2 FROM nama_tabel WHERE kondisi;
```
Perintah ini memungkinkan pengguna memilih kolom tertentu sekaligus membatasi baris yang ditampilkan sesuai syarat.
Contoh Kasus Misalnya, jika ingin menampilkan semua buku yang diterbitkan pada tahun 2020, maka query-nya adalah:
```
SELECT judul, penulis FROM buku WHERE tahun_terbit = 2020;
```
Klausa WHERE dapat digabungkan dengan operator logika untuk membuat kondisi lebih kompleks. Sebagai contoh, jika ingin menampilkan buku terbitan 2020 karya penulis “Sinta Dewi”, maka query yang digunakan adalah:
```
SELECT judul, penulis FROM buku WHERE tahun_terbit = 2020 AND penulis = 'Sinta Dewi';
```

### Kesalahan Umum
1. Lupa tanda kutip untuk nilai teks sehingga menyebabkan error.
2. Menggunakan nilai yang tidak ada dalam tabel sehingga hasil yang keluar kosong.
3. Menyaring Tanpa Memahami Struktur Kolom
4. Menggunakan Kondisi Terlalu Luas

### Best Practice
1. Selalu Gunakan Kutip untuk Nilai Teks
2. Periksa Data dengan `SELECT` Sebelum `WHERE`
3. Gunakan Kondisi yang Spesifik
4. Kombinasikan Kondisi untuk Akurasi

## Operator Perbandingan 
Operator perbandingan adalah salah satu fitur inti dari SQL yang membuat klausa WHERE semakin kuat dan berguna. Tanpa operator ini, penyaringan data hanya terbatas pada kecocokan sederhana. Dengan operator seperti =, >, <, dan LIKE, pengguna dapat menyeleksi data secara lebih presisi sesuai dengan kebutuhan analisis pengguna. 
### Perintah Dasar Operator Perbandingan
Operator = adalah operator paling sederhana dalam SQL. Fungsinya adalah mencari data yang nilainya sama persis dengan syarat tertentu. Misalnya, jika pustakawan ingin menampilkan semua buku yang terbit pada tahun 2020, query yang digunakan adalah:
```
SELECT judul, penulis FROM buku WHERE tahun_terbit = 2020;
```
operator > digunakan untuk mencari nilai yang lebih besar. Misalnya, untuk menampilkan semua buku yang terbit setelah 2018, pustakawan dapat menjalankan:
```
SELECT judul, tahun_terbit FROM buku WHERE tahun_terbit > 2018;
```
Operator LIKE berfungsi untuk pencarian pola teks. Misalnya, untuk menampilkan semua buku dengan judul yang mengandung kata “Pemrograman”, query yang digunakan adalah:
```
SELECT judul FROM buku WHERE judul LIKE '%Pemrograman%';
```
simbol % wildcard yang mewakili nol atau lebih karakter.

### Kesalahan Umum
1. Menggunakan Operator pada Kolom yang Salah
2. Salah Menempatkan Wildcard pada LIKE
3. Membandingkan Data dengan Format Tidak Sesuai
4. Mengabaikan Sensitivitas Pola Teks

### Best Practice
1. Gunakan Operator Sesuai Tipe Data
Jika kolom berupa angka atau tanggal, gunakan > atau <. Jika kolom berupa teks, gunakan = atau LIKE.
2. Gunakan Wildcard Secara Tepat
Gunakan simbol `%` pada LIKE sesuai dengan pola yang diinginkan. Jika ingin mencari teks di mana saja, gunakan `%teks%`. Jika hanya di awal, gunakan `teks%`.
3. Gunakan Fungsi Tambahan untuk Konsistensi
Untuk menghindari perbedaan huruf besar kecil, gunakan fungsi `LOWER()` atau `UPPER()`. Dengan cara ini, pencarian teks tidak akan terpengaruh oleh format huruf.
4. Gunakan Operator untuk Analisis Data
Operator perbandingan tidak hanya berguna untuk pencarian, tetapi juga analisis data. Anda bisa mencari jumlah buku baru dengan `>`, atau jumlah buku lama dengan `<`.

## Mengurutkan Data Menggunakan ORDER BY
Mengurutkan data adalah kebutuhan mendasar dalam pengolahan informasi. Tanpa pengurutan, hasil query SQL hanya akan menampilkan data sesuai urutan fisik di tabel, yang tidak selalu sesuai dengan kebutuhan analisis atau laporan. SQL menyediakan klausa ORDER BY untuk memberikan kontrol penuh atas urutan hasil. Dengan klausa ini, pengguna dapat menampilkan data berdasarkan urutan abjad, kronologis, atau bahkan berdasarkan kriteria khusus yang ditentukan. 

### Perintah Dasar
kata `ORDER BY` ditambahkan di akhir query `SELECT`. Secara default, kata `ASC` ini mengurutkan data secara menaik (ascending), tetapi pengguna dapat menambahkan kata kunci `DESC` untuk menampilkan data secara menurun (descending). contoh
urut naik
```
SELECT judul, penulis FROM buku ORDER BY judul ASC;
```
urut menurun
```
SELECT judul, penulis FROM buku ORDER BY judul DESC;
```
### Kesalahan Umum
1. Salah menulis nama kolom
Kesalahan ketik seperti judull akan menyebabkan error karena kolom tidak ditemukan. Solusi: periksa struktur tabel dengan DESCRIBE buku;.
2. Mengurutkan dengan kolom yang tidak ditampilkan
Walau valid, hasil bisa membingungkan karena urutan tidak terlihat jelas di output. Solusi: tampilkan juga kolom pengurutan.
3. Salah memahami urutan default
Default urutan adalah ASC (menaik), bukan DESC (menurun). Biasakan menuliskan arah pengurutan secara eksplisit.
4. Mengabaikan performa pada data besar
ORDER BY tanpa indeks pada tabel besar dapat memperlambat query secara signifikan. Solusi: gunakan indeks pada kolom yang sering diurutkan.

### Best Practice
1. Verifikasi nama kolom sebelum menulis ORDER BY.
2. Tampilkan kolom pengurutan di hasil agar mudah dipahami.
3. Tulis arah urutan secara eksplisit (ASC/DESC) untuk kejelasan.
4. Gunakan indeks pada kolom pengurutan untuk meningkatkan performa.

## Praktik Mencari Buku Berdasarkan Penulis
Mencari buku berdasarkan penulis adalah fitur yang sangat penting dalam sistem manajemen perpustakaan. Anggota perpustakaan sering kali hanya mengingat nama penulis favorit mereka, bukan judul buku secara lengkap. Hal ini membuat klausa WHERE dan operator teks seperti = dan LIKE menjadi sangat relevan untuk kebutuhan sehari-hari.
### Langkah-Langkah Pencarian Berdasarkan Penulis
1. Menggunakan `=`
   ```
   SELECT judul, tahun_terbit FROM buku WHERE penulis = 'Sinta Dewi';
   ```
2. menggunakan `LIKE`
   ```
   SELECT judul, penulis FROM buku WHERE penulis LIKE '%Dewi%';
   ```
3. menggunakan `ORDER BY`
   ```
   SELECT judul, tahun_terbit FROM buku WHERE penulis = 'Sinta Dewi' ORDER BY tahun_terbit DESC;
   ```

### Kesalahan Umum
1. Lupa menambahkan kutip pada nilai teks
Tanpa kutip, SQL mengira nilai tersebut adalah nama kolom, sehingga query error.
2. Salah mengetik nama penulis
SQL mencocokkan teks secara presisi, jadi ejaan yang salah akan menghasilkan hasil kosong.
3. Menggunakan = untuk nama parsial
Operator = hanya cocok untuk pencocokan penuh, bukan sebagian. Untuk mencari sebagian teks gunakan LIKE.
4. Lupa menambahkan wildcard % dalam LIKE
Tanpa %, pencarian hanya cocok dengan nilai persis. % di depan dan belakang teks memungkinkan pencarian lebih fleksibel.

### Best Practice
1. Gunakan kutip tunggal ('') untuk setiap nilai teks.
2. Gunakan LIKE dengan wildcard (%) untuk pencarian sebagian.
3. Kombinasikan dengan ORDER BY untuk hasil yang lebih rapi dan informatif.
