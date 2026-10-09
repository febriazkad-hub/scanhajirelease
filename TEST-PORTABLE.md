# Menguji ScanHaji portable 2.5.0

1. Unduh ZIP dari https://github.com/febriazkad-hub/scanhajirelease/releases/latest, ekstrak seluruh isi ke folder baru, buka ScanHaji.exe.
2. Pada Windows 10 mulai 1903 atau Windows 11 dengan Framework bawaan, aplikasi harus terbuka tanpa meminta Desktop Runtime 10. Versi menunjukkan 2.5.0. Jangan menghapus runtime sistem untuk pengujian.
3. Jika Framework 4.8 belum tersedia pada PC lama, launcher memandu unduhan Microsoft Framework 4.8 Runtime; pilih Tidak untuk membatalkan tanpa mengubah data.
4. Matikan internet lalu impor XLS/XLSX Siskohat melalui Data Jemaah. Periksa sheet/tahun, porsi 10 digit termasuk nol depan, tanggal dan jumlah baris; Terapkan Data.
5. Tutup/buka dan pastikan data/pengaturan tetap tersedia. Tutup lalu pindahkan seluruh folder ke PC lain dan ulangi. Data/settings tetap di akar folder.
6. Periksa biodata, MRZ, tombol scan/impor dan pratinjau pada skala 100%/125% serta ukuran layar kecil.

## Auto-update dan upgrade

Aktifkan internet pada versi lama yang dapat berjalan; tunggu update siap lalu tutup. Setelah updater selesai, buka ScanHaji.exe, cek versi, impor dan data/settings. Bandingkan cadangan Backups/updates.

Versi 2.4.0 yang belum bisa dibuka karena Desktop Runtime 10 tidak terpasang dapat diganti manual dengan ZIP 2.5 saat aplikasi tertutup. Data/settings di akar dipertahankan.

## Bukti pengujian

CI menjalankan EXE final setelah ILRepack, memastikan target Framework 4.8, mscorlib dan CLR Windows digunakan, tanpa CoreCLR maupun DLL pihak ketiga terpisah. DOTNET_ROOT menunjuk folder kosong dan PATH tanpa SDK saat menjalankan paket. Job impor tidak memasang Desktop Runtime 10 x86.

CI menguji Framework 4.7.2 ditolak, 4.8/4.8.1 diterima, panduan asli dan pembatalan. Pengujian impor/validasi/persistensi/MRZ/UI dan kegagalan updater dipertahankan. Updater native diuji dari paket publik 2.2.0, 2.3.0 dan 2.4.0 ke Framework 4.8, membandingkan hash Data/settings/snapshot dan menjalankan impor setelah update.

Uji ini tidak menjamin semua file Siskohat atau kebijakan PC. Jika muncul 0x800711C7, pengelola Application Control perlu memeriksa berkas yang ditolak.
