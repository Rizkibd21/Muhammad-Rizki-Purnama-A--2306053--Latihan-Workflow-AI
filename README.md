Cara menjalankan kode dan penjelasannya :
1. Membuat Data Penjualan dan Menyimpannya ke CSV
Kode berikut digunakan untuk membuat dataset sederhana dengan informasi produk yang dijual, jumlah terjual, stok, dan harga satuan.
Fungsi Kode:
-Membuat dataset dalam bentuk dictionary.
-Menyimpan dataset ke dalam DataFrame menggunakan pandas.
-Menyimpan DataFrame ke file CSV agar bisa digunakan dalam analisis berikutnya.

2. Membaca Data dari CSV
Fungsi Kode:
-Membaca kembali file CSV yang telah dibuat.
-Menampilkan 5 baris pertama data menggunakan .head().

3. Data Cleaning dan Penambahan Kolom Baru
Fungsi Kode:
-Mengecek apakah ada nilai kosong (missing values) dalam dataset.
-Mengubah kolom "Tanggal" menjadi format datetime untuk memudahkan analisis waktu.
-Menambahkan kolom "Total Penjualan" yang dihitung dari (Jumlah Terjual × Harga Satuan).
-Menambahkan kolom "Keuntungan", yang menghitung laba dengan asumsi harga modal per unit adalah 10.000.

4. Model Machine Learning (Decision Tree) untuk Prediksi Restock Produk
Fungsi Kode:
-Menggunakan fitur "Jumlah Terjual" dan "Stok" sebagai variabel input (X).
-Variabel target (y) dibuat berdasarkan apakah stok produk kurang dari 5 (1 = perlu restock, 0 = tidak perlu).
-Membagi data menjadi training set (80%) dan testing set (20%).
-Melatih model Decision Tree Classifier untuk memprediksi apakah stok perlu diisi ulang.
-Mengevaluasi akurasi model.

5. Prediksi Restock Produk Baru
Fungsi Kode:
-Menggunakan model yang sudah dilatih untuk memprediksi apakah produk baru dengan Jumlah Terjual = 8 dan Stok = 3 perlu diisi ulang atau tidak.
-Jika prediksi menunjukkan stok < 5, maka produk dianggap perlu di-restock.

Notebook ini membahas analisis data penjualan dengan fokus pada prediksi kebutuhan restock produk
menggunakan model Decision Tree Classifier. Data awal dibuat dan disimpan dalam format CSV, lalu
diproses dengan menambahkan kolom Total Penjualan dan Keuntungan. Model machine learning
dilatih menggunakan fitur Jumlah Terjual dan Stok, dengan target klasifikasi apakah stok perlu diisi
ulang atau tidak. Setelah evaluasi, model digunakan untuk memprediksi kebutuhan restock produk baru.
Pendekatan ini dapat membantu dalam manajemen inventaris dan pengambilan keputusan terkait stok barang.

