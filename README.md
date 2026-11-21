# FIRE IPTV Official Website

A responsive Arabic-first landing website built from the supplied FIRE IPTV Android project assets. Includes project overview, verified project feature descriptions, screenshots, download section, Firebase-backed moderated reviews, and a basic admin sign-in entry point.

## What was confirmed from the supplied Android project
- App name: FIRE IPTV
- Version: 1.0.0 (versionCode 1)
- Android minimum: API 24 / Android 7.0
- Application ID: `com.aistudio.fireiptv.mnxehb`
- Project metadata describes Media3 ExoPlayer, Xtream Codes, Stalker MAC Portal, M3U, and FGCode.
- Screens for Live TV, Movies, Series, and Kids are present.

## Run locally

```bash
npm install
cp .env.example .env
npm run dev
```

Add Firebase Web App configuration values to `.env`. Create a Cloud Firestore database and publish `firestore.rules` from Firebase Console. Public submissions are stored as `pending`; only approved reviews are publicly readable. The admin custom claim `admin: true` must be assigned securely using Firebase Admin SDK in a trusted environment. Never assign admin claims from the browser.

## APK download

The supplied archive is an Android source project; it does not contain a ready-to-download APK. Build and sign a release APK in Android Studio, upload it to a trusted host, then set `VITE_APK_URL` in `.env` to its direct URL and rebuild.

## Important

The first version intentionally does not invent a download link, file size, release date, rating count, or unimplemented app features. The Firebase review form requires valid Firebase configuration before it can submit or display live reviews.
