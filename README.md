**Dokumentasi Web Apps: Si Pintar Pencatat Pengeluaran**
========================================================

**1\. Deskripsi**
-----------------

**Si Pintar Pencatat Pengeluaran** adalah sebuah aplikasi web yang dirancang untuk merevolusi cara pengguna mencatat pengeluaran harian. Aplikasi ini memanfaatkan kekuatan kecerdasan buatan (AI) dari Google Gemini untuk memberikan pengalaman input data yang akurat dan efisien. Pengguna tidak lagi terbatas pada pengetikan manual; mereka dapat mendiktekan pengeluaran melalui suara, mengunggah gambar struk, atau bahkan memindai struk langsung dengan kamera.

Aplikasi ini bersifat _client-side_ (berjalan sepenuhnya di browser pengguna), membuatnya sangat ringan dan dapat di-hosting di platform gratis seperti GitHub Pages. Fleksibilitasnya memungkinkan pengguna memilih antara mode otomatis (menggunakan Kunci API Gemini pribadi) dan mode manual (menggunakan akun Google Gemini), memberikan kontrol penuh kepada pengguna.

Akses ke aplikasi ini silahkan klik >> [https://catatpengeluaran.isparmo.com/](https://catatpengeluaran.isparmo.com/)

**2\. Fitur-Fitur**
-------------------

*   **Pilihan Mode Penggunaan AI**:
    
*   **Mode Otomatis**: Dengan mengonfigurasi Kunci API Gemini, fitur input suara dan scan struk bekerja secara mulus di dalam aplikasi.
    
*   **Mode Manual**: Tanpa Kunci API, pengguna diarahkan ke akun Gemini mereka untuk melakukan analisis data, memberikan alternatif yang tetap fungsional.
    
*   **Tiga Metode Input Cerdas**:
    

1.  **Input dengan Suara**: Mendukung bahasa alami dalam Bahasa Indonesia, termasuk frasa waktu relatif seperti "kemarin" atau "dua hari yang lalu".
    
2.  **Upload Struk Belanja**: Mengunggah gambar struk dari galeri untuk dianalisis secara otomatis.
    
3.  **Scan Struk dengan Kamera**: Membuka kamera perangkat secara langsung untuk memfoto dan menganalisis struk (dioptimalkan untuk mobile).
    

*   **Penyimpanan Data Fleksibel**:
    
*   **Integrasi Google Sheets**: Data dapat disimpan dengan aman dan terorganisir di Google Sheet pribadi pengguna melalui Google Apps Script.
    
*   **Ekspor ke CSV**: Pengguna dapat mengunduh riwayat pengeluaran mereka sebagai file CSV untuk penggunaan offline atau analisis lebih lanjut.
    
*   **Antarmuka Pengguna Intuitif**:
    
*   **Panduan Interaktif**: Jendela _pop-up_ memandu pengguna langkah demi langkah dalam proses konfigurasi Kunci API dan koneksi ke Google Sheets.
    
*   **Desain Responsif**: Tampilan yang bersih dan adaptif di berbagai perangkat, dari desktop hingga mobile.
    
*   **Progress Bar Visual**: Memberikan umpan balik yang jelas saat AI sedang memproses data.
    

**3\. Teknologi yang Dipakai**
------------------------------

*   **Frontend**:
    
*   **HTML5**: Struktur dasar aplikasi web.
    
*   **Tailwind CSS**: Kerangka kerja CSS untuk membangun antarmuka yang modern dan responsif dengan cepat.
    
*   **JavaScript (ES6+)**: Menangani semua logika aplikasi, interaksi DOM, manajemen status (pilihan API), dan komunikasi dengan layanan eksternal.
    
*   **Kecerdasan Buatan (AI)**:
    
*   **Google Gemini API (model gemini-2.0-flash)**: Inti dari fitur cerdas, digunakan untuk _Natural Language Understanding_ (NLU) pada input suara dan _Optical Character Recognition_ (OCR) pada gambar struk.
    
*   **Web Speech API**: API bawaan browser untuk menangkap audio dari mikrofon pengguna.
    
*   **Penyimpanan & Backend Sederhana**:
    
*   **Google Sheets**: Berfungsi sebagai database gratis dan mudah diakses.
    
*   **Google Apps Script**: Bertindak sebagai _backend_ minimalis untuk menerima data dari aplikasi (via doPost) dan menuliskannya ke Google Sheets.
    
*   **Local Storage Browser**: Menyimpan preferensi pengguna seperti pilihan mode AI, Kunci API, dan URL Google Sheet Web App.
    

**4\. Untuk Siapa Saja**
------------------------

Aplikasi ini dirancang untuk:

*   **Individu & Mahasiswa**: Yang ingin memulai kebiasaan mencatat keuangan dengan cara yang tidak merepotkan.
    
*   **Profesional Sibuk**: Yang membutuhkan cara cepat untuk mencatat pengeluaran di tengah kesibukan.
    
*   **Pengguna GitHub Pages**: Developer atau individu yang ingin meng-hosting aplikasi personal tanpa biaya server.
    
*   **Keluarga**: Untuk melacak pengeluaran rumah tangga secara transparan.
    
*   **Siapa Saja yang Lelah dengan Input Manual**: Pengguna yang menginginkan efisiensi dan akurasi yang ditawarkan oleh AI.
    

**5\. Cara Menggunakan**
------------------------

### **A. Pengaturan Awal (Wajib)**

Saat pertama kali membuka aplikasi, Anda akan disambut dengan pilihan:

1.  **Gunakan Kunci API Gemini**: Pilih ini untuk pengalaman otomatis. Anda akan diminta memasukkan Kunci API yang bisa didapat dari **Google AI Studio**. Setelah disimpan, fitur suara dan scan akan berfungsi penuh.
    
2.  **Gunakan Akun Gemini (Google)**: Pilih ini jika Anda tidak memiliki atau tidak ingin menggunakan Kunci API. Saat Anda menggunakan fitur suara atau scan, aplikasi akan membuka tab baru ke **laman Gemini**, di mana Anda bisa melanjutkan proses secara manual.
    

### **B. Menghubungkan ke Google Sheet**

Untuk menyimpan data secara online, Anda perlu menghubungkan aplikasi ke Google Sheet:

1.  Klik tombol **"Simpan ke Google Sheet"**. Jendela panduan akan muncul.
    
2.  **Langkah 1**: Buat **Spreadsheet baru** di Google Sheets.
    
3.  **Langkah 2**: Buka **Ekstensi > Apps Script**, lalu **salin-tempel kode** yang disediakan di dalam panduan.
    
4.  **Langkah 3**: Lakukan **Deploy** sebagai **Web app**, atur akses ke **"Anyone"**, dan berikan izin.
    
5.  **Langkah 4**: Salin **Web app URL** yang Anda dapatkan, tempelkan ke kolom input di panduan, dan klik **Simpan**.
    

**6\. Saran Pengembangan di Masa Depan**
----------------------------------------

1.  **Dasbor Visualisasi Data & Laporan Otomatis**:
    

*   **Gambaran**: Menambahkan tab atau halaman baru di dalam aplikasi yang mengambil data dari Google Sheet dan menampilkannya dalam bentuk grafik (misalnya, diagram lingkaran pengeluaran per kategori, tren pengeluaran bulanan). Pengguna juga bisa mendapatkan laporan PDF bulanan yang dikirim ke email mereka.
    
*   **Manfaat**: Mengubah aplikasi dari sekadar alat pencatat menjadi alat analisis keuangan pribadi yang memberikan wawasan mendalam kepada pengguna.
    

1.  **Kategorisasi Otomatis & Fitur Anggaran (Budgeting)**:
    

*   **Gambaran**: Memperbarui prompt Gemini untuk tidak hanya mengekstrak item, tetapi juga mengkategorikannya secara otomatis (misalnya, "Kopi Starbucks" -> "Makanan & Minuman"). Pengguna kemudian dapat menetapkan batas anggaran untuk setiap kategori. Aplikasi akan memberikan notifikasi visual jika pengeluaran mendekati batas.
    
*   **Manfaat**: Membantu pengguna untuk lebih proaktif dalam mengelola keuangan, bukan hanya reaktif mencatat pengeluaran.
    

1.  **Fitur Pengingat & Pencatatan Berulang**:
    

*   **Gambaran**: Pengguna dapat mengatur pengeluaran rutin (misalnya, "Bayar langganan Netflix setiap tanggal 25"). Aplikasi akan secara otomatis menambahkan entri tersebut setiap bulan atau memberikan notifikasi pengingat kepada pengguna untuk mencatatnya.
    

**Manfaat**: Mengurangi beban pengguna untuk mengingat dan mencatat pengeluaran yang bersifat rutin, sehingga meningkatkan konsistensi pencatatan.
