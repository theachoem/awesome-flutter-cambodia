# Contributing

Thanks for wanting to contribute! This list stays useful because it's easy to add to.

## Adding an app

**Option 1: use an AI coding agent** (Claude Code or similar). Give it the app's Play Store and/or App Store link, plus the prompt below. It handles forking, verification, and the PR itself.

```
Add this app to https://github.com/theachoem/awesome-flutter-cambodia

Play Store: <PLAY_URL>
App Store: <APP_STORE_URL or "none">

1. Fork theachoem/awesome-flutter-cambodia and clone your fork locally (`gh repo fork theachoem/awesome-flutter-cambodia --clone` if you have the GitHub CLI).
2. Read this repo's CONTRIBUTING.md and README.md, and follow them: verify whether the app is fully built with Flutter or only uses it for one screen/module, fetch its category/description/icon, and add a row in the documented format (main list if fully Flutter, Partial Flutter Apps otherwise, noting which part uses Flutter).
3. If you can't conclusively verify Flutter is used at all, say so explicitly instead of guessing, and don't add the entry.
4. Commit, push to your fork, and open a PR summarizing what you verified and how.
```

**Option 2: contribute manually**

1. Fork this repo and clone your fork locally.
2. Verify whether the app is fully built with Flutter: see [How to verify an app is built with Flutter](./README.md#how-to-verify-an-app-is-built-with-flutter) in the README. If only one screen or module uses Flutter and the rest is native, it goes under [Partial Flutter Apps](./README.md#partial-flutter-apps) instead of the main list.
3. **Main list:** each category is its own `### <Category>` section with its own table in [`README.md`](./README.md). Add a row to the matching category's table, or create a new `### <Category>` section (own header + table) if none fits.
   **Partial Flutter Apps:** add a row to the single table under `### Partial Flutter Apps` (the last category under Cambodian Apps, not alphabetized with the others), filling in the **Flutter used in** column with the specific screen/module (e.g. "Marketplace tab").
4. Keep the row to: **Icon, App, Description, Link** (no Category column; the section header is the category, and the Partial Flutter Apps table additionally has a **Flutter used in** column).
   - **Icon**: optional. If you have one, drop a square PNG/JPG (ideally 128px+) into [`assets/logos/`](./assets/logos), named as a lowercase-kebab-case slug of the app name (e.g. `wing-bank.png`), and reference it as `<img src="assets/logos/your-file.png" width="48">`.
   - **App**: the app's name as shown on its store listing.
   - **Description**: one sentence, no marketing fluff.
   - **Link**: a badge per platform the app is available on, placed side by side in the one cell (see below). Badges render as fixed-size images, so unlike plain text links they never wrap awkwardly on narrow screens, and a contributor can add a badge for any platform without changing the table's shape.
5. Keep category sections alphabetized (`### Business` before `### Education`, etc.), and rows within each category alphabetized by app name.
6. Pick the category that best matches what the app is _for_, not just its industry: e.g. telecom self-care apps (topping up, checking data/SIM balance) go under **Telecom**, not Productivity or Tools.
7. Push to your fork and open a PR.

### Link badges

Copy the snippet for whichever platform(s) apply, swap in the real URL, and place them next to each other in the Link cell (a single space between badges is enough).

| Platform        | Preview                                                                                                                | Snippet                                                                                                                                  |
| --------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| Google Play     | ![Google Play](https://img.shields.io/badge/Google_Play-414141?style=flat&logo=googleplay&logoColor=white)             | `[![Google Play](https://img.shields.io/badge/Google_Play-414141?style=flat&logo=googleplay&logoColor=white)](PLAY_URL)`                 |
| App Store (iOS) | ![App Store](https://img.shields.io/badge/App_Store-0D96F6?style=flat&logo=appstore&logoColor=white)                   | `[![App Store](https://img.shields.io/badge/App_Store-0D96F6?style=flat&logo=appstore&logoColor=white)](APP_STORE_URL)`                  |
| Mac App Store   | ![Mac App Store](https://img.shields.io/badge/Mac_App_Store-000000?style=flat&logo=macos&logoColor=white)              | `[![Mac App Store](https://img.shields.io/badge/Mac_App_Store-000000?style=flat&logo=macos&logoColor=white)](MAC_APP_STORE_URL)`         |
| Snap Store      | ![Snap Store](https://img.shields.io/badge/Snap_Store-82BEA0?style=flat&logo=snapcraft&logoColor=white)                | `[![Snap Store](https://img.shields.io/badge/Snap_Store-82BEA0?style=flat&logo=snapcraft&logoColor=white)](SNAP_URL)`                    |
| Flathub         | ![Flathub](https://img.shields.io/badge/Flathub-4A86CF?style=flat&logo=flathub&logoColor=white)                        | `[![Flathub](https://img.shields.io/badge/Flathub-4A86CF?style=flat&logo=flathub&logoColor=white)](FLATHUB_URL)`                         |
| Microsoft Store | ![Microsoft Store](https://img.shields.io/badge/Microsoft_Store-0078D4?style=flat&logo=microsoftstore&logoColor=white) | `[![Microsoft Store](https://img.shields.io/badge/Microsoft_Store-0078D4?style=flat&logo=microsoftstore&logoColor=white)](MS_STORE_URL)` |
| Website         | ![Website](https://img.shields.io/badge/Website-4A90D9?style=flat&logo=googlechrome&logoColor=white)                   | `[![Website](https://img.shields.io/badge/Website-4A90D9?style=flat&logo=googlechrome&logoColor=white)](WEBSITE_URL)`                    |
| Source (GitHub) | ![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)                           | `[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)](REPO_URL)`                               |

Don't see the platform you need? Any [shields.io static badge](https://shields.io/badges/static-badge) with a matching [Simple Icons](https://simpleicons.org/) logo slug works. Add a new row to the table above in the same PR so the next contributor can reuse it.

## General guidelines

- One app/resource per PR is fine, but batching a few related additions in one PR is also fine.
- No affiliate links, no self-promotion beyond genuinely relevant additions.
- If a listing goes stale (app removed from stores, dead link, defunct community), a PR removing it is just as welcome as one adding something.
