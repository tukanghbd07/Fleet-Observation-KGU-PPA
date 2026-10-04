# Fleet Observation KGU - Android

Android WebView wrapper for the Fleet Observation KGU generator.

## Features
- Uses the V7 Fleet Observation web generator inside an Android app.
- Upload ZIP / XLSX / JPEG / PNG through Android file picker.
- Supports KGU Utara / Tengah / Selatan, Shift 1 / Shift 2, hourly review and AVG.
- Native Android Print dialog for Save as PDF.
- Report layout and PPA/Climb to the Top branding are included.

## Build APK on GitHub Actions
Push this folder to a GitHub repository. The included workflow `.github/workflows/build-apk.yml` builds an installable debug APK automatically.
Download it from the workflow artifact named `Fleet-Observation-KGU-APK`.

## Local build
Requirements: Android SDK 35, Java 17, Gradle 8.9.
Run:

    gradle :app:assembleDebug

APK output:

    app/build/outputs/apk/debug/app-debug.apk

## Notes
The embedded web app currently loads JSZip, SheetJS/XLSX and Tesseract.js from CDN, so internet access is required when those libraries are first loaded.
