# Fuel E-voucher System
Internship project portfolio: Studi kasus sistem e-voucher yang dikembangkan saat magang untuk digitalisasi distribusi BBM kendaraan operasional rumah sakit. Dilengkapi fitur pelacakan dan manajemen kuota. Source code bersifat private untuk mematuhi NDA dan menjaga kerahasiaan data fasilitas kesehatan. Halaman ini berisi arsitektur &amp; alur sistem.

> **Disclaimer Kerahasiaan (NDA):**
> Repository ini adalah dokumentasi portofolio dari proyek Magang Hub Kemnaker Batch 2 di rumah sakit. Demi mematuhi Non-Disclosure Agreement (NDA) dan menjaga kerahasiaan data operasional serta privasi rumah sakit, *source code* asli tidak dapat dipublikasikan. Halaman ini berfokus pada studi kasus, arsitektur sistem, dan penyelesaian masalah (*problem-solving*).

---

## Latar Belakang Proyek
Rumah sakit membutuhkan sistem yang cepat dan efisien untuk mengelola distribusi Bahan Bakar Minyak (BBM) bagi kendaraan operasional harian, seperti ambulans, mobil dinas eselon, kendaraan kurir, dan jerigen. Sebelumnya, proses ini dilakukan secara manual yang rentan terhadap antrean panjang, pencatatan yang tidak akurat, dan kesulitan dalam pelacakan kuota.

Sistem E-Voucher ini dibangun berbasis web yang digunakan untuk digitalisasi pengelolaan dan penyaluran kuota BBM bagi kendaraan operasional rumah sakit. Sistem ini menggantikan pencatatan manual dengan mekanisme Kode QR, memastikan transparansi transaksi antara pengguna (pegawai/driver) pihak Rumah Sakit dan operator SPBU mitra secara real-time. Dalam 

## Peran & Tanggung Jawab
Dalam proyek ini, saya dipercaya penuh sebagai **Fullstack Web Developer (Intern)** untuk membangun sistem dari nol hingga siap diimplementasikan. Tanggung jawab utama saya meliputi:

* **Pengembangan Backend (Logika & Sistem):** Membangun arsitektur aplikasi, logika pembuatan e-voucher, dan manajemen *database* relasional menggunakan *framework* **Laravel (PHP)**.
* **Desain & Implementasi Frontend (UI/UX):** Merancang antarmuka pengguna yang bersih, responsif, dan intuitif menggunakan **Tailwind CSS** dan sistem *templating* **Blade**. Kepekaan terhadap komposisi visual sangat membantu dalam menyusun tata letak *dashboard* yang ramah pengguna operasional.
* **Interaktivitas & API Internal:** Mengimplementasikan **Alpine.js** dan AJAX (Fetch API) untuk menangani interaktivitas di sisi klien (seperti *modal pop-up*, *dropdown*, dan pengambilan data *real-time*) secara efisien tanpa perlu memuat ulang halaman (*page reload*).
* **Manajemen Basis Data:** Merancang skema tabel dan relasi data menggunakan **MySQL**, serta mengelola *environment* basis data lokal selama masa pengembangan menggunakan **DBngin**.
* **Kolaborasi Keamanan & Deployment:** Berkoordinasi dengan tim IT rumah sakit untuk memastikan sistem mematuhi standar keamanan sebelum mereka melakukan *deployment* ke *production server* (yang didukung oleh Cloudflare, HSTS, dan HTTP/3).

## Teknologi yang Digunakan (Tech Stack)
* **Backend:** PHP, Laravel Framework
* **Frontend:** Tailwind CSS, Alpine.js, Blade Templating, Font Awesome
* **Database & Local Server:** MySQL, DBngin
* **Arsitektur Pengolahan Data:** AJAX / JSON (Internal API)
* **Infrastruktur Klien (Deployment oleh Tim IT):** Cloudflare, HSTS, HTTP/3

## Fitur Utama
* **Manajemen Kuota Kendaraan:** Sistem secara otomatis melacak batas maksimal pengisian BBM berdasarkan jenis kendaraan atau alat operasional.
* **Pembuatan E-Voucher Instan:** Pengguna dapat membuat *barcode* / kode unik e-voucher untuk ditukarkan di SPBU. 
* **Role-Based Access Control (RBAC):** Akses sistem dibagi berdasarkan peran, seperti Superadmin, Admin Operasional, dan Driver.
* **Laporan Real-time:** Dashboard untuk memantau riwayat pengisian BBM dan total anggaran operasional.

## Dampak & Hasil (Impact) 
Berikut adalah penyelesaian masalah utama (*problem-solving*) yang berhasil dicapai:

* **Efisiensi Waktu Persetujuan (*Approval*) yang Drastis:**
  * **Sebelum:** Pengajuan pengisian BBM menggunakan dokumen kertas yang harus memutar dari meja ke meja, memakan waktu **12 hingga 24 jam** hanya untuk mendapatkan izin dan tanda tangan manual.
  * **Sesudah:** Birokrasi dipangkas. Proses *approval* kini berjalan secara *real-time* dalam hitungan menit (Admin cukup memvalidasi dan melakukan klik persetujuan pada sistem).

* **Proses Penukaran Modern dengan QR Code:**
  * **Sebelum:** Driver harus membawa dan menyerahkan lembaran voucher kertas kepada operator SPBU, yang rentan rusak, tertinggal, atau hilang.
  * **Sesudah:** Penukaran voucher sepenuhnya nirkertas (*paperless*). Pengguna cukup menunjukkan dan melakukan **Scan QR Code** langsung dari sistem untuk mencairkan kuota BBM.

* **Keamanan Data & Digitalisasi Nota (*Zero Data Loss*):**
  * **Sebelum:** Mengandalkan nota fisik dari SPBU sebagai bukti transaksi yang sangat rawan terselip, pudar, atau hilang, sehingga menyulitkan proses audit.
  * **Sesudah:** Seluruh bukti transaksi dan nota terdigitalisasi dan tersimpan permanen di dalam *database* sistem, menghilangkan risiko kehilangan dokumen fisik.

* **Otomatisasi Laporan Keuangan & Operasional yang Transparan:**
  * **Sebelum:** Pencatatan pengeluaran operasional BBM dan rekapitulasi data masih dilakukan secara manual menggunakan buku catatan kertas.
  * **Sesudah:** Sistem secara otomatis melakukan kalkulasi dan menghasilkan laporan riwayat pengisian yang rapi, akurat, dan transparan. Laporan ini dapat diakses secara instan baik melalui *dashboard* Admin Rumah Sakit maupun *dashboard* Admin SPBU.

---
