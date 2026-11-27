# ScanHaji

Aplikasi portable untuk scan paspor dan impor data jemaah SISKOHAT.

Unduh [ScanHaji-win-Portable.zip](https://github.com/febriazkad-hub/scanhajirelease/releases/latest/download/ScanHaji-win-Portable.zip), ekstrak seluruh isi dan buka **ScanHaji.exe**.

Versi **2.6.0** memakai **.NET Framework 4.8 bawaan Windows** (x86), kompatibel dengan 4.8.1, dilengkapi Pusat Jemaah SQLite x86, engine Auto-Crop A4 portabel (~35 MB), serta Hub Dokumen Port `3010` & dukungan scanner WIA Epson. Pada Windows 10 mulai 1903 dan Windows 11 standar, tidak perlu memasang Desktop Runtime 10, SDK, atau Python. Launcher memberi panduan unduhan Microsoft Framework 4.8 Runtime jika belum tersedia pada PC lama.

Library impor digabung ke EXE dan runtime SQLite x86 dibundel di dalam paket; tidak perlu Excel/Office atau instalasi tambahan. Impor XLS/XLSX/CSV dan Pusat Jemaah bekerja offline. Auto-Crop A4, OCR API, dan auto-update memerlukan internet.

Konfigurasi AI bawaan memakai combo **scanhaji**: `https://9r2.mdgi.web.id/v1` sebagai utama dan `https://9r.mdgi.web.id/v1` sebagai cadangan. Instalasi baru siap digunakan tanpa mengisi endpoint, model atau API key. Pengelola harus menyediakan combo `scanhaji` yang mendukung input gambar pada kedua server. Pengaturan umum dan data jemaah dipertahankan saat pembaruan. Reset Bawaan mengembalikan dua endpoint tersebut.

Rilis stabil baru diunduh di latar belakang lalu dipasang setelah aplikasi ditutup. Data/settings tetap di akar portable. Tutup sebelum menyalin seluruh folder ke PC lain.

Klien versi sebelumnya (`2.2`–`2.5.5`) dapat menerima pembaruan ke **2.6.0** saat aplikasinya dapat berjalan. Jika 2.4 tidak bisa dibuka karena Desktop Runtime belum ada, ekstrak ZIP **2.6.0** saat aplikasi tertutup lalu buka launcher baru.

Baca [panduan pengujian](TEST-PORTABLE.md). Aplikasi belum memiliki sertifikat Authenticode publik; Windows Application Control tetap mengikuti kebijakan PC.

Repo ini hanya untuk rilis aplikasi. Jangan unggah data jemaah, hasil scan, konfigurasi pengguna atau API key.

