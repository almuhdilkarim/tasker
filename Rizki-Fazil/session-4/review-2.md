# Pengantar
## Perkenalan
pada modul pengantar ini, kita akan diperkenalkan dengan data, database, dan membandingkannya dengan DBMS, serta menyingkap mengenai potensi MariaDB.

## Apa itu Data dan Konsep Dasarnya
Data adalah representasi fakta, angka, atau simbol yang disimpan dalam bentuk tertentu sehingga dapat diproses menjadi informasi (Silberschatz, Korth, & Sudarshan, 2020). Dalam konteks sistem informasi, data menjadi pondasi yang memungkinkan organisasi melakukan pencatatan dan analisis. 

Data juga dapat dipahami sebagai sumber daya organisasi yang memiliki nilai strategis (Laudon & Laudon, 2018). Sama seperti aset fisik, data harus dikelola agar dapat dimanfaatkan secara optimal. Perpustakaan modern memanfaatkan data untuk mengetahui pola minat pembaca dan tren peminjaman. Dari sini, pengelola dapat menentukan koleksi mana yang perlu diperbarui. Dengan demikian, data bukan hanya catatan, tetapi juga aset yang mendukung pengambilan keputusan.

Definisi data terus berkembang seiring dengan teknologi yang digunakan untuk menyimpannya (Connolly & Begg, 2015). Jika dulu data hanya berupa catatan manual, kini data hadir dalam bentuk digital yang jauh lebih kompleks. Pada perpustakaan digital, data mencakup informasi bibliografi, metadata, bahkan interaksi pengguna dengan sistem. Hal ini menunjukkan pergeseran peran data dari sekadar catatan menjadi bagian penting dari infrastruktur informasi. Perubahan ini menuntut keterampilan baru dalam pengelolaannya.

### Perbedaan data dan informasi
Menurut Elmasri & Navathe (2016), data dapat dibedakan dari informasi berdasarkan tingkat pengolahannya. Data adalah bahan mentah, sedangkan informasi adalah hasil olahan yang memiliki makna bagi pengguna. Dalam perpustakaan, daftar buku yang baru masuk adalah data, tetapi laporan tren koleksi tahunan adalah informasi. Tanpa pengolahan yang tepat, data hanya menjadi kumpulan angka atau teks tanpa makna. Inilah mengapa pemahaman konsep data menjadi langkah awal sebelum mempelajari SQL.

### Jenis-Jenis Data
Menurut Han, Kamber, & Pei (2012), data dapat diklasifikasikan menjadi data terstruktur, semi-terstruktur, dan tidak terstruktur. Data terstruktur adalah data yang disimpan dalam format tabel dengan baris dan kolom jelas, seperti daftar anggota perpustakaan. Semi-terstruktur mencakup data dengan elemen fleksibel seperti JSON atau XML, contohnya metadata katalog buku. Data tidak terstruktur meliputi dokumen teks panjang atau catatan resensi pembaca. Klasifikasi ini memengaruhi cara pengolahan data dalam sistem.

### Representasi Data dalam Kehidupan Sehari-hari
Data hadir dalam kehidupan sehari-hari dalam berbagai bentuk. Dalam perpustakaan, data tercermin pada kartu anggota, catatan peminjaman, dan katalog buku. Representasi ini dapat berupa catatan fisik maupun digital. Digitalisasi membuat data lebih mudah diakses dan dibagikan. Dengan memahami representasi, peserta dapat menghubungkan teori dengan praktik.

Barcode adalah contoh representasi data modern di perpustakaan. Setiap buku diberi barcode yang memuat informasi unik. Saat dipindai, data buku langsung tercatat dalam sistem. Ini meminimalisir kesalahan pencatatan manual. Contoh ini memperlihatkan bagaimana representasi memengaruhi akurasi data.Dengan memahami representasi data, peserta dapat lebih siap menghadapi implementasi teknis. 

### Kualitas Data
Dimensi kualitas mencakup akurasi, kelengkapan, konsistensi, dan relevansi. Dalam perpustakaan, data yang tidak akurat menyebabkan kebingungan dalam pencarian buku. Kelengkapan data menjamin setiap entri memiliki atribut penting. Dengan kualitas yang terjaga, sistem menjadi lebih bermanfaat.

