# Jadwal Sholat

Aplikasi Flutter untuk menampilkan jadwal sholat dengan fitur lengkap termasuk kalibrasi waktu, pengaturan audio, dan arah kiblat.

## Fitur

- **Jadwal Sholat Real-time**: Menampilkan jadwal sholat untuk lokasi Anda
- **Kalender 30 Hari**: Lihat jadwal sholat untuk 30 hari ke depan
- **Kalibrasi Waktu**: Sesuaikan waktu sholat sesuai kebutuhan Anda
- **Pengaturan Audio**: Atur volume dan pilih audio untuk adzan dan sholawat
- **Auto Play**: Putar adzan dan sholawat secara otomatis
- **Arah Kiblat**: Temukan arah kiblat dari lokasi Anda
- **Manajemen Lokasi**: Pilih lokasi otomatis atau manual

## Instalasi

### Prerequisites
- Flutter SDK (versi 3.0.0 atau lebih tinggi)
- Dart SDK
- Android Studio atau Xcode (untuk development)

### Setup

1. Clone repository
```bash
git clone <repository-url>
cd jadwal_sholat
```

2. Install dependencies
```bash
flutter pub get
```

3. Setup Android (jika diperlukan)
```bash
cd android
./gradlew build
cd ..
```

4. Run aplikasi
```bash
flutter run
```

## Struktur Project

```
lib/
├── main.dart                 # Entry point aplikasi
├── theme/
│   └── app_theme.dart       # Tema aplikasi
├── models/
│   └── prayer_time.dart     # Model data jadwal sholat
├── providers/
│   ├── prayer_provider.dart # Provider untuk jadwal sholat
│   └── settings_provider.dart # Provider untuk pengaturan
├── services/
│   ├── prayer_service.dart  # Service untuk API jadwal sholat
│   └── audio_service.dart   # Service untuk audio
├── screens/
│   ├── home_screen.dart     # Layar utama
│   ├── calendar_screen.dart # Layar kalender 30 hari
│   ├── location_screen.dart # Layar pengaturan lokasi
│   ├── qibla_screen.dart    # Layar arah kiblat
│   ├── settings_screen.dart # Layar pengaturan
│   ├── calibration_screen.dart # Layar kalibrasi waktu
│   ├── audio_management_screen.dart # Layar manajemen audio
│   └── default_audio_screen.dart # Layar pilih audio default
└── widgets/
    └── prayer_card.dart     # Widget kartu jadwal sholat
```

## API

Aplikasi menggunakan API dari [Aladhan](https://aladhan.com/api) untuk mendapatkan jadwal sholat.

## Dependencies

- `intl`: Untuk format tanggal dan waktu
- `geolocator`: Untuk mendapatkan lokasi pengguna
- `geocoding`: Untuk reverse geocoding
- `http`: Untuk HTTP requests
- `shared_preferences`: Untuk menyimpan preferensi pengguna
- `just_audio`: Untuk memutar audio
- `permission_handler`: Untuk mengelola permissions
- `provider`: Untuk state management

## Lisensi

MIT License

## Kontribusi

Silakan buat pull request untuk kontribusi.

## Support

Untuk pertanyaan atau masalah, silakan buat issue di repository ini.
