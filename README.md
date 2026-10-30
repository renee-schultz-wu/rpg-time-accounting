# Skill Garden — GitHub Pages edition

A tiny offline-friendly skill RPG: choose a skill, start a practice timer, gain 1 XP per **full cumulative minute per skill**, and level up every 60 XP. Practice sessions are kept in IndexedDB on the device.

## Publish with GitHub Pages

1. On GitHub, create a new **public** repository, e.g. `skill-garden` (do not add a README when creating it).
2. Unzip the downloaded package. Open the **skill-garden** folder and upload **all files inside** the folder to the **root** of the repository via **Add file → Upload files**. Do not upload the ZIP itself.
3. In repository **Settings → Pages**, choose **Deploy from a branch**, select **main** and **/(root)**, then **Save**.
4. Visit `https://YOUR-USERNAME.github.io/skill-garden/` after GitHub finishes publishing.
5. On iPhone, open the URL in Safari, use **Share → Add to Home Screen**.

## Data and backup

The app stores skills, practice sessions, and a recovery record for an active timer in **IndexedDB**, separately on each browser/installation. GitHub Pages hosts only the app's code; **it does not store or sync your personal data**.

Open the gear icon → **Export backup** and save the JSON file to Files / iCloud Drive. To restore, choose **Restore from backup**. Import **replaces** existing data, so export first. Back up regularly, especially before deleting the Home Screen app or clearing Safari site data. Keep using one installation (Home Screen versus Safari) because browser storage may be separate.

## Limits

* No automatic cloud backup or sync. Exports are manual.
* On iOS, running timers calculate elapsed wall-clock time between start and pause/finish; if you forget to stop a timer, it keeps counting until you return. Pause when you stop practicing.
* The first version is intentionally simple and has no analytics or user accounts.
* This build's JavaScript passes a syntax check, but it has not been tested on a physical iPhone. Check timer recovery and export/import before relying on it long term.
