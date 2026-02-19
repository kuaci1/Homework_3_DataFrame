# Homework 3 – DataFrame Solutions
## Data Science Batch 57

Repositori ini berisi solusi untuk tugas analisis data menggunakan Python dan library Pandas. Fokus utama tugas ini adalah pembersihan data, manipulasi kolom, dan ekstraksi wawasan bisnis dari dataset transaksi. dan ini salah satu tugas HW_3 dalam bothcamp di DigitalSkola
# Ringkasan Hasil (Summary of Results)

# Task 1: Kolom Nama Lengkap
* **Deskripsi:** Membuat kolom baru "Full Name" yang menggabungkan First Name dan Last Name.
* **Posisi:** Disisipkan setelah kolom "Last Name".
* **Format:** Menggunakan format Title Case (Contoh: "Elvride Aries").

# Task 2: Perhitungan GMV
* **Rumus:** `GMV = Transaction Amount - Seller Discount + Delivery Fee`.
* **Hasil:** Total GMV di seluruh transaksi adalah **Rp 2.714.593.600,00**.

# Task 3: Pengelompokan Kategori & Tabel Pivot
Data dikelompokkan menjadi dua grup kategori utama untuk melihat tren bulanan:
* **Group 1:** Fashion, Babies/ Kids, Beauty/ Health.
* **Group 2:** Service/ Mokado, Gadget/ Komputer.

# Tabel Pivot - Total GMV per Bulan:

| Year-Month | Group 1 | Group 2 | Total |
|------------|--------------|----------------|----------------|
| 2017-07 | 83,916,600 | 194,045,200 | 277,961,800 |
| 2017-08 | 59,189,600 | 341,657,100 | 400,846,700 |
| 2017-09 | 198,279,800 | 156.506.600 | 354,786,400 |
| 2017-10 | 92,012,400 | 135,405,000 | 227,417,400 |
| 2017-11 | 221,708,700 | 300,590,900 | 522,299,600 |
| 2017-12 | 89,257,800 | 435,267,100 | 524,524,900 |

# Task 4 & 5: Analisis Seller Terbaik
* **Seller dengan GMV Tertinggi (Agustus 2017):** Petrus Sinda (Rp 18.500.000,00).
* **Seller dengan Transaksi Terbanyak (Fashion - Sept 2017):** A.Indraputra Wahyu.
  * *Catatan: Jika terdapat jumlah transaksi yang sama, sistem memilih urutan alfabet pertama*.

# Implementasi Kode Python
### Fungsi Utama yang Digunakan:
* `pd.read_csv()` – Memuat data.
* `.str.title()` – Mengonversi teks menjadi format title case.
* `pd.to_datetime()` – Mengonversi string tanggal menjadi objek datetime.
* `.pivot_table()` – Membuat tabel ringkasan data.
* `.groupby()` – Mengelompokkan data berdasarkan kriteria tertentu.
* `.sort_values()` – Mengurutkan hasil data.

### Langkah Pembersihan Data:
1. Menghapus karakter koma pada kolom numerik.
2. Mengonversi angka bertipe string ke tipe data *float*.
3. Membuat objek datetime yang tepat untuk analisis.
4. Menangani nilai kosong atau *null values* secara tepat.

## Instruksi Penggunaan (Submission)
1. Unggah Jupyter notebook ke **Google Colab**.
2. Unggah file CSV (`Paid-Transaction.csv` dan `Seller.csv`) ke Colab.
3. Perbarui jalur file (*file paths*) di dalam notebook jika diperlukan.
4. Jalankan semua sel (*Run All*) untuk memverifikasi hasil.
5. Atur izin berbagi menjadi **"Anyone with the link can view"**.
