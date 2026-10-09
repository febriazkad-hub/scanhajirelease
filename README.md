# ScanHaji

Aplikasi portable untuk scan paspor dan impor data jemaah SISKOHAT.

Unduh **[ScanHaji-win-Portable.zip](https://github.com/febriazkad-hub/scanhajirelease/releases/latest/download/ScanHaji-win-Portable.zip)** dari rilis stabil terbaru. Ekstrak seluruh isi ke folder yang dapat ditulis, lalu jalankan **ScanHaji.exe**.

Mulai **2.4.0**, paket tidak membawa runtime .NET 10. Dibutuhkan **.NET Desktop Runtime 10 x86**, cukup dipasang sekali per PC. Jika belum ada, launcher menampilkan panduan Bahasa Indonesia dan membuka [unduhan resmi Microsoft](https://dotnet.microsoft.com/en-us/download/dotnet/10.0): pilih **.NET Desktop Runtime > Windows > x86 > Installer**. Setelah instalasi, buka ScanHaji.exe lagi. Pada PC offline, pindahkan installer dari PC lain. Runtime x64 atau .NET Framework bawaan Windows tidak menggantikan Desktop Runtime x86.

Tidak perlu Excel/Office atau DLL tambahan. Library impor tetap dibundel, dan impor XLS/XLSX bekerja tanpa internet setelah runtime tersedia.

Auto-update mengecek rilis stabil yang lebih baru, mengunduh di latar belakang dan memasang setelah aplikasi ditutup. Data/settings tetap di akar folder. Tutup aplikasi sebelum menyalin seluruh folder ke PC lain; launcher memeriksa runtime di PC tujuan kembali.

**Upgrade dari 2.2/2.3:** pasang Desktop Runtime x86 lebih dulu; updater lama menunda pemasangan jika runtime belum ada karena memakai mode silent. Alternatif: ekstrak ZIP baru saat aplikasi tertutup, lalu buka launcher baru untuk panduan runtime.

Baca [panduan pengujian](TEST-PORTABLE.md), juga tersedia dalam paket. Windows Application Control tetap mengikuti kebijakan penerbit tepercaya; aplikasi belum memiliki sertifikat Authenticode publik.

Repo ini hanya untuk rilis aplikasi. Jangan unggah data jemaah, hasil scan, konfigurasi pengguna atau API key.
