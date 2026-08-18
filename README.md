# MacWinlink — Public Beta Releases

**MacWinlink is a native macOS [Winlink](https://www.winlink.org/) email client for amateur radio operators.**  It brings the Winlink global radio email network to macOS as a first-class app, with native SwiftUI, direct CAT rig control, and support for Telnet, VARA HF, VARA FM, ARDOP, and Packet transports.

This repository is the **official public beta distribution point** for MacWinlink and the primary channel for tester feedback.  The full source code and planning discussions currently live in a private repository under the Amateur Radio Safety Foundation while the project completes its pre-Mac-App-Store readiness work; public source-code visibility is on the roadmap but not yet enabled.

**File bugs and feature requests in [this repo's Issues tab](../../issues)** — regardless of any other MacWinlink URLs you may have seen in documentation or release notes.  Every report is read by the maintainer and triaged into the active development plan.

---

## Download

The latest beta build is on the [Releases page](../../releases).  Each release includes a `.dmg` disk image containing both the main **MacWinlink** app and the optional **MacWinlink Helper** app.

## Installing

1. Download the `.dmg` from the latest [release](../../releases).
2. Double-click the `.dmg` to mount it.
3. Drag `MacWinlink.app` (and `MacWinlink Helper.app` if you'll use VARA HF/FM or Direwolf packet) into your `Applications` folder.
4. On first launch, macOS will show a Gatekeeper warning — see the next section to bypass it.

## ⚠️ First-Launch Gatekeeper Warning — Read This

**MacWinlink is currently distributed as an ad-hoc-signed beta while ARSFI completes Apple Developer Program enrollment for Mac App Store distribution.**  This means macOS Gatekeeper does not yet recognize MacWinlink as coming from an identified developer, and will show a warning the first time you launch it.  **The warning is expected for this beta.**

### Since macOS Sequoia (macOS 15), Control-click-to-open no longer bypasses this warning.

You must go through **System Settings** to allow the app.  Do this once per version — updates from the same developer don't re-prompt.

### Step-by-step

1. **Double-click** `MacWinlink.app` in `Applications` as normal.
2. A dialog will appear saying something like *"macOS cannot verify that this app is free from malware"* — click **Done** (or **Cancel** on some macOS versions) to dismiss it.  Don't click "Move to Trash."
3. Open **System Settings** → **Privacy & Security**.
4. Scroll down to the **Security** section.
5. You'll see a message: *"'MacWinlink' was blocked to protect your Mac."*  Click **Open Anyway** next to it.
6. macOS will ask you to confirm — enter your **admin password** (or use Touch ID).
7. A final dialog will appear — click **Open**.

MacWinlink will now launch, and future launches of this same version will open normally.  You'll need to repeat these steps once when a new beta version is installed.

**If you also installed MacWinlink Helper**, repeat the same steps for it — it will appear in the same Privacy & Security list the first time you launch it.

### Is this safe?

Yes — for this specific app.  MacWinlink is built from source by the ARSFI project and signed ad-hoc during release packaging.  The Gatekeeper warning is a general macOS protection against unidentified developers, not a specific warning about MacWinlink.  Once Apple Developer Program enrollment completes, future builds will be Developer-ID signed and notarized, and this manual step will no longer be needed.

---

## System Requirements

- **macOS 15.0 (Sequoia) or later.**
- **Apple Silicon Mac (M1, M2, M3, M4, or later).**  Intel Macs are not supported — MacWinlink is an Apple Silicon–only project.  Even if a build happens to launch on Intel, no testing is performed on that architecture and no Intel-specific issues will be fixed.
- **Amateur radio license and callsign** for RF transports (VARA HF/FM, ARDOP, Packet).  Telnet works without a radio for testing and basic Winlink email over the internet.
- **Radio hardware and audio interface** for RF modes — see the in-app setup wizard.

---

## Reporting Bugs and Requesting Features

**This repository's [Issues tab](../../issues) is the intake point for all beta tester feedback.**  Please file everything here — bugs, feature requests, and questions.

- **Bug report** — use the **Bug report** issue template.  Include your macOS version, MacWinlink version, and steps to reproduce.  Screenshots and log excerpts are enormously helpful.
- **Feature request** — use the **Feature request** issue template.  Describe the problem you're trying to solve and the outcome you'd like to see.

### How reports get handled

1. You file an issue here.
2. The maintainer triages and reviews it.  You may be asked for clarifying details or additional logs.
3. Confirmed bugs and accepted feature requests are tracked internally against the codebase; you'll be notified in the original issue when a fix or feature ships in a subsequent beta.

Filing here keeps the public beta feedback organized in one place and gives every tester visibility into what others have reported.

---

## Checking for Updates

New beta builds are published to the [Releases page](../../releases).  Each release is tagged with its version (e.g. `v1.0.0-beta19`) and includes release notes summarizing what's changed.

You can **watch this repo** (top-right → Watch → Custom → Releases) to get notified whenever a new beta is published.

---

## Project Home

This repo (`jjones9527/macwinlink-releases`) is the public face of MacWinlink for the ongoing beta cycle — it hosts the DMGs, the release notes, and the issue tracker.  Source code, architectural discussions, and long-form roadmap work live in a private planning repository until the project's public-visibility prep (audit sweep, license clean-up, credential scrub) completes.  Once opened, that repo will be linked here.

See [CONTRIBUTING.md](CONTRIBUTING.md) for details on what this repo is and isn't for.
