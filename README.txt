MOMENTS STUDIO — GALLERY + INSTAGRAM UPDATE

This package updates the existing Moments Studio editor.

1. Replace the repository root index.html with this package's index.html.
2. If your repository also uses www/index.html for Capacitor, replace that file with www/index.html from this package.
3. Commit the changes and redeploy GitHub Pages.

New behaviour:
- Save to Gallery creates the edited 1080x1920 JPEG and opens the iOS share sheet when supported. On iPhone/iPad, choose “Save Image” to place it in Photos. If file sharing is unavailable, it downloads to Files.
- Open Instagram launches the Instagram app when installed, otherwise it falls back to Instagram's website.
- Instagram does not receive or post the photo automatically. Choose the saved photo inside Instagram.

Note: A browser website cannot silently write directly into the iOS Photos library. Direct Photos saving without the share sheet requires a native iOS app implementation with photo-library permissions.
