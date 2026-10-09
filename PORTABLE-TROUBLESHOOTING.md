# ScanHaji 2.5.1 portable .NET Framework 4.8

Ekstrak seluruh isi ZIP rilis ke folder yang dapat ditulis, lalu jalankan **ScanHaji.exe** di akar folder.

Aplikasi menggunakan **.NET Framework 4.8 bawaan Windows**, dan dapat berjalan pada Framework 4.8.1. Pada Windows 10 mulai 1903 dan Windows 11 standar, pengguna tidak perlu memasang .NET Desktop Runtime 10 atau SDK. Library impor digabung ke EXE; tidak memerlukan Excel/Office maupun DLL tambahan.

Jika launcher menampilkan **Persiapan ScanHaji**, Framework 4.8 belum terdeteksi. Pilih Ya untuk membuka https://dotnet.microsoft.com/en-us/download/dotnet-framework/net48. Pasang **Runtime**, bukan Developer Pack, lalu restart bila diminta. PC offline dapat memakai installer offline resmi yang diunduh lewat PC lain. Izin administrator mungkin diperlukan pada PC dengan Framework lama.

Impor XLS/XLSX Siskohat dan penyimpanan data berjalan offline. OCR API dan auto-update memerlukan internet. Data Jemaah > pilih file, sheet/tahun > periksa pratinjau > Terapkan Data. Tetap periksa validitas file/kolom dan nomor porsi.

Data dan settings.json berada di akar folder portable di luar current. Tutup sebelum memindahkan seluruh folder. Jangan hanya menyalin EXE atau current. Cadangan update tersedia di Backups/updates.

Pengguna 2.2/2.3/2.4/2.5.0 dapat menerima 2.5.1 melalui auto-update saat versi lamanya dapat berjalan. Jika 2.4 belum dapat dibuka karena Desktop Runtime belum ada, tutup aplikasi dan ekstrak ZIP 2.5.1 ke folder lama: paket baru menggunakan Framework Windows dan mempertahankan Data/settings di akar.

## Jika Windows memblokir

0x800711C7 menunjukkan Application Control menolak berkas. Menggabungkan library dan memakai Framework bawaan tidak memberikan izin melewati kebijakan. Aplikasi belum memiliki sertifikat Authenticode penerbit tepercaya.

Pengelola PC dapat memeriksa Event Viewer > Applications and Services Logs > Microsoft > Windows > CodeIntegrity > Operational. Gunakan sertifikat penerbit yang diizinkan atau allow policy organisasi bila diwajibkan. Run as administrator tidak menggantikan izin kebijakan.

Unduh hanya dari https://github.com/febriazkad-hub/scanhajirelease/releases/latest. TEST-PORTABLE.md memuat langkah pengujian.

