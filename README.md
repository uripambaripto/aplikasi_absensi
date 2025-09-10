Panduan Menghubungkan Aplikasi dengan Google Sheets
Ikuti langkah-langkah ini untuk menyiapkan Google Sheets sebagai database dan menghubungkannya ke aplikasi web Anda.

Bagian 1: Menyiapkan Google Sheet
Buat Spreadsheet Baru:

Buka Google Sheets.

Beri nama spreadsheet Anda, misalnya "Database Absensi SMP Diponegoro".

PENTING: Anda tidak perlu membuat sheet DataGuru atau DataSiswa secara manual. Skrip akan membuatnya secara otomatis saat pertama kali dijalankan.

Bagian 2: Membuat dan Mengkonfigurasi Google Apps Script
Ini adalah bagian terpenting untuk membuat jembatan (API) antara aplikasi Anda dan spreadsheet.

Buka Editor Skrip:

Dari spreadsheet Anda, klik Extensions > Apps Script.

Sebuah tab baru akan terbuka dengan editor skrip. Hapus semua kode contoh yang ada di dalamnya.

Tempelkan Kode Skrip:

Salin seluruh isi dari file code.gs yang telah disediakan.

Tempelkan ke dalam editor skrip yang kosong.

Simpan Proyek:

Klik ikon Simpan (disket) di bagian atas.

Beri nama proyek Anda, misalnya "API Absensi", lalu klik "Rename".

Bagian 3: Deploy sebagai Aplikasi Web (Wajib Diikuti dengan Teliti)
Ini adalah langkah krusial untuk membuat skrip Anda dapat diakses dari internet.

Buka Dialog Deployment:

Di pojok kanan atas editor skrip, klik tombol biru Deploy > New deployment.

Konfigurasi Deployment:

Klik ikon roda gigi (Select type) di sebelah kiri "Select type".

Pilih "Web app".

Pada bagian "Configuration":

Description: Isi dengan deskripsi singkat, misalnya "Versi 1 Aplikasi Absensi".

Execute as: Biarkan "Me".

Who has access: INI BAGIAN PALING PENTING. Ubah dari "Only myself" menjadi "Anyone". Ini memungkinkan aplikasi web Anda (yang dihosting di GitHub) untuk mengakses skrip tanpa perlu login.

Klik tombol "Deploy".

Otorisasi Skrip:

Google akan meminta izin agar skrip dapat mengelola spreadsheet Anda. Klik "Authorize access".

Pilih akun Google Anda.

Anda mungkin akan melihat peringatan "Google hasn’t verified this app". Ini normal. Klik "Advanced", lalu klik "Go to (nama proyek Anda)".

Klik "Allow" untuk memberikan izin.

Salin URL Web App:

Setelah deployment berhasil, Anda akan melihat sebuah URL di bawah "Web app URL". URL ini diakhiri dengan /exec.

Klik tombol "Copy" untuk menyalin URL ini. Simpan URL ini karena Anda akan menempelkannya ke dalam file HTML.

Klik "Done".

Bagian 4: Menghubungkan Aplikasi Web ke Skrip
Buka file aplikasi_absensi.html.

Cari baris kode berikut (biasanya di dekat bagian atas tag <script>):

const SCRIPT_URL = ''; // <-- PASTE URL ANDA DI SINI

Tempelkan URL yang telah Anda salin dari Google Apps Script di antara tanda kutip ''.
Contoh hasil akhir:

const SCRIPT_URL = '[https://script.google.com/macros/s/ABCdeFG123.../exec](https://script.google.com/macros/s/ABCdeFG123.../exec)';
