# Kaharian Sentinel — Android TWA Project

## What is this?
This is a **Trusted Web Activity (TWA)** Android project that wraps your PWA at
`https://sentinel.kaharian.com` into a native Android app for the Google Play Store.

---

## Quick Setup

### Step 1 — Place assetlinks.json on your server
Upload `assetlinks.json` to your web server so it's accessible at:
```
https://sentinel.kaharian.com/.well-known/assetlinks.json
```
This verifies that your app "owns" the domain. Without this, the browser URL bar will show inside the app.

**In Plesk:**
1. Go to File Manager for `sentinel.kaharian.com`
2. Create folder `.well-known` in the root (public_html or httpdocs)
3. Upload `assetlinks.json` into it
4. Verify: https://sentinel.kaharian.com/.well-known/assetlinks.json

---

### Step 2 — Open in Android Studio
1. Download and install [Android Studio](https://developer.android.com/studio)
2. Open this folder as a project
3. Wait for Gradle sync to complete

### Step 3 — Build the APK
- **Debug APK:** Build > Build Bundle(s)/APK(s) > Build APK(s)
- **Release AAB (for Play Store):** Build > Generate Signed Bundle/APK

### Step 4 — Signing Credentials (KEEP THESE SAFE!)
```
Keystore file:  sentinel-release.keystore
Alias:          sentinel
Store password: Sentinel2026!
Key password:   Sentinel2026!
SHA-256:        3C:2F:50:68:7E:35:F8:8D:52:DB:42:9A:C3:CF:67:3D:42:F1:41:B3:73:C4:AA:D6:7A:8C:1B:81:7F:49:BC:B3
```
⚠️ BACK UP sentinel-release.keystore securely. If you lose it, you cannot update the app on Play Store.

---

### Step 5 — Submit to Google Play
1. Go to https://play.google.com/console
2. Create a new app (Health & Fitness category)
3. Upload the signed AAB
4. Fill in store listing (use your Sentinel app description)
5. Submit for review (usually 1–3 days)

---

## App Details
| Field | Value |
|---|---|
| Package ID | com.kaharian.sentinel |
| App Name | Kaharian Sentinel |
| Short Name | Sentinel |
| Target URL | https://sentinel.kaharian.com |
| Min Android | 5.0 (API 21) |
| Theme Color | #D4AF37 (gold) |
| Background | #121212 (dark) |

---

## Updating the App
Since this is a TWA, **you don't need to republish to Play Store for content updates**.
Any changes you make in Lovable.dev automatically appear in the app.
You only need to republish if you change the package name, permissions, or native code.

