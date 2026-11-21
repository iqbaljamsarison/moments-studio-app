# moments. — Hybrid Starter (Capacitor)

This starter prepares a local project structure for turning the existing Moments Studio website into an iOS/Android hybrid app.

## Important
- This is a starter shell, not the finished native app.
- The existing GitHub Pages site remains the current web demo.
- The current editor must be ported into `www/` before it is functionally equivalent.
- Instagram Story handoff requires a native iOS/Android integration and testing on real devices. This starter intentionally does not pretend a normal web link can inject an edited image into Instagram.
- Never ask users for their Instagram or WhatsApp passwords. Authentication must happen inside the official apps.

## Requirements
- Node.js 20+ recommended
- Xcode on a Mac for iOS builds
- Android Studio for Android builds

## Setup (computer required)
```bash
npm install
npm install @capacitor/ios @capacitor/android
npx cap add ios
npx cap add android
npm run build
npx cap sync
```

Open native projects:
```bash
npx cap open ios
npx cap open android
```

## Next implementation
1. Port the existing Moments Studio editor into `www/`.
2. Generate the edited Story as a JPEG/PNG Blob.
3. Write the image to a temporary native file.
4. Implement Instagram Stories sharing using Meta's supported iOS/Android sharing mechanism.
5. Implement WhatsApp sharing using the native share sheet / supported share intents.
6. Test fallback behavior when an app is absent or cannot receive the media.

A GitHub Pages static site cannot build and sign an iOS app. iOS builds require macOS/Xcode and Android builds require Android Studio.
