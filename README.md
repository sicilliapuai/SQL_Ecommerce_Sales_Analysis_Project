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
-   **`Products`**: Informasi detail produk (ID, nama, kategori, harga, stok).
-   **`Customers`**: Data pelanggan (ID, nama, email, kota).
-   **`Orders`**: Ringkasan pesanan (ID pesanan, ID pelanggan, tanggal, total jumlah).
-   **`Order_Items`**: Detail setiap item dalam pesanan (ID item, ID pesanan, ID produk, kuantitas, harga saat dibeli).

Berikut adalah representasi skema database:
*(Jika kamu bisa membuat ERD sederhana (Entity-Relationship Diagram) menggunakan alat seperti [draw.io](https://draw.io/) atau [Lucidchart](https://www.lucidchart.com/), sisipkan gambarnya di sini. Jika tidak, cukup jelaskan seperti di atas sudah bagus.)*

---

## Data

Data yang digunakan dalam proyek ini adalah data buatan (simulasi) yang sengaja dirancang untuk mencerminkan skenario penjualan e-commerce. Berikut adalah contoh sebagian kecil data dari setiap tabel:

**`Products`**
| product_id | product_name | category   | price  | stock_quantity |
|------------|--------------|------------|--------|----------------|
| 1          | Laptop       | Elektronik | 1200.00| 50             |
| 2          | Mouse        | Elektronik | 25.00  | 200            |
| ...        | ...          | ...        | ...    | ...            |

**`Customers`**
| customer_id | customer_name | email          | city    |
|-------------|---------------|----------------|---------|
| 101         | Budi Santoso  | budi@example.com| Jakarta |
| 102         | Ani Wijaya    | ani@example.com| Bandung |
| ...         | ...          | ...            | ...     |

*(Lanjutkan dengan contoh data untuk `Orders` dan `Order_Items` juga)*

---

## Pertanyaan Analitis & Insight

Berikut adalah pertanyaan bisnis yang dijawab menggunakan SQL, beserta `query` yang digunakan dan `insight` yang diperoleh:

### 1. Produk Terlaris Berdasarkan Kuantitas Terjual
* **Pertanyaan:** Produk apa yang paling banyak terjual dalam hal jumlah unit?
* **Query SQL:**
    ```sql
    -- Tulis query di sini, sama seperti yang di file .sql kamu
    SELECT
        p.product_name,
        SUM(oi.quantity) AS total_quantity_sold
    FROM
        Products p
    JOIN
        Order_Items oi ON p.product_id = oi.product_id
    GROUP BY
        p.product_name
    ORDER BY
        total_quantity_sold DESC
    LIMIT 5;
    ```
* **Hasil & Insight:** (Tuliskan hasil singkat yang kamu dapatkan, contoh: "Hasil menunjukkan 'Laptop' adalah produk terlaris dengan 1 unit terjual, diikuti 'Mouse' dengan 2 unit. Ini mengindikasikan Laptop adalah produk dengan nilai tinggi yang diminati, sementara Mouse adalah aksesori yang populer.")

### 2. Total Pendapatan per Kategori Produk
* **Pertanyaan:** Berapa total pendapatan yang dihasilkan oleh setiap kategori produk?
* **Query SQL:**
    ```sql
    -- Tulis query di sini
    ```
* **Hasil & Insight:** (Jelaskan hasil dan insight dari query ini)

### 3. Pelanggan dengan Pembelian Terbanyak
* **Pertanyaan:** Siapa 5 pelanggan teratas berdasarkan total uang yang mereka belanjakan?
* **Query SQL:**
    ```sql
    -- Tulis query di sini
    ```
* **Hasil & Insight:** (Jelaskan hasil dan insight dari query ini)

### 4. Rata-rata Nilai Order
* **Pertanyaan:** Berapa rata-rata nilai total dari setiap pesanan?
* **Query SQL:**
    ```sql
    -- Tulis query di sini
    ```
* **Hasil & Insight:** (Jelaskan hasil dan insight dari query ini)

### 5. Pendapatan Bulanan
* **Pertanyaan:** Bagaimana tren pendapatan dari bulan ke bulan?
* **Query SQL:**
    ```sql
    -- Tulis query di sini
    ```
* **Hasil & Insight:** (Jelaskan hasil dan insight dari query ini)

### 6. Produk dengan Stok Rendah (Kurang dari 100 unit)
* **Pertanyaan:** Produk mana yang stoknya di bawah 100 unit dan perlu diisi ulang?
* **Query SQL:**
    ```sql
    -- Tulis query di sini
    ```
* **Hasil & Insight:** (Jelaskan hasil dan insight dari query ini)

---

## Kesimpulan & Pembelajaran

Proyek ini telah berhasil mendemonstrasikan kemampuan dalam:
* Merancang dan mengimplementasikan skema database relasional.
* Mengisi dan memanipulasi data menggunakan perintah DDL dan DML dasar SQL.
* Melakukan analisis data untuk menjawab pertanyaan bisnis menggunakan berbagai fungsi dan klausa SQL (JOIN, GROUP BY, Aggregate Functions, WHERE, ORDER BY, DATE_FORMAT).
* Menginterpretasikan hasil query dan mengubahnya menjadi insight yang berarti.

Analisis ini memberikan pemahaman awal tentang pola penjualan, performa produk, dan perilaku pelanggan yang dapat digunakan untuk pengambilan keputusan bisnis yang lebih baik.

---
