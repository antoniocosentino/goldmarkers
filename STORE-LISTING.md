# Chrome Web Store submission draft

## Name

Gmail Gold Markers

## Short description

Restore gold importance markers in Gmail.

## Detailed description

Prefer Gmail's gold importance markers? Gmail Gold Markers replaces the blue
important-message markers with gold ones.

- Works automatically when you open Gmail.
- Preserves Gmail's importance controls and tooltips.
- Uses a bundled icon, with no external image downloads.
- No settings or additional account required.
- Does not collect or transmit your data.

After installation, reload any open Gmail tabs to apply the change.

This extension changes the appearance of importance markers. Gmail continues to
control which messages are important. Gmail interface updates may affect
compatibility.

An independent extension, not affiliated with or endorsed by Google.

## Single purpose

Restore the gold appearance of important-message markers in Gmail.

## Site access justification

Access to https://mail.google.com/* is needed to automatically apply a local CSS
stylesheet that replaces the background image of importance markers. The
extension contains no JavaScript and does not read, collect, or transmit email
content or other user data.

## Privacy declarations

- No user data is collected or transferred.
- No remote code is used.
- No additional API permissions are requested.
- A bundled image is exposed only to Gmail so the stylesheet can display it.

## Reviewer instructions

1. Open Gmail using a reviewer's own account.
2. Mark a conversation as important if needed.
3. Install the extension and reload Gmail.
4. Confirm that the importance marker is gold.
5. Toggle importance off and on to confirm the control still works.

An account with Gmail's blue importance markers provides the clearest before/after
comparison. No extension-specific login or credentials are required.

## Remaining submission materials

- Extension icons are included in manifest.json at 16, 32, 48, and 128 pixels square.
- At least one screenshot showing actual behavior: preferably 1280 x 800.
- Small promotional image: 440 x 280.
- Developer account registration, contact details, and 2-Step Verification.
- Complete the dashboard's privacy declarations and distribution options.
- Upload `dist/gmail-gold-markers-0.1.0.zip`. It contains only manifest.json,
  content.css, and the required assets, with manifest.json at the ZIP root.
  Screenshots and promotional images are uploaded separately in the store listing.

Official instructions:
https://developer.chrome.com/docs/webstore/publish
https://developer.chrome.com/docs/webstore/images
https://developer.chrome.com/docs/webstore/cws-dashboard-privacy