* Akurasi berarti data sesuai dengan kondisi sebenarnya. 
* Kelengkapan mencegah kehilangan informasi penting.
* Konsistensi berarti data disimpan dengan format seragam
* Relevansi berarti data sesuai dengan kebutuhan pengguna

### Pentingnya Pengelolaan Data
Pengelolaan data adalah proses memastikan data tetap akurat, konsisten, dan aman dengan salah satu tujuan utama pengelolaan data adalah mendukung pengambilan keputusan. pengelolaan data juga mencakup perlindungan dari akses tidak sah dengan adanya perlindungan tersebut dapat menjaga Integritas data tetap konsisten dan valid meskipun terjadi perubahan. 

### Keterbatasan Penyimpanan manual
penyimpanan manual menggunakan buku catatan atau kartu indeks sering menimbulkan keakuratan data dan juga mudah hilang, serta menimbulkan kesulitan dalam mendukung kebutuhan organisasi besar dengan jumlah data yang terus bertambah sehingga tidak menyebabkan terjadinya data yang tumpang tindih juga terjadi duplikasi. 

Sehingga adanya dengan adanya permasalahan tersebut menegaskan perlu adanya sistem yang dapat mengintegrasikan data, yang menjadi motivasi utama dalam mengadopsi database. Karena database menawarkan cara lebih sistematis untuk mencatat, menyimpan, dan mengakses data.

### Pentingnya Akses Cepat ke Data
adanya permasalahan waktu dalam mengakses data menggunakan sistem manual, menjadi faktor pendukung adanya sistem pengelolaan data menggunakan database. 

Hal tersebut disebabkan oleh, database yang menawarkan kecepatan dan kualitas layanan dalam mengakses data, sehingga dengan kecepatan, sistem tidak hanya lebih efisien tetapi juga lebih responsif. 

### Konsistensi dan Integritas Data
Konsistensi berarti data selalu sesuai dengan aturan yang telah ditentukan. Misalnya, format tanggal harus sama pada setiap catatan. Integritas memastikan bahwa hubungan antar data tetap terjaga dengan benar. Kedua aspek ini sulit diwujudkan dalam sistem manual. 

Sistem manual rawan kehilangan integritas karena keterbatasan sumber daya manusia. Hal tersebut disebabkan oleh adanya Kesalahan penulisan atau lupa mencatat transaksi menyebabkan inkonsistensi. 

Database mengurangi masalah ini dengan validasi otomatis. database memiliki mekanisme untuk menjaga integritas. Salah satunya adalah primary key yang memastikan setiap entitas unik. Mekanisme ini menjaga konsistensi yang tidak mungkin dilakukan manual. Hal tersebut juga menegaskan bahwa integritas data mendukung kepercayaan pengguna. Jika data tidak konsisten, laporan menjadi tidak dapat dipercaya. Dengan konsistensi dan integritas, database menjadi fondasi terpercaya untuk operasional.

### Keamanan Data
Keamanan data menjadi aspek vital dalam pengelolaan database. Dengan adanya permasalahan yang ada pada sistem manual yaitu sulitnya membatasi siapa saja yang bisa mengakses data karena Catatan fisik dapat dibaca atau diubah tanpa izin. Database menyediakan mekanisme otentikasi dan otorisasi. Hal ini membuat akses data lebih terkendali.

Database memungkinkan pengaturan hak akses ini secara detail. Tanpa database, pembatasan akses hampir mustahil dilakukan. Inilah keunggulan besar dalam hal keamanan. Sehingga Keamanan menjadi alasan penting mengapa database dibutuhkan. Sistem manual tidak mampu menjamin kerahasiaan, integritas, maupun ketersediaan data.

### Efisiensi dan Penghematan Sumber Daya
Database mendukung efisiensi dengan mengurangi duplikasi dan mempercepat proses. Sedangkan Sistem manual cenderung menghasilkan catatan ganda.penghematan waktu adalah salah satu manfaat utama database karena Pencarian, penyimpanan, dan pemrosesan data dapat lebih cepat. 

