# Toss Away — legal and support pages

Published with GitHub Pages. App Store Connect needs both a privacy policy URL
(mandatory for anything with subscriptions) and a support URL, and both have to
be live *before* the app is submitted — not after.

## Publishing

```sh
gh repo create mustafaglden/tossaway --public --source=docs-site --push
# then: Settings → Pages → Source: main, folder /(root)
```

Live at:

| Page | URL |
|---|---|
| Privacy | `https://mustafaglden.github.io/tossaway/privacy` |
| Support | `https://mustafaglden.github.io/tossaway/support` |
| Terms | `https://mustafaglden.github.io/tossaway/terms` |

Those exact URLs are already in `SnapSweep/Resources/Config.plist`, so the
in-app Privacy and Terms links point at them. If the repository is named
anything other than `tossaway`, update the plist to match.

## Keeping them honest

The privacy page describes the app as it actually behaves — on-device analysis,
no upload, no account, bucketed analytics, permanent deletion in the Files tab.
If any of that changes, the page changes with it, and the App Privacy answers in
App Store Connect have to keep agreeing with `PrivacyInfo.xcprivacy`.
