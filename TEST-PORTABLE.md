# Menguji ScanHaji portable 2.3.0

Paket ini membawa runtime .NET 10 dan library impor sendiri. Pengguna tidak perlu memasang .NET, Excel/Office, SDK atau DLL tambahan. Gunakan Windows 10/11 x86 atau x64 dengan folder aplikasi dan folder sementara yang dapat ditulis.

## Uji di PC lain

1. Unduh `ScanHaji-win-Portable.zip` dari https://github.com/febriazkad-hub/scanhajirelease/releases/latest. Ekstrak seluruh isi ke folder baru, misalnya `D:\ScanHaji-Uji`. Jangan menjalankan langsung dari ZIP. Buka `ScanHaji.exe` di akar folder.
2. Pastikan judul aplikasi menunjukkan v2.3.0. Matikan koneksi internet untuk uji impor; tidak perlu menghapus .NET yang sudah ada di Windows.
3. Buka **Data Jemaah**, pilih hasil ekspor Siskohat `.xls` atau `.xlsx`, pilih sheet dan tahun, lalu periksa pratinjau. Nomor porsi harus tetap 10 digit termasuk nol di depan; jumlah baris dan tanggal lahir harus sesuai file sumber. Terapkan Data.
4. Tutup dan buka kembali aplikasi. Pastikan data yang diimpor masih tersedia. Pengaturan tersimpan di `settings.json` dan data di `Data` pada akar folder portable.
5. Tutup aplikasi, salin **seluruh folder** ke PC lain atau lokasi baru. Jalankan launcher `ScanHaji.exe`; ulangi impor dan cek data tersimpan. Jangan hanya menyalin EXE atau `current`.
6. Uji tampilan pada skala layar 100% dan 125%: tombol impor, pratinjau dan nomor porsi harus terbaca dan dapat diklik.

## Uji auto-update

Auto-update memerlukan rilis stabil dengan nomor versi lebih tinggi; commit source dengan versi sama tidak menghasilkan update baru.

1. Sebelum menguji, buat cadangan seluruh folder. Pengguna 2.2.0 dapat menerima 2.3.0 otomatis. Jika versi lama belum bisa berjalan di PC tujuan, ekstrak paket 2.3.0 secara manual ke folder lama saat aplikasi tertutup.
2. Aktifkan internet, buka versi lama dan tunggu unduhan selesai. Judul menampilkan `Update v... siap`. Pemeriksaan pertama dimulai setelah sekitar 10–30 detik; unduhan bergantung koneksi.
3. Tutup aplikasi dan tunggu pemasangan selesai. Buka lagi melalui `ScanHaji.exe`. Pastikan nomor versi naik, data jemaah dan pengaturan tetap tersedia, serta impor XLS/XLSX tetap berhasil.
4. Periksa `Backups\updates` untuk cadangan sebelum update. Log ringkas ada di `Logs\auto-update.log` bila update belum siap. Saat offline, versi saat ini harus tetap dapat mengimpor data.

## Bukti pengujian build

Windows CI menjalankan EXE yang benar-benar ada di ZIP, dengan PATH tanpa SDK dan DOTNET_ROOT mengarah ke folder kosong. Pemeriksaan memastikan runtime dan CoreLib berasal dari bundle aplikasi dan library pihak ketiga dimuat dari bundle. CI menguji XLS/XLSX, nol di depan nomor porsi, tanggal, validasi, simpan/muat, folder dipindah, UI, kegagalan updater, update native dan upgrade dari paket 2.2.0 publik. Hash data, pengaturan dan cadangannya dibandingkan sebelum/sesudah update.

Ini tidak menggantikan uji dengan file Siskohat asli di PC tujuan. Bila Windows menampilkan `0x800711C7`, catat berkas yang ditolak dan minta pengelola kebijakan Application Control memeriksanya; runtime bawaan tidak mengubah izin kebijakan Windows.
