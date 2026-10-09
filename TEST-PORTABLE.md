# Menguji ScanHaji portable 2.4.0

1. Ekstrak seluruh ZIP dari https://github.com/febriazkad-hub/scanhajirelease/releases/latest ke folder baru dan buka ScanHaji.exe.
2. Pada PC tanpa .NET Desktop Runtime 10 x86, pastikan pesan Persiapan ScanHaji tampil. Pilih Tidak: aplikasi keluar tanpa mengubah data. Buka lagi, pilih Ya dan unduh Desktop Runtime 10 Windows x86 Installer resmi Microsoft. Pasang lalu buka ScanHaji lagi. Bila offline, pindahkan installer dari PC lain.
3. Pastikan versi menunjukkan 2.4.0. Matikan internet, impor XLS/XLSX Siskohat melalui Data Jemaah, pilih sheet/tahun, periksa pratinjau dan Terapkan Data. Porsi harus tetap 10 digit termasuk nol depan.
4. Tutup/buka dan pastikan data/pengaturan tersedia. Tutup lalu salin seluruh folder ke PC lain; runtime PC tujuan diperiksa lagi.
5. Periksa tampilan pada skala 100% dan 125%.

## Auto-update

Pembaruan memerlukan rilis stabil dengan nomor lebih tinggi. Aktifkan internet pada versi lama; setelah judul menunjukkan update siap, tutup dan tunggu pemasangan. Buka lagi lewat ScanHaji.exe, periksa versi, impor, Data/settings dan Backups/updates.

Untuk upgrade 2.2.0/2.3.0, pasang Desktop Runtime 10 x86 lebih dulu. Klien lama menunda pemasangan bila runtime kurang karena update-nya memakai mode silent. Atau pasang ZIP baru manual saat aplikasi tertutup untuk mendapat launcher dengan panduan runtime.

## Pengujian build

Windows CI memeriksa launcher yang memakai Framework bawaan: runtime kosong, base runtime tanpa Desktop, versi salah, preview, patch stabil dan instalasi tidak lengkap. CI menampilkan dialog panduan asli dan memilih Tidak secara otomatis untuk memeriksa pembatalan tanpa unduhan.

Runtime x86 untuk CI diunduh dari Microsoft; SHA-512 dan tanda tangan Microsoft diverifikasi sebelum pemasangan. EXE ZIP diuji dengan PATH tanpa SDK. CoreLib harus berasal dari runtime terpasang, sementara ExcelDataReader dan library aplikasi tetap berasal dari bundle tanpa DLL terpisah. CI menguji XLS/XLSX, porsi, tanggal, validasi, persistensi, pindah folder, UI, updater gagal, update native, serta upgrade paket publik 2.2.0 dan 2.3.0 dengan hash data/settings/cadangan sama.

Uji ini belum mencakup seluruh kebijakan keamanan PC atau setiap berkas Siskohat asli. Application Control tetap perlu izin penerbit/administrator bila memblokir berkas.
