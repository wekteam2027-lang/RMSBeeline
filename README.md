# RMS WebView Android Project (ready for GitHub Actions build)

This archive contains a minimal Android (Kotlin) project that opens https://rms.beeline.uz/ in a WebView.
Also includes a GitHub Actions workflow that will build an APK in the cloud.

## Steps for a beginner: upload to GitHub and build APK

1. Create a GitHub account at https://github.com (if you don't have one).
2. Create a new repository (click New repository) and name it, e.g. `RMSApp`.
3. On the repository page, click **Add file → Upload files**.
4. Drag & drop the *entire contents* of this ZIP (all folders/files) into the upload area, or upload this ZIP after extracting.
5. Commit the changes (at bottom: Commit changes).
6. Go to the **Actions** tab in your repo. You'll see the workflow "Build Android APK".
7. Click it and then click **Run workflow** (or push to the main branch to trigger automatically).
8. Wait a few minutes for the workflow to finish.
9. Open the latest workflow run, scroll to the **Artifacts** section, download `RMS-App.zip`.
10. Inside the ZIP you'll find `app-debug.apk` — install it on your Android device.

## If the workflow fails to find gradle/gradlew:
- The workflow tries `./gradlew assembleDebug` first; if gradlew is missing it runs `gradle assembleDebug` using the gradle action which provides gradle binary.
- If any error appears, copy the error message and send it to me — I'll help.

## Want a release-signed APK?
I can add steps to generate a signed release APK (requires a keystore and GitHub Secrets). Ask me and I'll add it.
