# ScanHaji

Aplikasi portable untuk scan paspor dan impor data jemaah SISKOHAT.

Unduh [ScanHaji-win-Portable.zip](https://github.com/febriazkad-hub/scanhajirelease/releases/latest/download/ScanHaji-win-Portable.zip), ekstrak seluruh isi dan buka **ScanHaji.exe**.

Versi **2.5.2** memakai **.NET Framework 4.8 bawaan Windows**, kompatibel dengan 4.8.1. Pada Windows 10 mulai 1903 dan Windows 11 standar, tidak perlu memasang Desktop Runtime 10 atau SDK. Launcher memberi panduan unduhan Microsoft Framework 4.8 Runtime jika belum tersedia pada PC lama.

Library impor digabung ke EXE; tidak perlu Excel/Office atau DLL tambahan. Impor XLS/XLSX dan data jemaah bekerja offline. OCR API dan auto-update memerlukan internet.

Konfigurasi AI bawaan memakai combo **scanhaji**: `https://9r2.mdgi.web.id/v1` sebagai utama dan `https://9r.mdgi.web.id/v1` sebagai cadangan. Instalasi baru siap digunakan tanpa mengisi endpoint, model atau API key. Pengelola harus menyediakan combo `scanhaji` yang mendukung input gambar pada kedua server. Konfigurasi AI lama diganti saat dimuat oleh 2.5.2; pengaturan umum dan data jemaah dipertahankan. Reset Bawaan mengembalikan dua endpoint tersebut.

Rilis stabil baru diunduh di latar belakang lalu dipasang setelah aplikasi ditutup. Data/settings tetap di akar portable. Tutup sebelum menyalin seluruh folder ke PC lain.

Klien 2.2/2.3/2.4/2.5.0/2.5.1 dapat menerima versi baru saat aplikasi lamanya dapat berjalan. Jika 2.4 tidak bisa dibuka karena Desktop Runtime belum ada, ekstrak ZIP 2.5.2 saat aplikasi tertutup lalu buka launcher baru.

Baca [panduan pengujian](TEST-PORTABLE.md). Aplikasi belum memiliki sertifikat Authenticode publik; Windows Application Control tetap mengikuti kebijakan PC.

Repo ini hanya untuk rilis aplikasi. Jangan unggah data jemaah, hasil scan, konfigurasi pengguna atau API key.

