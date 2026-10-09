# ScanHaji 2.4.0 portable ringan

Ekstrak seluruh isi ZIP rilis ke folder yang dapat ditulis. Jalankan **ScanHaji.exe** di akar folder. Aplikasi tidak menyertakan runtime .NET 10: dibutuhkan **.NET Desktop Runtime 10 x86** yang dipasang terpisah, cukup sekali per PC. Library impor tetap dibundel; tidak perlu Excel/Office atau DLL tambahan.

## Saat runtime belum ada

Launcher kecil memakai .NET Framework bawaan Windows 10/11, sehingga panduan tetap dapat tampil tanpa .NET 10. Pesan **Persiapan ScanHaji** menjelaskan runtime yang kurang. Pilih **Ya** untuk membuka unduhan resmi https://dotnet.microsoft.com/en-us/download/dotnet/10.0, pilih **.NET Desktop Runtime > Windows > x86 > Installer**, lalu jalankan installer Microsoft. Setelah selesai, buka ScanHaji.exe lagi.

Runtime x64 saja, .NET Runtime biasa, SDK x64, dan .NET Framework bawaan Windows tidak menggantikan Desktop Runtime x86. Jika PC offline, unduh installer x86 di PC lain dan pindahkan. Bila pemasangan memerlukan izin administrator, pengelola PC perlu menyetujuinya. Menolak panduan tidak mengubah data/settings.

Setelah runtime tersedia, impor XLS/XLSX bekerja tanpa internet. Pilih Data Jemaah, ekspor Siskohat, sheet/tahun dan periksa pratinjau sebelum Terapkan Data. OCR API dan auto-update memerlukan internet.

Data dan settings.json disimpan di akar folder di luar current. Tutup aplikasi sebelum menyalin seluruh folder ke PC lain. PC tujuan memerlukan Desktop Runtime x86 juga; launcher memeriksanya kembali. Jangan hanya menyalin EXE.

## Upgrade versi lama

Klien 2.2.0/2.3.0 memakai pemasangan update silent. Bila Desktop Runtime x86 belum terpasang, updater menunda upgrade 2.4.0 dan mempertahankan versi lama. Pasang runtime resmi sekali lalu buka/tutup aplikasi lama lagi, atau ekstrak ZIP 2.4.0 saat aplikasi tertutup dan gunakan launcher baru untuk panduan runtime. Mulai 2.4.0, updater dapat menampilkan prompt pemasangan prasyarat baru sebelum mengganti aplikasi.

## Jika Windows memblokir

0x800711C7 berarti kebijakan Application Control menolak berkas. Runtime terpasang dan launcher tidak memberi izin melewati kebijakan Windows. Paket belum memiliki sertifikat Authenticode penerbit tepercaya.

Pengelola PC dapat memeriksa Event Viewer > Applications and Services Logs > Microsoft > Windows > CodeIntegrity > Operational. Kebijakan publisher membutuhkan sertifikat rilis yang diizinkan atau allow policy organisasi. Run as administrator tidak menggantikan izin kebijakan.

Unduh hanya dari https://github.com/febriazkad-hub/scanhajirelease/releases/latest. build-info.json mencatat versi, commit dan kebutuhan runtime; TEST-PORTABLE.md menjelaskan pengujian.
