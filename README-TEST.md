# Moments Studio — Direct Instagram Launch Test

This package uses the user's original Moments Studio editor and changes only the Instagram button behavior.

## What this test does
- Tapping **Instagram Story** attempts to open `instagram-stories://share` on a compatible mobile device.
- If the browser remains on the page, it asks whether to open Instagram's website.
- It does NOT transfer the edited photo into Instagram. A normal web page cannot write the required iOS pasteboard item for Meta's Stories handoff.
- WhatsApp continues to use the Web Share API and may show the iOS share sheet.

## Replace files in GitHub
1. Replace repository root `index.html` with this package's `index.html`.
2. Replace `www/index.html` with this package's `www/index.html`.
3. Commit changes and wait for GitHub Pages deployment.
4. Open the GitHub Pages site in Safari on an iPhone/iPad with Instagram installed.
5. Select a test photo and tap Instagram Story. Record whether Instagram opens, whether it opens Story Composer, or whether it shows an error.

## Full photo handoff
Meta's documented Instagram Stories sharing flow requires a native iOS/Android integration. On iOS, the app writes the image bytes to UIPasteboard using the `com.instagram.sharedSticker.backgroundImage` key, then opens `instagram-stories://share?source_application=...`. A website alone cannot perform that native iOS pasteboard operation.
