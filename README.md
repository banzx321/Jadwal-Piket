# Jadwal Piket

Aplikasi Android untuk jadwal piket mingguan. Setiap orang memasang aplikasi ini di HP-nya sendiri, memilih namanya, lalu otomatis mendapat notifikasi di hari ia kebagian piket.

## Cara mendapatkan file APK

### Cara 1: GitHub (tanpa memasang apa pun di komputer)
1. Buat akun di github.com, lalu buat repository baru (misalnya `jadwal-piket`).
2. Klik **uploading an existing file**, lalu seret **semua isi** folder ini ke sana (termasuk folder `.github`), dan klik **Commit changes**.
   - Kalau folder `.github` tidak ikut terunggah (karena tersembunyi), buat file baru lewat **Add file → Create new file**, beri nama `.github/workflows/build-apk.yml`, lalu salin isi file tersebut ke situ.
3. Buka tab **Actions**. Proses build berjalan otomatis (sekitar 3–5 menit).
4. Setelah tanda centang hijau muncul, klik proses tersebut, lalu unduh **JadwalPiket-apk** di bagian *Artifacts*. Ekstrak zip-nya untuk mendapatkan `app-debug.apk`.

### Cara 2: Android Studio
1. Buka folder ini di Android Studio (**File → Open**).
2. Tunggu proses sinkronisasi Gradle selesai.
3. Pilih **Build → Build App Bundle(s) / APK(s) → Build APK(s)**. File APK ada di `app/build/outputs/apk/debug/`.

## Cara memakai
1. **Admin/ketua** membuka aplikasi dan menekan **Tambah anggota**: isi nama lalu pilih hari piketnya.
2. Buka menu **⋮ → Bagikan jadwal**, lalu kirim ke grup WhatsApp.
3. **Setiap anggota** memasang APK, menyalin pesan jadwal tadi, lalu membuka **⋮ → Impor jadwal** (kodenya otomatis tertempel) dan memilih namanya sendiri.
4. Atur **Jam pengingat** (bawaan 06.30). Di hari piketnya, HP anggota itu akan menampilkan notifikasi beserta nama rekan piketnya.
5. Tekan **Kirim notifikasi uji** untuk memastikan notifikasi sudah aktif.

Kalau jadwal berubah, admin cukup membagikan ulang jadwalnya dan anggota mengimpornya lagi.

## Tips agar pengingat tidak terlewat
- Izinkan **Notifikasi** saat aplikasi memintanya.
- Izinkan **Alarm & pengingat** (Android 12 ke atas) agar notifikasi muncul tepat waktu.
- Di HP Xiaomi, Oppo, Vivo, atau Realme: buka Pengaturan aplikasi → Baterai → pilih **Tanpa batasan**, dan aktifkan **Mulai otomatis**. Tanpa itu, sistem bisa menahan pengingat.

Butuh Android 8.0 ke atas.
