# Release Notes - Jadwal Sholat

## Version 1.8.4 (Build 28)
**Release Date:** 4 Maret 2026

### 🎉 What's New
- Update versi aplikasi ke 1.8.4

### 🔧 Technical Updates
- Build number dinaikkan ke 28
- Sinkronisasi versi di semua platform (Android, iOS, dan konfigurasi aplikasi)

### 📱 Platform Support
- Android: minSdk 29, targetSdk 36
- iOS: 11.0+

---

## Version 1.8.3 (Build 27)

### 🚀 Major Changes
**Migrasi ke Google Sheets API**
- Aplikasi sekarang menggunakan Google Sheets sebagai sumber data tunggal untuk jadwal sholat dan imsyakiyah
- Menggantikan perhitungan Ephemeris lokal dengan data langsung dari spreadsheet
- Data TERBIT dan DHUHA diambil langsung dari Google Sheets

### ⚡ Performance Improvements
- Implementasi cache system (5 menit) untuk performa optimal
- Support offline mode dengan cache terakhir
- Auto-refresh otomatis untuk data terbaru

### 📅 Data Availability
- Data tersedia sampai Maret 2027
- Update otomatis dari Google Sheets

### 🔒 Security Enhancements
- Keamanan credentials dengan multiple layers protection
- .gitignore dan .gitattributes untuk proteksi file sensitif
- Pre-commit hook untuk mencegah commit credentials

---

## Version 1.8.2 (Build 26)

### 🐛 Bug Fixes
- Waktu tambahan (Sahur, Imsak, Terbit, Dhuha) sekarang memperhitungkan kalibrasi waktu dari menu pengaturan
- Card waktu tambahan menggunakan window 30 menit sebelum dan sesudah dengan prioritas pada waktu yang lebih dekat

### 🔧 Technical Improvements
- Gradle deprecated syntax diperbaiki untuk kompatibilitas Gradle 9.0
- Build script ditambahkan flag --warning-mode all untuk debugging

---

## Version 1.8.1 (Build 25)

### 🔄 Major Updates
**Perhitungan Lokal 100%**
- Hapus semua API Aladhan
- Implementasi perhitungan lokal menggunakan Ephemeris
- Kriteria Kemenag RI permanen (Subuh 20°, Isya 18°, Syafi'i)

### 📆 Kalender Hijriah
- Kalender Hijriah Rukyatul Hilal Global
- Koreksi Ramadan 1447 H (19 Feb 2026)
- Menu Perhitungan Kalender Hijriah dengan penyesuaian tanggal ±5 hari

### ⏱️ Real-Time Countdown & Widget
- HomeScreen ganti ValueNotifier<int> ke ValueNotifier<DateTime> untuk update real-time setiap detik
- Countdown card hitung manual real-time (bukan dari provider cache)
- Efek kedip countdown (tampil 700ms hilang 300ms)
- Widget Android tambah next prayer name di countdown (format: SUBUH 05:30:45)
- Enhanced widget logging untuk debugging
- Multiple SharedPreferences fallback untuk kompatibilitas Android 10-16
- Auto-detect date change untuk refresh data sholat di tengah malam

---

## Version 1.8.0 (Build 24)

### 🐛 Critical Fixes
**Real-Time Update**
- Fix countdown widget dan data widget (jam, tanggal) sekarang update real-time setiap detik
- Fix countdown tidak bergerak dengan perhitungan manual real-time
- Fix countdown 00:00:00 saat adzan dengan auto-skip ke prayer berikutnya
- Tambah tanda "-" sebelum countdown (format: - HH:MM:SS)

### 🔧 Optimizations
- Tambah deteksi perubahan tanggal otomatis untuk refresh data sholat di tengah malam
- Optimasi timer lifecycle management dengan error handling dan mounted checks

---

## Version 1.7.9 (Build 23)

### 🐛 Critical Fixes
- Fix ForegroundServiceDidNotStartInTimeException crash di Android 15
- startForeground dipanggil segera dalam 1-2 detik
- Fix card normal tidak muncul setelah adzan/iqamah selesai
- Native Android sekarang clear SharedPreferences dengan benar via clearDartAudioState

### 🎵 Audio Lifecycle
- Enhanced audio lifecycle management dengan proper cleanup
- Auto-stop timer di onCompletion, onError, dan onDestroy

---

## Version 1.7.8 (Build 22)

### 🔔 Notification Improvements
- Notifikasi bar menggunakan MediaStyle seperti pemutar MP3
- Logo aplikasi sebagai large icon
- Background color (orange untuk sholawat, merah untuk adzan)
- Tap body notifikasi membuka aplikasi tanpa stop audio
- Tombol STOP tetap berfungsi untuk stop audio dan clear notifikasi

---

## Version 1.7.7 (Build 21)

### 🎵 Background Audio & Notifications
- Implementasi MediaSession untuk lock screen controls
- Audio Focus management untuk handle konflik dengan app lain
- Notifikasi HIGH importance dengan MediaStyle
- Volume mengikuti pengaturan user dari menu settings
- Swipe-to-dismiss notification
- Enhanced logging untuk debugging

---

## Version 1.7.6 (Build 20)

### 🔄 Migration to WorkManager
- Mengganti android_alarm_manager_plus dengan WorkManager untuk kompatibilitas Android 15
- Perbaikan semua error kompilasi
- Cleanup code yang tidak digunakan
- Fix duplicate AlarmActivity di AndroidManifest

---

## Previous Versions

### Version 1.7.5 - Card Replacement Fixes
### Version 1.7.4 - Android 10-15 Setup Guide
### Version 1.7.3 - Permission Fixes
### Version 1.7.2 - Card & Dialog Improvements
### Version 1.7.1 - AndroidManifest Fix
### Version 1.7.0 - Android 15 Support
### Version 1.6.4 - Audio Management
### Version 1.6.3 - Version Update
### Version 1.6.2 - Background Audio Fixes
### Version 1.6.1 - Notification Optimization
### Version 1.6.0 - Hijri Calendar Implementation
### Version 1.5.6 - Auto Play Features
### Version 1.5.3 - Qibla Direction
### Version 1.5.2 - Performance Optimization
### Version 1.5.1 - Debug Logger
### Version 1.5.0 - Initial Release

---

## 📞 Contact & Support

**Developer:** Hikmal  
**Email:** hiikmall777@gmail.com  
**Company:** Jadwal Sholat Team  
**Website:** https://tokke-luwuutara.desa.id

---

## 🎯 Key Features

- ✅ Jadwal Sholat Real-time (Metode Kemenag RI)
- ✅ Kalender Hijriah (Rukyatul Hilal Global)
- ✅ Auto Play Adzan & Sholawat (Support Custom MP3)
- ✅ Kalibrasi Waktu Manual & Otomatis
- ✅ Arah Kiblat dengan Sensor Compass
- ✅ Upload & Kelola Audio Custom
- ✅ Kalender 30 Hari
- ✅ Lokasi Otomatis & Manual
- ✅ Background Alarm System
- ✅ Offline Support
- ✅ Google Sheets Integration
