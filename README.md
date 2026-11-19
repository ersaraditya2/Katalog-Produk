# Katalog Produk - Aplikasi Manajemen Katalog Toko

Aplikasi manajemen katalog produk berbasis *desktop* menggunakan **JavaFX** dan **JDBC**.

## Deskripsi

**Katalog Produk** adalah aplikasi pengelolaan katalog produk toko yang terhubung ke database relasional melalui JDBC. Pengguna dapat menambahkan produk baru (nama, harga, dan pilihan foto), mengedit data produk yang sudah ada, menghapus produk dengan dialog konfirmasi, serta melihat daftar katalog dalam bentuk kartu visual (`TilePane`) beserta informasi jumlah produk secara *real-time*.

## Tampilan Aplikasi
Berikut adalah contoh tampilan antarmuka katalog produk:

### 1. Tampilan Form & Katalog
<p align="center">
  <img src="SS/Katalog-produk.png" alt="Form Input dan Kartu Katalog Produk" width="400">
</p>

### 2. Konfirmasi Hapus Produk
<p align="center">
  <img src="SS/Konfirmasi-hapus.png" alt="Dialog Konfirmasi Hapus Produk" width="400">
</p>

## Fitur Utama

- **Tambah & Edit Produk (`saveProduct`)**: Menambah produk baru (`add`) atau memperbarui produk terpilih (`update`) langsung dari form input.
- **Hapus Produk (`hapusProduk`)**: Menghapus data produk berdasarkan `id` melalui repository setelah konfirmasi pengguna.
- **Katalog Kartu Visual (`showData`)**: Menampilkan foto (`roti.png`, `susu.png`, `kopi.png`), nama, harga, dan ID produk dalam `TilePane` serta memperbarui total jumlah produk.
- **Akses Database Terstruktur (`PreparedStatement`)**: Memisahkan logika query SQL pada `ProdukRepository` dan koneksi pada `Database`.

## Teknologi

- **Java**
- **JavaFX** & **FXML**
- **JDBC**
- **Maven**
- **IDE**: NetBeans

## Struktur Proyek

```text
KatalogProduk/
├── pom.xml
├── README.md
├── SS/
│   ├── Katalog-produk.png
│   └── Konfirmasi-hapus.png
└── src/
    └── main/
        ├── java/
        │   ├── controller/
        │   │   └── KatalogController.java
        │   ├── data/
        │   │   └── ProdukRepository.java
        │   ├── db/
        │   │   └── Database.java
        │   ├── main/
        │   │   └── MainApp.java
        │   └── model/
        │       └── Produk.java
        └── resources/
            ├── image/
            │   ├── kopi.png
            │   ├── roti.png
            │   └── susu.png
            ├── view/
            │   └── katalog.fxml
            └── view/styles/
                └── app.css
```

## Persyaratan

- JDK 26 atau versi yang kompatibel dengan konfigurasi proyek.
- Maven.
- JavaFX yang dikelola melalui dependensi Maven.

## Cara Menjalankan

1. Clone repositori.
2. Buka folder proyek di NetBeans atau IDE yang mendukung Maven.
3. Pastikan JDK yang digunakan sesuai dengan konfigurasi proyek.
4. Tunggu Maven mengunduh dependensi yang diperlukan.
5. Jalankan aplikasi menggunakan Maven

## Lisensi

Belum ditentukan.