efisiensi juga berarti penghematan biaya. Dengan sistem manual, organisasi membutuhkan lebih banyak staf untuk mengelola catatan. Database memungkinkan otomatisasi sehingga tenaga kerja bisa dialihkan ke tugas lain. Selain itu juga database mendukung pemrosesan data skala besar. Sistem manual tidak mungkin mengelola ribuan transaksi harian. Database juga mampu melakukannya dengan cepat dan akurat. Sehingga membuat database menjadi investasi yang berharga.

### Skalabilitas dan Adaptabilitas
Skalabilitas berarti kemampuan sistem menangani pertumbuhan data Sedangkan adaptabilitas adalah kemampuan menyesuaikan dengan kebutuhan baru. 

skalabilitas penting dalam organisasi modern. Pertumbuhan data tidak bisa dihindari di era digital. Database memungkinkan organisasi tetap efisien meskipun data berlipat ganda. selain itu menambahkan database relasional juga dapat mendukung integrasi dengan aplikasi lain. 

Skalabilitas dan integrasi membuat database lebih fleksibel. Fleksibilitas ini tidak dimiliki sistem manual. Sehingga Dengan skalabilitas, database tidak hanya relevan untuk saat ini tetapi juga masa depan.
 
### Dampak Database pada Perpustakaan
Database membawa perubahan besar dalam manajemen perpustakaan, diantaranya adalah :
* Pencatatan manual digantikan dengan sistem digital
* Anggota dapat mencari buku dengan mudah melalui katalog online.
* Peminjaman dan pengembalian dicatat otomatis dalam database
Sehingga, dengan adanya perubahan tersebut dapat meningkatkan kualitas layanan kepada para pemustaka.

## DBMS vs File Biasa
File biasa adalah metode penyimpanan data tradisional menggunakan sistem file di komputer. Data disimpan dalam bentuk teks atau spreadsheet tanpa aturan relasional yang ketat. Dalam perpustakaan, file biasa bisa berupa daftar anggota dalam dokumen Excel. Sistem ini mudah dibuat tetapi tidak efisien ketika data semakin banyak. Kekurangannya akan terlihat saat organisasi berkembang.

Database Management System (DBMS) adalah perangkat lunak yang dirancang untuk mengelola data secara sistematis. DBMS memungkinkan penyimpanan, pengolahan, dan pengaksesan data dengan lebih efisien. Dalam perpustakaan, DBMS digunakan untuk mencatat anggota, koleksi buku, dan transaksi peminjaman. Semua data terintegrasi dalam satu sistem yang terstruktur. Sehingga DBMS menjadi solusi atas kelemahan file biasa.

### Perbedaan Struktural File vs DBMS
File biasa menyimpan data dalam bentuk datar tanpa relasi. Sebalikstruktur DBMS lebih fleksibel. Perubahan atribut dapat dilakukan tanpa mengganggu keseluruhan sistem. Dalam file biasa, menambah kolom baru seringkali memerlukan modifikasi besar. Hal ini membuat file biasa kurang adaptif. DBMS menggunakan model relasional. Model ini menyederhanakan hubungan antar data dengan konsep tabel. Misalnya, tabel anggota, tabel buku, dan tabel peminjaman dapat saling terhubung. File biasa tidak mampu merepresentasikan hubungan ini secara alami. Relasi menjadi kekuatan utama DBMS. DBMS mendukung normalisasi data. Normalisasi mengurangi redundansi dan meningkatkan konsistensi. Dalam file biasa, redundansi sulit dihindari karena data disimpan berulang-ulang. Normalisasi membuat database lebih efisien.

Perbedaan operasional menunjukkan mengapa DBMS lebih unggul. File biasa sederhana tetapi terbatas. DBMS mendukung operasi kompleks, aman, dan efisien.

### Efisiensi Penyimpanan
selanjutnya efisiensi penyimpanan yang berdampak pada kecepatan akses file dengan redudansi besar membutuhkan waktu yang lebih lama untuk diproses sehingga dbms dapat mengurangi beban ini dengan adanya struktur yang terorganisasi. sehingga keunggulan adanya dbms yang menggunakan sistem normalisasi dapat mengurangi redudansi dan juga dapat mendukung adanya indexing yang mempercepat pencarian data tanpa perlu membaca seluruh tabel. sedangkan file biasa tidak memiliki mekanisme serupa. adanya efisiensi penyimpanan pula berdampak pada biaya penyimpanan karena dbms dapat menghemat ruang sehingga lebih ekonomis. efisiensi penyimpanan juga menegaskan keunggulan dbms dibanding file biasa yang menjadi boros seiring pertumbuhan data. sehingga DBMS tetap efisien meskipun data semakin banyak.

