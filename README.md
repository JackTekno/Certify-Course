# Certify-Course

CertifyCourse (Course Education Recognition Tool for Issuing and Facilitating Your Complete Online Universal Reliable Secure E-certificates) adalah Plugin WordPress untuk membuat, mengelola, dan memvalidasi sertifikat course dengan QR code yang aman.

## Daftar Isi
- [Demo](#demo)
- [Deskripsi](#deskripsi)
- [Fitur](#fitur)
- [Instalasi](#instalasi)
- [Penggunaan](#penggunaan)
  - [Membuat Sertifikat Individual](#membuat-sertifikat-individual)
  - [Bulk Generate Sertifikat](#bulk-generate-sertifikat)
  - [Validasi Sertifikat](#validasi-sertifikat)
  - [Mengelola Sertifikat](#mengelola-sertifikat)
- [Fitur Keamanan](#fitur-keamanan)
- [Styling Kustom](#styling-kustom)
- [Struktur Database](#struktur-database)
- [Persyaratan](#persyaratan)
- [Dukungan](#dukungan)
- [Kredit](#kredit)
- [Riwayat Versi](#riwayat-versi)
- [Versi Akan Datang](#versi-akan-datang)
- [Lisensi](#lisensi)
- [Screenshot](#screenshot)

## Demo

Silahkan kunjungi link [siberin.id/validate-certificate/](https://siberin.id/validate-certificate/) dan masukkan kode unik: `SIBERIN7b2fac0840a0012d04ccbab313e751d6`
atau bisa langsung melalui link berikut ini [siberin.id/validate-certificate/?code=SIBERIN7b2fac0840a0012d04ccbab313e751d6](https://siberin.id/validate-certificate/?code=SIBERIN7b2fac0840a0012d04ccbab313e751) (kode unik akan otomatis disubmit).

## Deskripsi

Sistem Sertifikat Course adalah plugin WordPress komprehensif yang dirancang untuk membantu platform pendidikan, penyedia kursus, dan organisasi pelatihan dalam membuat dan mengelola sertifikat digital untuk siswa mereka. Plugin ini menyediakan sistem validasi yang aman menggunakan kode unik dan QR code, memungkinkan siapa saja untuk memverifikasi keaslian sertifikat.

## Fitur

- **Pembuatan Sertifikat**: Menghasilkan sertifikat individu dengan kode keamanan unik
- **Bulk Generate Sertifikat**: Membuat beberapa sertifikat sekaligus menggunakan unggahan CSV
- **Validasi Sertifikat**: Halaman publik untuk memverifikasi keaslian sertifikat
- **Integrasi QR Code**: QR code yang dibuat otomatis untuk validasi sertifikat yang mudah
- **Filter Course**: Mengorganisir dan memfilter sertifikat berdasarkan nama course
- **Ekspor Data**: Mengekspor data sertifikat ke format CSV
- **Validasi Aman**: Rate limiting untuk mencegah serangan brute force
- **Responsif Mobile**: Antarmuka yang user-friendly di semua perangkat

## Instalasi

1. Unggah folder `sistem-sertifikat-course` ke direktori `/wp-content/plugins/`
2. Aktifkan plugin melalui menu 'Plugins' di WordPress
3. Akses sistem manajemen sertifikat dari menu 'Sertifikat' di dashboard admin

## Penggunaan

### Membuat Sertifikat Individual

1. Navigasikan ke 'Sertifikat' > 'Buat Sertifikat' di admin WordPress
2. Isi detail sertifikat:
   - Tanggal penyelesaian
   - Nama peserta
   - Nama course
3. Klik 'Buat Sertifikat' untuk menghasilkan sertifikat
4. Sistem akan secara otomatis menghasilkan kode keamanan unik dan QR code

### Bulk Generate Sertifikat

1. Navigasikan ke 'Sertifikat' > 'Bulk Generate' di admin WordPress
2. Unduh template CSV sampel
3. Isi detail peserta dalam format CSV:
   - Kolom pertama: Nama peserta
   - Kolom kedua: Nama course
   - Kolom ketiga: Tanggal (format YYYY-MM-DD)
4. Unggah file CSV yang sudah diisi
5. Klik 'Generate Sertifikat' untuk membuat semua sertifikat
6. Unduh hasil CSV yang mencakup semua kode unik dan URL QR code

### Validasi Sertifikat

Plugin ini secara otomatis membuat halaman validasi di `/validate-certificate/` dimana pengguna dapat:

1. Memasukkan kode unik sertifikat
2. Atau memindai QR code menggunakan pemindai QR code apa pun
3. Melihat hasil validasi sertifikat yang menampilkan:
   - Status validasi
   - Nama peserta
   - Nama course
   - Tanggal penyelesaian

### Mengelola Sertifikat

1. Navigasikan ke 'Sertifikat' di admin WordPress
2. Lihat semua sertifikat dalam tabel yang dapat diurutkan
3. Filter sertifikat berdasarkan nama course
4. Hapus sertifikat jika diperlukan
5. Ekspor sertifikat ke format CSV

## Fitur Keamanan

- Pembuatan kode unik yang aman menggunakan `random_bytes()`
- Rate limiting untuk mencegah penyalahgunaan validasi
- Sanitasi dan validasi input
- Prepared SQL statements untuk mencegah injeksi

## Styling Kustom

Plugin ini sudah dilengkapi dengan desain responsif, tetapi Anda dapat menyesuaikan tampilan dengan menambahkan CSS kustom ke tema Anda.

## Struktur Database

Plugin ini membuat tabel kustom di database WordPress Anda dengan struktur berikut:

- `id`: ID Sertifikat (auto-increment)
- `date`: Tanggal penyelesaian
- `name`: Nama peserta
- `course_name`: Nama course
- `unique_code`: Kode verifikasi unik yang aman

## Persyaratan

- WordPress 4.7 atau lebih tinggi
- PHP 7.0 atau lebih tinggi (untuk dukungan `random_bytes()`)
- Akses tulis ke database WordPress

## Dukungan

Untuk dukungan atau permintaan fitur, silakan hubungi email **[zaky@siberin.id](mailto:zaky@siberin.id)**.

## Kredit

Dikembangkan oleh **JackTekno ([zaky@siberin.id](mailto:zaky@siberin.id))**.

## Riwayat Versi

- 1.0: Versi stabil saat ini.
- 1.1: Menambahkan fitur custom id sertifikat diawal langsung pada dashboard wordpress. Seperti **JackTekno**7b2fac0840a0012d04ccbab313e751d6.
- 1.2: Menambahkan fitur dukungan export.

## Versi Akan Datang

- 2.0: Menambahkan pengatauran pilihan Bahasa.
- 2.1: Menambahkan bahasa Inggris (English).

## Lisensi

Plugin ini dilisensikan di bawah ketentuan lisensi `GPL-3.0 license`.

## Screenshot

- **Daftar Sertifikat**
  
  ![Daftar Sertifikat](/Images/daftar-sertifikat.png)

- **Menu Dashboard Wordpress**
  
  ![Menu Dashboard Wordpress](/Images/menu.png)

- **Buat Sertifikat**
  
  ![Buat Sertifikat](/Images/buat-sertifikat.png)

- **Bulk Sertifikat**
  
  ![Bulk Sertifikat](/Images/bulk-sertifikat.png)

- **Validasi Sertifikat**
  
  ![Validasi Sertifikat](/Images/validasi-sertifikat.png)

- **Hasil Validasi Sertifikat**
  
  ![Hasil Validasi Sertifikat](/Images/validasi-hasil.png)
