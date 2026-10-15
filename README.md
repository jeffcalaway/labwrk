<p align="center"><img src="images/app-icon.png" width="112" alt="Labwrk application icon"></p>

# Labwrk

A native macOS menu bar application for monitoring GitLab CI/CD pipelines. Follow builds across your projects, inspect job states, and receive notifications when pipelines start or finish.

The name combines GitLab with the idea of laboratory work: a small instrument for observing your pipeline activity.

**[Download the latest release](https://github.com/jeffcalaway/labwrk/releases/latest)** · **[Report an issue](https://github.com/jeffcalaway/labwrk/issues)**

Current release: **[Labwrk 1.1.5](https://github.com/jeffcalaway/labwrk/releases/tag/v1.1.5)**, for Apple silicon and macOS 14 or later.

> [!IMPORTANT]
> **First launch on macOS:** the current release is locally signed and has not been Apple-notarized. If macOS displays **“Labwrk Not Opened”**, use **System Settings → Privacy & Security → Open Anyway** as described below.

## Install and open Labwrk

1. Download the ZIP from [the official Releases page](https://github.com/jeffcalaway/labwrk/releases/latest).
2. Extract it and drag **Labwrk.app** into **Applications**.
3. Open **Labwrk** from Applications. If macOS blocks it, follow the first-launch steps below.

### First launch: “Labwrk Not Opened”

Only continue if you downloaded Labwrk directly from this repository and trust the release.

1. In the warning dialog, select **Done**.
2. Open **System Settings → Privacy & Security** and scroll to the **Security** section.
3. Find the message about Labwrk being blocked and select **Open Anyway**.
4. Authenticate if requested, then confirm **Open** when macOS asks again.

**Open Anyway appears after you have tried to open the app and macOS has blocked it.** If the message is absent, try opening Labwrk from Applications again, then return to Privacy & Security. See [Apple’s instructions for opening an unnotarized app](https://support.apple.com/en-us/102445).

This creates an exception for Labwrk; you do not need to disable macOS security protections globally. Future Apple-notarized releases will be identified in their release notes.

### Connect GitLab

Labwrk appears in the **menu bar**, with no Dock icon. Click its indicator, open **Settings → Account**, and select **Sign in with GitLab**. Complete authorization in your default browser. Allow notifications if desired, then choose projects under **Settings → Projects**.

Check for updates from the indicator’s right-click menu or **Settings → About**. Automatic updating can be enabled in Preferences. Older versions without a built-in updater need one manual installation of a newer version.

## Features

- Three compact status dots and a running-pipeline count in the menu bar; dots show the three newest pipelines within a configurable time window (60 minutes by default), with empty outlines for unused slots. Running pipelines use blue outlines. The count is hidden when no pipelines are running.
- A GitLab-style panel with pipeline status, repository links, stages, individual jobs, and downstream pipelines shown after an arrow.
- Refined hover and cursor feedback for panel links, status circles, and controls.
- GitLab.com browser sign-in; self-managed GitLab and personal access tokens are also supported.
- Monitor all member projects or choose specific projects.
- Separate notification controls for started, passed, warning, failed, canceled, and skipped pipelines.
- Four settings tabs: Preferences, Account, Projects, and About.
- Open at login, manual update checks, and optional automatic updates with signed update verification.

![Labwrk pipeline panel](images/pipeline-panel.png)

![Labwrk preferences](images/preferences.png)

## Progress and privacy

Pipeline status progress measures finished jobs, not elapsed time; running stages and jobs use a general clock icon. GitLab does not expose a percentage inside an individual job, so running jobs show a general clock icon and elapsed time when available. Downstream jobs contribute to job-completion progress; the parent’s overall status remains the status reported by GitLab. If downstream details are unavailable, progress is marked unavailable. The running count covers top-level pipelines in the watched projects. Status changes are observed by polling, every 30 seconds by default.

GitLab credentials are stored in macOS Keychain. The app reads GitLab project/pipeline data; it does not run or modify pipelines. Software update checks contact the public update feed and GitHub release downloads, and do not send GitLab credentials.

## Support and license

Use [GitHub Issues](https://github.com/jeffcalaway/labwrk/issues) for bug reports and feature requests. Include your app and macOS versions and reproduction steps. Do not share access tokens, passwords, OAuth codes, or confidential project information.

Labwrk is **proprietary freeware**, free for personal and professional use. It is not open source. Redistribution, resale, rebranding, or derivative applications require separate authorization. See [LICENSE.md](LICENSE.md) and [third-party notices](THIRD_PARTY_NOTICES.txt).

This public repository contains documentation, branding, user support resources, and update information. The proprietary implementation is maintained separately.

Copyright © 2026 Jeff Calaway. All rights reserved. Labwrk is not affiliated with or endorsed by GitLab.
