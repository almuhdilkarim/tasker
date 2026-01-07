# **Pemanfaatan AI untuk Normalisasi Database hingga Bentuk Normal ke-3 (1NF, 2NF, 3NF)**

### **Pendahuluan**

Normalisasi database adalah proses untuk menyusun data dalam sebuah basis data agar lebih efisien, bebas dari redundansi (pengulangan data), dan menjaga integritas data. Biasanya normalisasi dilakukan secara manual, tapi sekarang dengan bantuan **AI (Artificial Intelligence)**, proses ini bisa menjadi **lebih cepat, akurat, dan otomatis**.

Artikel ini akan membahas langkah-langkah praktis menggunakan AI untuk membantu proses normalisasi database hingga bentuk normal ke-3 (1NF, 2NF, dan 3NF).

---

## **Apa Itu Normalisasi Database? Singkatnya…**

* **1NF (First Normal Form):** Tidak ada data yang berulang atau array dalam satu kolom.
* **2NF (Second Normal Form):** Sudah 1NF + semua atribut non-kunci bergantung sepenuhnya pada primary key.
* **3NF (Third Normal Form):** Sudah 2NF + tidak ada ketergantungan transitif (atribut non-kunci tidak boleh bergantung ke atribut non-kunci lainnya).

---

## **Langkah-Langkah Praktis Menggunakan AI untuk Normalisasi Database**

### **Langkah 1: Siapkan Data Awal dalam Bentuk Tabel Flat (Non-Normalisasi)**

Buat file dataset (misalnya Excel atau CSV) yang berisi data awal. Contoh:

| ID | Nama Pelanggan | Produk | Kategori Produk | Harga   | Kota     | Provinsi   |
| -- | -------------- | ------ | --------------- | ------- | -------- | ---------- |
| 1  | Amel           | Laptop | Elektronik      | 7000000 | Surabaya | Jawa Timur |
| 2  | Arya           | HP     | Elektronik      | 3000000 | Surabaya | Jawa Timur |
| 3  | Dewi           | Meja   | Furniture       | 1500000 | Surabaya | Jawa Timur |

### **Langkah 2: Gunakan AI untuk Analisis Struktur Data**

Bisa menggunakan alat berbasis AI seperti:

* **ChatGPT (seperti ini)**
* **AutoML tools** seperti Google AutoML atau Azure ML
* **Python + AI Model sederhana** (dengan Pandas + LLM API)

Contoh jika menggunakan ChatGPT:

```plaintext
Prompt: "Berikut data pelanggan dan transaksi. Tolong bantu saya normalisasi data ini ke 1NF, 2NF, dan 3NF."
```

>  AI akan menganalisis kolom mana yang berulang, mana yang redundant, dan memberikan saran struktur tabel.

---

### **Langkah 3: Normalisasi ke 1NF (First Normal Form)**

###  Tujuan:

Hilangkan data yang berulang, pecah kolom yang memiliki multiple value menjadi baris terpisah.

### Output AI untuk 1NF:

Pisahkan data menjadi satu baris satu entitas. Contoh:

| ID | Nama Pelanggan | Produk | Kategori Produk | Harga   | Kota     | Provinsi   |
| -- | -------------- | ------ | --------------- | ------- | -------- | ---------- |
| 1  | Amel           | Laptop | Elektronik      | 7000000 | Surabaya | Jawa Timur |
| 3  | Dewi           | Meja   | Furniture       | 1500000 | Surabaya | Jawa Timur |

Semua data sudah atomic (1 data per kolom), tidak ada array atau list.

---

## **Langkah 4: Normalisasi ke 2NF (Second Normal Form)**

### Tujuan:

Pastikan semua kolom non-kunci bergantung **sepenuhnya** pada primary key.

### Strategi:

* Pisahkan tabel `Pelanggan`
* Pisahkan tabel `Produk`

### Output AI untuk 2NF:

**Tabel Pelanggan**

| ID_Pelanggan | Nama | Kota     | Provinsi   |
| ------------ | ---- | -------- | ---------- |
| 1            | Amel | Surabaya | Jawa Timur |
| 2            | Arya | Surabaya | Jawa Timur |

**Tabel Produk**

| ID_Produk | Nama Produk | Kategori   | Harga   |
| --------- | ----------- | ---------- | ------- |
| P1        | Laptop      | Elektronik | 7000000 |
| P2        | HP          | Elektronik | 3000000 |
| P3        | Meja        | Furniture  | 1500000 |

**Tabel Transaksi**

| ID_Transaksi | ID_Pelanggan | ID_Produk |
| ------------ | ------------ | --------- |
| T1           | 1            | P1        |
| T2           | 2            | P2        |
| T3           | 1            | P3        |

---

## **Langkah 5: Normalisasi ke 3NF (Third Normal Form)**

### Tujuan:

Hilangkan **ketergantungan transitif**, yaitu atribut non-kunci tergantung pada atribut non-kunci lain.

### Analisis:

* Dalam tabel **Pelanggan**, kolom **Kota** dan **Provinsi** berhubungan. Maka pisahkan jadi tabel sendiri.

### Output AI untuk 3NF:

**Tabel Wilayah**

| ID_Kota | Kota     | Provinsi   |
| ------- | -------- | ---------- |
| K1      | Surabaya | Jawa Timur |

**Tabel Pelanggan (Update)**

| ID_Pelanggan | Nama | ID_Kota |
| ------------ | ---- | ------- |
| 1            | Amel | K1      |
| 2            | Arya | K1      |

---

## **Kesimpulan**

Dengan bantuan AI, proses normalisasi bisa dilakukan secara:

* **Otomatis dan cepat**
* **Lebih akurat** karena AI mampu melihat pola-pola ketergantungan data
* **Efisien**, terutama untuk dataset besar

---

## **Tools dan Teknologi yang Bisa Digunakan**

| Tools AI        | Kegunaan                                  |
| --------------- | ----------------------------------------- |
| ChatGPT         | Analisis struktur data, bantu normalisasi |
| Google AutoML   | Machine learning pipeline data            |
| Python + Pandas | Olah data dan integrasi dengan AI         |
| dbdiagram.io    | Visualisasi ERD setelah normalisasi       |

### Bukti Kehadiran Seminar_Ira Khairina 3B
![IMG_20251001_151735](https://github.com/user-attachments/assets/05651326-c4ba-4c8e-9f29-db3b251b0e75)

![IMG_20251001_134401](https://github.com/user-attachments/assets/219d637f-8254-4d3f-98ee-f6778c41a10b)
