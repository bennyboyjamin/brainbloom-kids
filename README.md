# BrainBloom Kids

Brain-training games for kids aged 5–13, with Pixel the robot. Everything runs on the device: no accounts, ads, tracking or outside links.

- `index.html`: the whole app (also works in any web browser)
- `privacy.html`: privacy policy (served by GitHub Pages)
- `app-icon.png` (1024×1024) and `app-splash.png` (2732×2732)
- `.github/workflows/ios-app.yml`: builds the iPhone/iPad app on GitHub's Macs and uploads it to TestFlight
- `.github/scripts/asc.rb`: makes and removes the App Store signing files during a build

## One-time setup

1. **App ID**: at developer.apple.com → Certificates, IDs & Profiles → Identifiers, register an App ID such as `com.yourname.brainbloomkids` (no extra capabilities needed).
2. **App Store Connect**: My Apps → + → New App: iOS, name "BrainBloom Kids", the same bundle ID, any SKU.
3. **Repository secrets** (Settings → Secrets and variables → Actions):
   - `APPLE_TEAM_ID`, `BUNDLE_ID`, `ASC_KEY_ID`, `ASC_ISSUER_ID`, `ASC_KEY_P8` (the same API key you use for Say Math works).
4. **Privacy page**: either copy `privacy.html` to your saystudios.github.io site (for example `https://saystudios.github.io/brainbloom-kids/privacy.html`), or turn on Pages here (Settings → Pages → Deploy from branch `main`, folder `/`) for `https://bennyboyjamin.github.io/brainbloom-kids/privacy.html`.

## Build

Actions → **Build iPhone app** → Run workflow → enter the version (for example `1.0`). About 15–30 minutes after it finishes, the build shows up in App Store Connect → TestFlight.

## App Store listing tips

- Category: Education. Age rating: 4+. Turn on **Kids Category** (Ages 6–8 or 9–11).
- App Privacy: "Data Not Collected".
- Privacy Policy URL: the privacy page link from step 4.
- Copyright: © 2026 Say Studios LLC. Support email: SayStudiosllc@yahoo.com.
- Describe it as games for fun and practice; it does not diagnose or treat anything.
