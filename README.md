# Task Manager - Flutter Todo App

<div align="center">

![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white)

Aplikasi manajemen tugas (task manager) yang dibangun menggunakan Flutter dengan database lokal SQLite untuk membantu Anda mengorganisir aktivitas harian dengan lebih efektif.

**Kelompok 2 - PBP (E) 2025**  
**Universitas Diponegoro**

</div>

---

## 📱 Tentang Aplikasi

Task Manager adalah aplikasi mobile dan desktop yang memungkinkan pengguna untuk mengelola tugas-tugas harian mereka dengan mudah. Aplikasi ini menggunakan SQLite sebagai database lokal untuk menyimpan data secara persisten, sehingga data tidak akan hilang meskipun aplikasi ditutup.

### ✨ Fitur Utama

- ✅ **Manajemen Tugas Lengkap**: Tambah, edit, dan hapus tugas dengan mudah
- 📋 **Sistem Prioritas**: Kategorikan tugas berdasarkan prioritas (High, Medium, Low)
- 📅 **Pencatatan Tanggal**: Otomatis mencatat tanggal pembuatan/modifikasi tugas
- ✔️ **Status Tugas**: Tandai tugas sebagai selesai atau belum selesai
- 📊 **Riwayat Tugas**: Lihat daftar tugas yang telah diselesaikan
- ⚙️ **Pengaturan**: Halaman pengaturan untuk kustomisasi aplikasi
- 🎨 **UI Modern**: Interface yang bersih, responsif, dan user-friendly
- 💾 **Penyimpanan Lokal**: Data tersimpan secara lokal menggunakan SQLite

---

## 📂 Struktur Project

```
flutter-todoapp/
│
├── lib/
│   ├── helpers/
│   │   └── database_helper.dart       # Helper untuk operasi database SQLite
│   │
│   ├── models/
│   │   └── task_model.dart            # Model data Task (id, title, description, dll)
│   │
│   ├── screens/
│   │   ├── splash_screen.dart         # Splash screen dengan logo aplikasi
│   │   ├── home_screen.dart           # Halaman utama - daftar tugas aktif
│   │   ├── add_task_screen.dart       # Halaman tambah/edit tugas
│   │   ├── history_screen.dart        # Halaman riwayat tugas selesai
│   │   └── settings_screen.dart       # Halaman pengaturan aplikasi
│   │
│   └── main.dart                      # Entry point aplikasi
│
├── assets/                            # Folder untuk gambar dan asset lainnya
├── test/                              # Folder untuk unit testing
├── android/                           # Konfigurasi platform Android
├── ios/                               # Konfigurasi platform iOS
├── web/                               # Konfigurasi platform Web
├── windows/                           # Konfigurasi platform Windows
├── linux/                             # Konfigurasi platform Linux
├── macos/                             # Konfigurasi platform macOS
│
├── pubspec.yaml                       # Dependencies dan metadata project
└── README.md                          # Dokumentasi project
```

---

## 🛠️ Teknologi yang Digunakan

| Teknologi         | Versi   | Deskripsi                           |
| ----------------- | ------- | ----------------------------------- |
| **Flutter**       | 3.0+    | Framework UI cross-platform         |
| **Dart**          | 2.17+   | Bahasa pemrograman                  |
| **sqflite**       | ^2.3.0  | Database SQLite untuk Flutter       |
| **path_provider** | ^2.1.0  | Akses ke direktori sistem file      |
| **intl**          | ^0.18.0 | Internationalization dan formatting |

---

## 🚀 Cara Menjalankan Project

### Prerequisites

Pastikan Anda telah menginstall:

