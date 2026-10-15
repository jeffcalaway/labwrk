<p align="center"><img src="images/app-icon.png" width="112" alt="Labwrk application icon"></p>

# Labwrk

A native macOS menu bar application for monitoring GitLab CI/CD pipelines. Follow builds across your projects, inspect job states, and receive notifications when pipelines start or finish.

The name combines GitLab with the idea of laboratory work: a small instrument for observing your pipeline activity.

**[Download the latest release](https://github.com/jeffcalaway/labwrk/releases/latest)** · **[Report an issue](https://github.com/jeffcalaway/labwrk/issues)**

Release status: the initial public release is being prepared. Do not assume a downloadable build is available until it appears on the Releases page.

## Features

- Three compact status dots and a running-pipeline count in the menu bar; the indicator is neutral when no pipelines are running.
- A GitLab-style panel with pipeline status, repository links, stages, and individual jobs.
- GitLab.com browser sign-in; self-managed GitLab and personal access tokens are also supported.
- Monitor all member projects or choose specific projects.
- Separate notification controls for started, passed, warning, failed, canceled, and skipped pipelines.
- Four settings tabs: Preferences, Account, Projects, and About.
- Open at login, manual update checks, and optional automatic updates with signed update verification.

![Labwrk pipeline panel](images/pipeline-panel.png)

## Installation

Current builds require **macOS 14 or newer and an Apple silicon Mac**.

1. Download the Labwrk ZIP from the [Releases page](https://github.com/jeffcalaway/labwrk/releases/latest).
2. Extract it and drag **Labwrk.app** to **Applications**.
3. Open Labwrk. It appears in the menu bar and has no Dock icon.
4. Click the indicator, open Settings → Account, and select **Sign in with GitLab**. Complete authorization in your default browser.
5. Allow notifications if desired, then choose projects in Settings → Projects.

The current build is locally signed and has not been Apple Developer ID signed or notarized. If macOS blocks opening it, review the warning and use the per-app Open Anyway option in Privacy & Security only if you trust this official download. Future signed/notarized releases will be identified in their release notes.

Check for updates from the indicator’s right-click menu or Settings → About. Automatic updating can be enabled in Preferences. Versions without a built-in updater require one manual installation of the newer app.

## Progress and privacy

Pipeline and stage progress measures finished jobs, not elapsed time. GitLab does not expose a percentage inside an individual job, so running jobs show a general clock icon and elapsed time when available. Status changes are observed by polling, every 30 seconds by default.

GitLab credentials are stored in macOS Keychain. The app reads GitLab project/pipeline data; it does not run or modify pipelines. Software update checks contact the public update feed and GitHub release downloads, and do not send GitLab credentials.

## Support and license

Use [GitHub Issues](https://github.com/jeffcalaway/labwrk/issues) for bug reports and feature requests. Include your app and macOS versions and reproduction steps. Do not share access tokens, passwords, OAuth codes, or confidential project information.

Labwrk is **proprietary freeware**, free for personal and professional use. It is not open source. Redistribution, resale, rebranding, or derivative applications require separate authorization. See [LICENSE.md](LICENSE.md) and [third-party notices](THIRD_PARTY_NOTICES.txt).

This public repository contains documentation, branding, user support resources, and update information. The proprietary implementation is maintained separately.

Copyright © 2026 Jeff Calaway. All rights reserved. Labwrk is not affiliated with or endorsed by GitLab.
