# Monitoring EXP — Aurora Edition 3.0

Aplikasi Android untuk memantau tanggal expired, scan barcode, membuat alarm, dan mengirim laporan.

## Fitur
- Dashboard Aurora modern
- Logo **Monitoring EXP**
- Produk + barcode + tanggal expired
- Google Code Scanner
- Alarm otomatis H-30, H-7, H-1 dan Hari H pukul 08:00
- Alarm custom tanggal + jam
- Suara alarm Android + getar + notifikasi prioritas tinggi
- Layar alarm fullscreen dengan Snooze 10 menit / Matikan
- Penjadwalan ulang alarm setelah restart / perubahan waktu
- Export CSV
- Backup JSON
- Kirim laporan expired melalui aplikasi email/share
- GitHub Actions untuk build APK debug

## Membuka project
1. Extract ZIP.
2. Buka folder `MonitoringEXP_Aurora_v3` di Android Studio.
3. Pastikan Android SDK 35 dan JDK 17 tersedia.
4. Gradle Sync.
5. Run ke emulator/HP Android.

## Izin penting
Pada Android 13+, izinkan notifikasi.
Pada Android 12+, jika ingin alarm benar-benar tepat waktu, izinkan **Alarms & reminders** dari Pengaturan Android. Jika tidak diizinkan, aplikasi memakai alarm non-exact sebagai fallback.

## GitHub
Buat repository baru, lalu:
```bash
git init
git add .
git commit -m "Monitoring EXP Aurora 3.0"
git branch -M main
git remote add origin https://github.com/USERNAME/MonitoringEXP.git
git push -u origin main
```

Workflow `.github/workflows/android.yml` akan membangun APK debug setiap push ke `main`/`master`.

## Catatan
Versi ini menggunakan Java + AppCompat dan Google Code Scanner. Email menggunakan Android share/email intent sehingga pengguna memilih akun/aplikasi email. Tidak ada password email yang ditanam di aplikasi.
