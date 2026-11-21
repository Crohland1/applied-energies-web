# Applied Energies offline web app (Apple / Android / desktop)

This version is derived from the supplied Applied Energies Android HTML app and retains its report form, multi-page patterns, calculations, threshold coloring, manual coloring, backup/restore, and browser print support.

## Publish from your phone using GitHub Pages
1. Create a NEW public GitHub repository for the web version (do not overwrite the Android project).
2. Upload all files in this folder to the repository root.
3. Open Settings → Pages → Build and deployment → Deploy from a branch → main / (root) → Save.
4. Open the published HTTPS URL in iPhone Safari. Use Share → Add to Home Screen.
5. Open once while online; after the first successful load, the service worker caches the app for offline use. Test offline before relying on it.

## Share an editable report
Open or fill in a report → Share Editable Report. On supported devices the native share sheet opens; otherwise a .json file downloads. Send this file to another employee. They open the web app → Import Editable Report → select the JSON file. Imports always create a separate saved copy; they never overwrite an existing report.

## Important limits
- Local device/browser storage is not cloud sync and may be erased. Export Backup regularly and store copies somewhere safe.
- Safari's print dialog can Save to Files as PDF; it does not necessarily provide editable PDF form fields. Editable sharing is via JSON.
- The web app cannot call the Android-only native print bridge; it uses browser print. Verify multi-page printing and PDF layout on target Apple devices.
- Service worker requires HTTPS (GitHub Pages provides it); opening index.html directly from Files will not install an offline PWA.
- This is a prepared implementation, not a verified live deployment or iPhone-tested release.
