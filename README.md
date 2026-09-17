# Gmail Gold Markers

A minimal Manifest V3 Chrome extension that restores Gmail's gold importance
markers. It injects one stylesheet on `https://mail.google.com/*` and uses a
bundled image. No JavaScript, backend, analytics, or Gmail API access.

## Load into Chrome

1. Open `chrome://extensions`.
2. Enable **Developer mode**.
3. Click **Load unpacked** and select this project folder.
4. Reload any already-open Gmail tabs.

After editing the extension, click its **Reload** button on
`chrome://extensions`, then reload Gmail. Disable or remove the extension to
restore Gmail's own colors.

## How it works

`content.css` selects the final direct `div` child of
`[role="switch"][data-is-important="true"]` and replaces only its background
image. Gmail retains control of size, position, clicks, tooltips, and importance
state. CSS also applies to matching elements inserted during navigation.

The selector avoids Gmail's variable class names and localized accessible labels.
It assumes the icon is the final direct `div` child, as in the supplied Gmail
markup. Gmail's internal DOM is not a public API; different layouts or future
changes may require a selector update. This initial version covers these
importance switches, not every importance-related icon in Gmail's sidebar or menus.

The image is exposed only to Gmail through `web_accessible_resources`. The
extension makes no image download at runtime and does not read or transmit email.
Chrome may display a site-access warning because its stylesheet modifies Gmail.

## Manual validation in Gmail

- Check an account with blue markers: important conversations should become gold.
- Check an account with existing gold markers for visual regressions.
- Toggle importance off and on: unimportant markers should retain Gmail's style.
- Navigate between inbox, search results, and conversations; load more messages.
- Check light and dark themes and different display densities.
- Confirm tooltips, keyboard interaction, and marking messages still work.
- Disable the extension and reload Gmail to confirm the original appearance returns.

The initial version has been reported working in the user's Gmail account.
The broader checks above remain the pre-release validation checklist.

## Asset provenance

`assets/important-yellow.png` is the original 20 × 20 PNG downloaded from Google:

https://ssl.gstatic.com/ui/v1/icons/mail/gm3/1x/label_important_fill_googyellow500_20dp.png

The asset belongs to its respective rights holder; this project does not grant
a separate license for it. This extension is not affiliated with Google.
