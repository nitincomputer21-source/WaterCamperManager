# Water Camper Manager Android APK

## Features
- Android WebView app containing the supplied Water Camper Manager.
- Excel (.xlsx/.xls) and CSV import from Android's file picker.
- Preview before importing rows.
- Customer, delivery, payment and settings data stored in WebView localStorage on the phone.
- CSV report and full JSON backup saved to `Downloads/WaterCamper`.
- Restore full JSON backup from a file on the phone.

## Build APK with GitHub Actions
1. Upload all files and folders in this project to the root of your GitHub repository.
2. Commit to `main` (or `master`).
3. Open the repository's **Actions** tab.
4. Select **Build Water Camper APK** and choose **Run workflow**, or let the push trigger it.
5. Open the completed workflow run, scroll to **Artifacts**, and download `Water-Camper-Manager-APK`.
6. Extract the downloaded ZIP and install `app-debug.apk` on your Android phone.

## Important data notes
- The database is stored locally inside the app's WebView storage. It remains across normal app closes/restarts, but uninstalling the app or clearing app storage can erase it.
- Use **पूरा डेटा बैकअप डाउनलोड करें** regularly and keep a copy outside the phone.
- CSV reports and JSON backups are saved by the Android app to `Downloads/WaterCamper`.
- Excel parsing currently loads SheetJS from jsDelivr, so internet is required when opening/importing Excel. The rest of the app's UI and stored data are local.
- This is a debug APK for testing. A release APK should be signed with a private keystore before distribution.