### Keamanan dan Pemeliharaan
Perbandingan DBMS dengan File biasa adalah sebagai berikut :
* DBMS memiliki fitur audit trail yang memungkinkan setiap perubahan data dapat dilacak, sedangkan file biasa tidak mendukung hal tersebut.
* DBMS menyediakan kontrol akses berbasis peran (role-based access control), sehingga hak admin dan anggota berbeda, sementara file biasa tidak memiliki pengaturan hak akses.
* DBMS mendukung mekanisme backup dan recovery otomatis, memungkinkan pemulihan data dengan cepat jika terjadi kerusakan, sedangkan file biasa hanya bergantung pada salinan manual yang rawan kehilangan data.
* DBMS memiliki alat administrasi untuk pemeliharaan sistematis, sehingga pengaturan dan pengelolaan data lebih mudah dilakukan, sedangkan file biasa memerlukan intervensi manual yang rawan kesalahan.
* DBMS lebih andal dalam menjamin keamanan, akuntabilitas, dan ketahanan data, sedangkan file biasa tidak mampu memberikan perlindungan setara.
* Dalam konteks perpustakaan, penggunaan DBMS memastikan data anggota, koleksi, dan transaksi lebih aman, dapat dilacak, serta mudah dikelola dibandingkan sistem berbasis file biasa.

### Studi Kasus Perpustakaan
Penggunaan DBMS memungkinkan perubahan pengelolaan data yang ada di perpustakaan, diantaranya adalah :
Bayangkan perpustakaan kecil yang awalnya menggunakan file Excel untuk mencatat peminjaman. Data sering ganda dan sulit dicari. Pengelola kesulitan menghasilkan laporan bulanan. Setelah beralih ke DBMS, semua catatan terintegrasi. Proses pencarian dan pelaporan menjadi instan.

DBMS membantu organisasi beradaptasi dengan pertumbuhan. Perpustakaan dengan ribuan anggota tetap dapat dikelola efisien. Sistem file biasa tidak sanggup menghadapi skala besar. DBMS menjadi solusi jangka panjang. Hal ini membuktikan keunggulan nyata DBMS.DBMS meningkatkan konsistensi data. Dalam perpustakaan, setiap peminjaman terkait langsung dengan anggota dan buku. Tidak ada lagi duplikasi atau data hilang. Konsistensi membuat laporan lebih terpercaya. Database menjadi sumber kebenaran tunggal.

DBMS mempercepat pelayanan. Anggota dapat mengetahui ketersediaan buku secara real-time. Staf tidak lagi perlu membuka file manual. Layanan menjadi lebih cepat dan akurat. Hal ini meningkatkan kepuasan anggota.

Studi kasus ini menunjukkan perbedaan nyata file biasa dan DBMS. File biasa sederhana tetapi tidak efisien. DBMS lebih kompleks tetapi mendukung integritas, keamanan, dan efisiensi.

## Pengenalan MariaDB bagi Pemula
MariaDB merupakan turunan dari MySQL yang lahir setelah akuisisi MySQL oleh Oracle. Kekhawatiran akan hilangnya sifat open-source mendorong Monty Widenius, salah satu pencipta MySQL, untuk mengembangkan MariaDB. Nama MariaDB diambil dari nama anaknya, Maria. Seiring waktu, MariaDB berkembang pesat menjadi alternatif populer bagi MySQL.

Salah satu keunggulan utama MariaDB sebagai solusi database berkelanjutan adalah MariaDB tetap mempertahankan kompatibilitas penuh dengan MySQL, sehingga organisasi dapat bermigrasi tanpa banyak perubahan. Hal ini memudahkan perpustakaan yang sebelumnya menggunakan MySQL untuk beralih ke MariaDB secara mudah dan efisien. 

