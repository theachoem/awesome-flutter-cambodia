# Contributing

Thanks for wanting to contribute! This list stays useful because it's easy to add to.

## Adding an app

The easiest way to contribute: give an AI coding agent (Claude Code or similar) the app's Play Store and/or App Store link, plus the prompt below — it can look up the metadata, verify Flutter, fetch the icon, and open a PR for you.

```
Add this app to https://github.com/theachoem/awesome-flutter-cambodia

Play Store: <PLAY_URL>
App Store: <APP_STORE_URL or "none">

1. Read this repo's CONTRIBUTING.md and the "How to verify an app is built with Flutter" section of README.md for the format and verification method this list uses.
2. Fetch the store listing(s) for category, a one-sentence description, and developer name.
3. Verify the app is fully built with Flutter (not just using it for one screen/feature) per the two-step method in README.md. If you can't conclusively confirm this — e.g. no device/emulator access to check the context menu, or an APK analysis that's inconclusive — say so explicitly instead of guessing, and don't add the entry.
4. Download the app icon (highest resolution available) to assets/logos/<kebab-case-app-name>.png.
5. Add a row to the correct category table in README.md, following the existing row format and the badge snippets in this file.
6. Open a PR summarizing what you verified and how.
```

Contributing without an agent works too — just follow the steps below yourself.

1. Verify the app is fully built with Flutter — see [How to verify an app is built with Flutter](./README.md#how-to-verify-an-app-is-built-with-flutter) in the README. An app that only uses Flutter for one screen or an embedded module is outside this list's scope.
2. Add a row to the table in the relevant category (or create a new category if none fits) in [`README.md`](./README.md).
3. Keep the row to: **Icon, App, Category, Description, Link**.
   - **Icon** — optional. If you have one, drop a square PNG/JPG (ideally 128px+) into [`assets/logos/`](./assets/logos), named as a lowercase-kebab-case slug of the app name (e.g. `wing-bank.png`), and reference it as `<img src="assets/logos/your-file.png" width="32">`.
   - **App** — the app's name as shown on its store listing.
   - **Category** — one of the existing categories where possible, to keep the list scannable.
   - **Description** — one sentence, no marketing fluff.
   - **Link** — a badge per platform the app is available on, placed side by side in the one cell (see below). Badges render as fixed-size images, so unlike plain text links they never wrap awkwardly on narrow screens, and a contributor can add a badge for any platform without changing the table's shape.
4. Keep rows within a category alphabetized by app name.

### Link badges

Copy the snippet for whichever platform(s) apply, swap in the real URL, and place them next to each other in the Link cell (a single space between badges is enough).

| Platform | Snippet |
|---|---|
| Google Play | `[![Google Play](https://img.shields.io/badge/Google_Play-414141?style=flat&logo=googleplay&logoColor=white)](PLAY_URL)` |
| App Store (iOS) | `[![App Store](https://img.shields.io/badge/App_Store-0D96F6?style=flat&logo=appstore&logoColor=white)](APP_STORE_URL)` |
| Mac App Store | `[![Mac App Store](https://img.shields.io/badge/Mac_App_Store-000000?style=flat&logo=macos&logoColor=white)](MAC_APP_STORE_URL)` |
| Snap Store | `[![Snap Store](https://img.shields.io/badge/Snap_Store-82BEA0?style=flat&logo=snapcraft&logoColor=white)](SNAP_URL)` |
| Flathub | `[![Flathub](https://img.shields.io/badge/Flathub-4A86CF?style=flat&logo=flathub&logoColor=white)](FLATHUB_URL)` |
| Microsoft Store | `[![Microsoft Store](https://img.shields.io/badge/Microsoft_Store-0078D4?style=flat&logo=microsoftstore&logoColor=white)](MS_STORE_URL)` |
| Website | `[![Website](https://img.shields.io/badge/Website-4A90D9?style=flat&logo=googlechrome&logoColor=white)](WEBSITE_URL)` |
| Source (GitHub) | `[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)](REPO_URL)` |

Don't see the platform you need? Any [shields.io static badge](https://shields.io/badges/static-badge) with a matching [Simple Icons](https://simpleicons.org/) logo slug works — add a new row to the table above in the same PR so the next contributor can reuse it.

## Adding a course, community, or company

Add a row to the relevant table under **Courses & Learning**, **Communities**, or **Companies & Jobs**. Keep descriptions short and factual.

## General guidelines

- One app/resource per PR is fine, but batching a few related additions in one PR is also fine.
- No affiliate links, no self-promotion beyond genuinely relevant additions.
- If a listing goes stale (app removed from stores, dead link, defunct community), a PR removing it is just as welcome as one adding something.
