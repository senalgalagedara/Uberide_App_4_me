RIDE PROFIT - Android app (Capacitor)

YOU NEED (one time, on a PC/Mac/Linux):
  1. Node.js (LTS)        https://nodejs.org
  2. Android Studio       https://developer.android.com/studio

STEPS (run in this folder):
  npm install @capacitor/core @capacitor/android
  npm install -D @capacitor/cli
  npx cap add android
  npx cap sync android
  npx cap open android

In Android Studio (wait for Gradle sync to finish):
  - Test: plug in your phone (USB debugging on) and press the green Run button.
  - Make an APK to install: Build > Build Bundle(s) / APK(s) > Build APK(s)
    The file appears under android/app/build/outputs/apk/debug/app-debug.apk
    Send it to your phone and open it (allow "install unknown apps").

AFTER YOU CHANGE www/index.html:
  npx cap sync android   (then Run / Build again)

NOTES:
  - Rides and settings are stored inside the app on that phone.
    Data from the browser version does NOT carry over.
  - Uninstalling the app erases its data.

--- BUILD IN THE CLOUD WITH GITHUB (no Android tools needed) ---
  1. Make a free account at github.com and create a new PRIVATE repository.
  2. Upload this whole folder (including the hidden .github folder) to it, on the main branch.
  3. Open the repo > Actions tab > "Build Android APK" > wait about 5-8 minutes for the green tick.
  4. Click the finished run > Artifacts > ride-profit-apk > download, unzip, install app-debug.apk on your phone.
