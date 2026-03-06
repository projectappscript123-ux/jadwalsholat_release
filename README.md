# Release Notes - Jadwal Sholat

## Version 1.8.4 (Build 29)
**Release Date:** 7 Maret 2026

### 🐛 Bug Fixes
- Fix bug kalender Hijriah: urutan tanggal yang salah (30 Ramadan → 30 Shawwal → 2 Shawwal) sudah diperbaiki
- Fix bug Sahur tidak auto play: waktu tambahan (Sahur, Imsak, Terbit, Dhuha) yang sudah lewat hari ini sekarang otomatis dijadwalkan untuk besok dengan data akurat dari kalender 30 hari

### 🎵 Audio Management
- Pisahkan folder MP3 waktu tambahan ke `audio/tambahan/` (terpisah dari `audio/sholawat/`)
- Default audio waktu tambahan diubah ke Surat Al-Baqarah Ayat 284-286
- Default sholawat setelah adzan tetap TARHIM (tidak berubah)

### 🔧 Technical Updates
- Perbaiki logika visibilitas hilal yang menyebabkan tanggal stuck
- Fix overflow adjustment menggunakan while loop
- Fix type comparison error: DateTime sekarang dibandingkan dengan benar

### 📱 Platform Support
- Android: minSdk 29, targetSdk 36
- iOS: 11.0+

---
