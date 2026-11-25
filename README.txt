APPLIED ENERGIES — AE APP ICON UPDATE

Revised design: the A keeps the company logo’s star-shaped arrow form. Its red arrow also serves as the middle stroke of the capital E. The full mark is red on black, centered with generous safe-area margin so Android round/rounded masks do not crop it. The app label is “Drilling and Blasting Tools.”

WEB / PWA
1. Copy icon-192.png, icon-512.png, and manifest.webmanifest into the same published folder as the app start page.
2. Ensure the page links to the manifest: <link rel="manifest" href="manifest.webmanifest">
3. Publish, then remove the old home-screen shortcut and install/add the app again so Android reloads the icon and app label.

ANDROID / CAPACITOR
Merge the android-res files into the matching Android res folders, replacing the existing launcher icon resources, then rebuild and reinstall the APK. Set the Android app/activity label to “Drilling and Blasting Tools.”

This package provides icon assets and configuration; it does not itself publish the web app or rebuild the APK.
