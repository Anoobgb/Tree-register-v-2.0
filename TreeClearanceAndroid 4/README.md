# Tree Clearance Register – Android Studio project

This is an Android WebView application source project for the Transmission Line Tree Clearance Register.

## Build an APK
1. Install Android Studio on a computer.
2. Open this folder (`TreeClearanceAndroid`) in Android Studio.
3. Allow Gradle sync and install the Android SDK Platform 35 if prompted.
4. Select **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
5. Android Studio will produce the debug APK under `app/build/outputs/apk/debug/`.

## Included
- Active and Completed locations
- Urgent location count for due dates within 7 days or overdue; tap to filter
- Tower From / Tower To, criticality days, inspection date and entry timestamp
- 13 tree species, quantity, per-tree clearance checkbox and timestamp
- Automatic location completion when all selected trees are cleared
- Due-date urgency styling and blinking alert under 3 days / overdue
- Separate Active and Completed CSV exports with access-code prompts
- Local storage on the Android device

## Important limitations
- This project is source code, not a compiled APK. This environment did not have Android SDK / Gradle available to compile and test an APK.
- Data is stored locally on the device; it does not sync between phones.
- The access-code prompts are client-side protection only, not production-grade security. A deployed Power Grid operational app should use authenticated access and a secure backend.
- CSV exports are Excel-compatible; they are not native XLSX workbooks.
- Existing browser prototype data is not automatically migrated into this Android app.


## Android WebView fixes

- Android dialogs now handle JavaScript prompts, alerts, and confirmations.
- CSV exports are saved through Android's Downloads provider on Android 10 and newer.
- Rebuild the APK after using this fixed project.