Kekuatan MariaDB terletak pada komunitas global yang aktif berkontribusi terhadap pengembangan fitur dan perbaikan sistem. Dukungan komunitas yang luas menjadikan MariaDB lebih dinamis dan inovatif dibandingkan produk komersial tertutup. Selain itu, MariaDB memiliki fleksibilitas tinggi karena dapat dijalankan di berbagai platform seperti Windows, Linux, maupun server cloud.

### Fitur Utama MariaDB
fitur utama Maria DB menawarkan banyak fitur unggulan untuk pemula maupun profesional diantaranya adalah :
* dukungan penuh terhadap SQL standar dengan SQL pengguna dapat menulis query universal yang dipahami di banyak dbms sehingga memudahkan pembuatan laporan dan standarisasi pembuat Maria DB lebih mudah dipelajari.
* Maria DB menyediakan engine penyimpanan fleksibel seperti innoDB yang mendukung transaksi dengan jaminan ACID sehingga dengan fitur tersebut dbms modern seperti MariaDB dapat lebih unggul karena adanya stabilitas transaksi.
* MariaDB juga memiliki kemampuan replikasi yang memungkinkan salinan database di server lain sebagai backup sehingga fitur ini memastikan layanan tetap berjalan meski server utama bermasalah yang meningkatkan keandalan sistem sehingga replikasi menjadi keunggulan penting bagi adanya ketersediaan data.
* MariaDB juga mendukung keamanan canggih melalui sistem autentikasi, otorisasi dan enkripsi yang memperkuat perlindungan data. fitur ini sangat penting di era digital yang rawan kebocoran data sehingga keamanan menjadi pilar utama kepercayaan pengguna.

sehingga dengan fitur-fitur tadi MariaDB tampil sebagai dbms modern yang kuat, fleksibilitas, berstandar SQL, replikasi dan keamanan yang membuatnya ideal untuk organisasi terutama perpustakaan.

### Perbedaan MariaDB dengan MySQL, Serta Keunggulannya
* lisensi open source yang benar-benar bebas my SQL meski open source dikendalikan oleh Oracle sedangkan mariaDB bebas dari kendali perusahaan hal tersebut memberikan fleksibilitas yang lebih luas kepada MariaDB
* MariaDB sering lebih cepat dalam merilis fitur baru karena dengan adanya komunitas aktif memastikan inovasi berkelanjutan seperti engine Aria dan ColumnStore merupakan keunggulan mariaDB dengan adanya fitur tersebut dapat memperluas kemampuan analisis data 
* memiliki optimasi query lebih baik dengan beberapa benchMark menunjukkan performa MariaDB unggul dibanding MySQL dengan adanya performa yang baik memastikan layanan tetap lancar sehingga optimalisasi menjadi daya tarik penting bagi MariaDB
* MariaDB lebih transparan dalam pengembangan dengan adanya semua pembaruan yang dapat diakses publik dan juga didukung oleh adanya komunitas yang dapat mengusulkan perbaikan atau fitur baru menjadikan transparansi Maria DB berbeda dengan pengembangan MySQL sehingga menjadikan MariaDB lebih inklusif.

## Penggunaan Database
Penggunaan Database, dapat kita temui dengan mudah dalam kehidupan sehari-hari contoh mudahnya ada pada aplikasi-aplikasi yang kerap kita gunakan yaitu Media Sosial, Perbankan, E-Commerce. Media sosial menyimpan profil pengguna, daftar teman, dan riwayat interaksi. Perbankan digital mengandalkan database untuk mencatat saldo, transaksi, dan pinjaman. E-commerce menggunakan database untuk menyimpan daftar produk, stok, dan pesanan pelanggan. Semua layanan ini tidak mungkin berjalan tanpa database yang kuat.

Selain itu Pendidikan adalah salah satu sektor yang paling banyak memanfaatkan database. Sistem akademik menggunakan database untuk menyimpan nilai, jadwal, dan informasi mahasiswa. E-learning platform menyimpan data materi, aktivitas, dan hasil ujian. 

Kemudian, penggunaan Database juga dapat kita temui pada sektor pemerintahan, perpustakaan, dll. Sehingga Kesimpulannya adalah potensi database melampaui sekadar penyimpanan data. Ia adalah motor penggerak inovasi di berbagai sektor. 
