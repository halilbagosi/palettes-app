# Palettes app site

Support and privacy policy pages for the Palettes iOS app, served with GitHub Pages.

- Support: https://palettes.halilbagosi.com/support/
- Privacy: https://palettes.halilbagosi.com/privacy/

The privacy page is generated from `Palettes/Resources/PrivacyPolicy.md` in the app repo; keep the two in sync.

## Shared links

The app's Share button sends `https://palettes.halilbagosi.com/p/#<data>` (palette) or `/c/#<data>` (color), where `<data>` is base64url JSON holding the colors (format in `Palettes/Utilities/SharedLink.swift` in the app repo).

- `.well-known/apple-app-site-association` lets iOS open those paths in Palettes (Associated Domains `applinks:palettes.halilbagosi.com`, app ID `KCH5545G6F.com.halilbagosi.Palettes`). `.nojekyll` keeps the dot-folder published.
- `p/index.html` and `c/index.html` are the same page: it shows the shared colors and, on iPhone or iPad (where reaching the page means the app isn't installed), redirects to the App Store. Keep the two copies identical.
