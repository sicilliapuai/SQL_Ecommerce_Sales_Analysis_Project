# Proyek Portofolio SQL: Analisis Penjualan E-commerce Sederhana

---

## Gambaran Umum Proyek

Proyek ini adalah analisis data penjualan e-commerce sederhana yang dibangun dari nol menggunakan SQL. Tujuannya adalah untuk menunjukkan kemampuan dalam merancang skema database, memanipulasi data, dan mengekstraksi insight bisnis dari data transaksional.

---

## Teknologi yang Digunakan

* **SQL** (MySQL/MariaDB via XAMPP)
* **GitHub** (untuk dokumentasi dan hosting proyek)

---

## Desain Database (Skema)

Database ini terdiri dari 4 tabel yang saling berhubungan:
-   **'Products'** : informasi detail produk (ID, nama, kategori, harga, stok).
-   **'Customers'** : data pelanggan (ID, nama, email, kota).
-   **'Orders'** : ringkasan pesanan (ID pesanan, ID pelanggan, tanggal, total jumlah).
-   **'Order_Items'** : detail setiap item dalam pesanan (ID item, ID pesanan, ID produk, kuantitas, harga saat dibeli).

---

##Data

Data yang digunakan dalam proyek ini adalah data buatan (simulasi) yang sengaja dirancang untuk mencerminkan skenario penjualan e-commerce. Berikut adalah contoh sebagian kecil data dari setiap tabel:

**'Products'**