- [Flutter SDK](https://flutter.dev/docs/get-started/install) (versi 3.0 atau lebih baru)
- [Dart SDK](https://dart.dev/get-dart) (biasanya sudah termasuk dalam Flutter)
- [Android Studio](https://developer.android.com/studio) atau [VS Code](https://code.visualstudio.com/)
- [Git](https://git-scm.com/downloads)

**Untuk platform tertentu:**

- **Android**: Android SDK dan Android Emulator
- **iOS**: Xcode (hanya untuk macOS)
- **Web**: Google Chrome
- **Windows**: Visual Studio 2022 dengan Desktop development dengan C++
- **Linux**: GTK 3.0+ development libraries

### Langkah Instalasi

1. **Clone atau Download Project**

   ```bash
   # Clone repository (jika menggunakan Git)
   git clone <repository-url>

   # Atau ekstrak file ZIP jika diunduh
   ```

2. **Navigasi ke Direktori Project**

   ```bash
   cd "c:\Learning Space\Coding Space\pbpFlutter-todoapp\flutter-todoapp"
   ```

3. **Verifikasi Instalasi Flutter**

   ```bash
   flutter doctor -v
   ```

   Pastikan tidak ada error kritis. Periksa:

   - ✓ Flutter (Channel stable)
   - ✓ Android toolchain (untuk Android)
   - ✓ Chrome (untuk Web)
   - ✓ Visual Studio (untuk Windows)

4. **Install Dependencies**

   ```bash
   flutter pub get
   ```

5. **Cek Perangkat yang Tersedia**

   ```bash
   flutter devices
   ```

   Output akan menampilkan daftar devices yang tersedia:

   ```
   3 connected devices:
   Windows (desktop) • windows • windows-x64    • Microsoft Windows
   Chrome (web)      • chrome  • web-javascript • Google Chrome
   Edge (web)        • edge    • web-javascript • Microsoft Edge
   ```

### Menjalankan Aplikasi

#### **Untuk Windows Desktop:**

```bash
flutter run -d windows
```

#### **Untuk Web Browser:**

```bash
# Chrome
flutter run -d chrome

# Edge
flutter run -d edge
```

#### **Untuk Android:**

```bash
# Pastikan emulator sudah berjalan atau device terhubung
flutter run

# Atau spesifik ke Android
flutter run -d android
```

#### **Mode Development dengan Hot Reload:**

```bash
flutter run --hot
```

Hot reload memungkinkan Anda melihat perubahan kode secara real-time tanpa restart aplikasi.

---

## 📦 Build untuk Production

### Build APK untuk Android

```bash
# Build APK debug
flutter build apk --debug

# Build APK release (ukuran lebih kecil, performa lebih baik)
flutter build apk --release

# Build APK split per ABI (menghasilkan file lebih kecil)
flutter build apk --split-per-abi --release
```

File APK akan tersimpan di: `build/app/outputs/flutter-apk/`

### Build untuk Web

```bash
flutter build web --release
```

File web akan tersimpan di: `build/web/`

### Build untuk Windows

```bash
flutter build windows --release
```

File executable akan tersimpan di: `build/windows/runner/Release/`

---

## 🗄️ Database Schema

Aplikasi menggunakan SQLite dengan skema berikut:

**Tabel: tasks**

| Kolom         | Tipe Data | Deskripsi                               |
| ------------- | --------- | --------------------------------------- |
| `id`          | INTEGER   | Primary Key (Auto Increment)            |
| `title`       | TEXT      | Judul tugas                             |
| `description` | TEXT      | Deskripsi detail tugas                  |
| `priority`    | TEXT      | Prioritas: "High", "Medium", atau "Low" |
| `date`        | TEXT      | Tanggal pembuatan (format: MMM d, yyyy) |
| `status`      | INTEGER   | Status: 0 = belum selesai, 1 = selesai  |

**Lokasi Database:**

- **Android**: `/data/data/com.example.pbp_project_flutter/databases/tasks.db`
- **Windows**: `%APPDATA%/com.example.pbp_project_flutter/tasks.db`

---

## 🎨 Fitur Detail

### 1. Splash Screen

- Tampilan awal aplikasi dengan delay 3 detik
- Menampilkan logo dan nama aplikasi
- Transisi smooth ke halaman utama

### 2. Home Screen

- Menampilkan daftar semua tugas yang belum selesai
- Filter berdasarkan prioritas
- Floating action button untuk menambah tugas baru
- Checkbox untuk menandai tugas selesai
- Swipe atau tap untuk edit/hapus

### 3. Add/Edit Task Screen

- Form input untuk judul dan deskripsi tugas
- Dropdown untuk memilih prioritas
- Tombol Save untuk menyimpan
- Tombol Delete untuk menghapus (saat edit)
- Validasi input otomatis

### 4. History Screen

- Menampilkan semua tugas yang sudah selesai
- Informasi tanggal penyelesaian
- Opsi untuk mengembalikan ke daftar aktif

### 5. Settings Screen

- Pengaturan tema aplikasi (coming soon)
- Pengaturan notifikasi (coming soon)
- Informasi tentang aplikasi

---

## 🐛 Troubleshooting

### Error: "Flutter SDK not found"

```bash
# Pastikan Flutter sudah terinstall dan ada di PATH
flutter doctor -v

# Jika belum, tambahkan Flutter ke PATH atau install ulang
```

### Error: "Gradle build failed"

```bash
# Clean project dan rebuild
flutter clean
flutter pub get
cd android
./gradlew clean
cd ..
flutter run
```

### Error: "SQLite database locked"

```bash
# Restart aplikasi atau clear data aplikasi
flutter clean
flutter run
```

### Error: "Could not find package"

```bash
# Update dependencies
flutter pub upgrade

# Atau install ulang
flutter pub get
```

### Aplikasi lag atau lambat

```bash
# Build dalam mode release untuk performa maksimal
flutter run --release
```

### Hot Reload tidak bekerja

```bash
# Restart aplikasi dengan hot restart
# Tekan 'R' di terminal saat aplikasi berjalan

# Atau restart penuh
# Tekan 'r' (lowercase) di terminal
```

---

## 📝 Catatan Pengembangan

### Dependencies

Berikut adalah dependencies yang digunakan dalam project:

```yaml
dependencies:
  flutter:
    sdk: flutter
  sqflite: ^2.3.0 # SQLite database
  path_provider: ^2.1.0 # File system paths
  intl: ^0.18.0 # Date formatting
  cupertino_icons: ^1.0.2 # iOS style icons

dev_dependencies:
  flutter_test:
    sdk: flutter
  flutter_lints: ^2.0.0 # Linting rules
```

### Command yang Berguna

```bash
# Menjalankan tests
flutter test

# Analyze kode
flutter analyze

# Format kode
flutter format lib/

# Lihat outdated packages
flutter pub outdated

# Update packages
flutter pub upgrade

# Generate app bundle (Android)
flutter build appbundle
```

---

## 🔄 Versi

### v1.0.0 (December 2025)

- ✅ Initial release
- ✅ CRUD operations untuk tugas
- ✅ Sistem prioritas tugas
- ✅ Riwayat tugas selesai
- ✅ Database SQLite lokal
- ✅ Support multi-platform (Android, iOS, Web, Windows, Linux, macOS)

### Future Updates (Insyaallah 🙏)

- 🔔 Notifikasi reminder
- 🌙 Dark mode
- 📊 Statistik produktivitas
- 🔐 Pin/password protection
- ☁️ Cloud sync
- 📤 Export/import data

---

## 👥 Kontributor

**Kelompok 2 - PBP (E) 2025**  
**Fakultas Sains dan Matematika**  
**Universitas Diponegoro**

---

## 📄 Lisensi

© 2025 Kelompok 2 - PBP (E) Universitas Diponegoro

Project ini dibuat untuk keperluan pembelajaran mata kuliah Pemrograman Berbasis Platform.

---

## 📞 Kontak & Dukungan

Jika Anda mengalami masalah atau memiliki pertanyaan:

1. Buka **Issues** di repository ini
2. Hubungi anggota kelompok
3. Konsultasi dengan dosen pengampu

---

## 🙏 Acknowledgments

- Flutter Team untuk framework yang luar biasa
- Dosen pengampu PBP Universitas Diponegoro
- Komunitas Flutter Indonesia
- Stack Overflow dan dokumentasi Flutter

---

<div align="center">

**Made with ❤️ by Kelompok 2 PBP (E) 2025**

[Universitas Diponegoro](https://www.undip.ac.id/)

</div>
