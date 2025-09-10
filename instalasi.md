Panduan Instalasi Aplikasi Absensi ke GitHub Pages
Dokumen ini akan memandu Anda langkah demi langkah untuk mempublikasikan aplikasi web absensi Anda (file aplikasi_absensi.html) secara online menggunakan GitHub Pages, sehingga dapat diakses melalui internet.

Prasyarat
Sebelum memulai, pastikan Anda memiliki:

Akun GitHub: Jika belum punya, Anda bisa mendaftar gratis di github.com.

File Aplikasi: Siapkan file aplikasi_absensi.html yang sudah final.

URL Google Apps Script: Anda harus sudah menyelesaikan langkah-langkah di file instructions.md dan memiliki URL Web App dari Google Apps Script Anda.

Langkah 1: Membuat Repository Baru di GitHub
Repository adalah tempat untuk menyimpan kode atau file proyek Anda.

Login ke akun GitHub Anda.

Di pojok kanan atas, klik ikon + lalu pilih "New repository".

Isi detail repository:

Repository name: Beri nama yang mudah diingat, misalnya aplikasi-absensi-smp.

Description (Opsional): Beri deskripsi singkat, contohnya "Aplikasi Absensi Siswa dan Guru SMP Diponegoro Sampang".

Pilih "Public" agar bisa diakses melalui GitHub Pages.

Centang "Add a README file". Ini akan memudahkan inisialisasi repository.

Klik tombol "Create repository".

Langkah 2: Mengunggah File Aplikasi
Sekarang kita akan memasukkan file aplikasi_absensi.html ke dalam repository yang baru dibuat.

Di halaman repository Anda, klik tombol "Add file" lalu pilih "Upload files".

Seret (drag and drop) file aplikasi_absensi.html ke area unggah, atau klik "choose your files" untuk memilih file dari komputer Anda.

Setelah file berhasil diunggah, gulir ke bawah dan klik tombol "Commit changes".

Langkah 3: Mengaktifkan GitHub Pages
Ini adalah langkah untuk mempublikasikan file HTML Anda sebagai sebuah situs web.

Di halaman utama repository Anda, klik tab "Settings".

Di menu sebelah kiri, cari dan klik "Pages".

Pada bagian "Build and deployment", di bawah "Source", pilih "Deploy from a branch".

Di bawah "Branch", pastikan branch yang terpilih adalah main (atau master). Biarkan folder di / (root).

Klik "Save".

Setelah Anda menyimpan, halaman akan me-refresh. Gulir kembali ke bagian GitHub Pages. Anda akan melihat notifikasi berwarna hijau atau biru yang berisi: "Your site is live at https://<NAMA_PENGGUNA_ANDA>.github.io/<NAMA_REPOSITORY_ANDA>/aplikasi_absensi.html".

Penting: Mungkin butuh beberapa menit (1-5 menit) agar situs web Anda benar-benar aktif setelah pertama kali diaktifkan.

Langkah 4: Menggunakan Aplikasi Anda
Klik tautan yang diberikan oleh GitHub Pages. Tautan tersebut akan membuka aplikasi absensi Anda.

Aplikasi kini sudah online dan dapat diakses dari mana saja menggunakan laptop atau ponsel.

Semua data akan disimpan dan diambil dari Google Sheet yang telah Anda konfigurasikan sebelumnya.

Catatan Tambahan
Pembaruan: Jika Anda ingin memperbarui tampilan atau fitur aplikasi, Anda hanya perlu mengedit file aplikasi_absensi.html di komputer Anda, lalu unggah kembali file tersebut ke repository GitHub dengan cara yang sama seperti di Langkah 2. Perubahan akan otomatis tayang di situs web Anda setelah beberapa saat.

Keamanan: Metode ini sangat aman. Koneksi ke Google Sheets Anda dijembatani oleh Google Apps Script, sehingga tidak ada informasi sensitif yang terlihat di kode HTML Anda.

Pastikan URL Skrip Benar: Jika aplikasi tidak dapat memuat data, pastikan URL SCRIPT_URL di dalam file aplikasi_absensi.html sudah benar dan sesuai dengan URL yang Anda dapatkan saat men-deploy Google Apps Script.