# Warkop POS SGL — Android Free Wrapper

Android Studio project for the Warkop POS SGL production URL:

https://warkop-pos-single.netlify.app/

App ID:
com.krianapps.warkoppos.sgl

The wrapper is designed to handle HTML `<input type="file">` uploads in a native Android WebView, including gallery/file picker and camera capture, plus downloads and printing.

## Build
1. Install the latest stable Android Studio and the required Android SDK.
2. Open this folder in Android Studio.
3. Let Gradle Sync complete.
4. Connect an Android phone with USB debugging or start an emulator.
5. Build > Build APK(s).
6. Install the generated APK on a physical Android phone.

## Important
- The app loads the live Warkop POS SGL website; do not replace the URL unless the production URL changes.
- The app requests CAMERA permission because the app needs camera capture for product images.
- Gallery/file selection uses Android's document picker; no broad photo-storage permission is required on modern Android.
- Notifications are only for download notifications and are not required for product image upload.
