# WARKOP POS SGL — Build APK Gratis via GitHub Actions

Project ini dapat dibuild di server GitHub Actions sehingga Android Studio tidak perlu dipasang di laptop.

## Yang perlu disiapkan
- Akun GitHub gratis.
- Repository GitHub untuk project ini. Untuk build gratis tanpa memakai kuota akun private, gunakan repository PUBLIC. GitHub menyatakan standard GitHub-hosted runners gratis untuk public repositories.

## Langkah
1. Buat repository baru di GitHub, misalnya `warkop-pos-sgl-android`.
2. Set repository menjadi **Public**.
3. Upload seluruh isi folder `WARKOP_POS_SGL_ANDROID_FREE` ke repository. File `.github/workflows/build-apk.yml` harus ikut terupload.
4. Pastikan struktur root repository terlihat seperti:

   ```text
   .github/workflows/build-apk.yml
   app/
   build.gradle
   settings.gradle
   gradle.properties
   ```

5. Masuk menu **Actions** pada repository.
6. Pilih workflow **Build Warkop POS SGL APK**.
7. Klik **Run workflow**. Workflow juga otomatis berjalan setiap ada push ke branch `main`.
8. Tunggu sampai job berstatus **Success**.
9. Buka hasil workflow tersebut dan pada bagian **Artifacts** download `WARKOP_POS_SGL-debug-apk`.
10. Di dalam artifact terdapat `app-debug.apk`.

## Konfigurasi aplikasi
- App: Warkop POS SGL
- Package: `com.krianapps.warkoppos.sgl`
- URL: `https://warkop-pos-single.netlify.app/`
- Camera: ditangani oleh native WebView file chooser
- Gallery/file picker: ditangani oleh native Android file chooser

## Catatan penting
- APK ini adalah build DEBUG untuk pengujian fungsi.
- Jangan gunakan APK debug sebagai paket penjualan final sebelum kita membuat signing/release APK.
- Jangan memasukkan MASTER_SECRET ke repository GitHub. Project Android ini hanya menunjuk ke URL Warkop POS.
- Tidak perlu Android Studio pada laptop untuk proses build ini.
