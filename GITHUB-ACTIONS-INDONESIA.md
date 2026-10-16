# Membuat APK Sonora melalui GitHub Actions

Workflow `.github/workflows/android-apk.yml` membangun APK debug bernama `Sonora.apk`
di GitHub Actions. Kamu tidak perlu memasang Android Studio, JDK, Gradle, atau Android SDK
di komputer lokal.

## Cara pakai

1. Buat repository baru di GitHub, misalnya `Sonora-Android`.
2. Ekstrak ZIP proyek ini di komputer.
3. Unggah **isi folder proyek** ke root repository GitHub, termasuk folder `.github`.
   Pastikan `settings.gradle.kts`, `build.gradle.kts`, dan folder `app` berada di root.
4. Buka tab **Actions** di repository. Jika diminta, aktifkan workflows.
5. Pilih workflow **Build Sonora APK**, klik **Run workflow**, lalu klik **Run workflow** lagi.
   Workflow juga berjalan otomatis saat ada push ke branch `main` atau `master`.
6. Tunggu sampai semua langkah selesai dengan tanda centang hijau.
7. Buka hasil run workflow, gulir ke bagian **Artifacts**, lalu unduh **Sonora-debug-APK**.
8. Ekstrak ZIP artifact. Di dalamnya terdapat `Sonora.apk`. Kirim APK ke HP Android dan instal.

## Catatan

- Workflow menghasilkan **APK debug untuk pengujian**, bukan APK release resmi.
- Build pertama bisa gagal jika dependensi upstream tidak tersedia atau ada masalah kompilasi.
  Buka log workflow untuk melihat error yang tepat.
- Workflow memasang Gradle 9.6.1 dan menjalankan Gradle secara langsung.
- Nama paket aplikasi Android internal masih dipertahankan agar perubahan nama tampilan
  tidak mengganggu referensi kode yang ada. Nama yang terlihat di launcher adalah Sonora.
- Jangan mengunggah keystore, token, atau rahasia ke repository publik.
