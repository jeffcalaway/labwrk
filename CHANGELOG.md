# Changelog

## 1.1.6 — prepared for release

- Showed the running clock in pipeline Status badges until the first job finishes, then switched to measured progress.

## 1.1.5 — 2026-10-15

- Changed running pipeline menu bar dots to blue outlines with transparent centers.
- Changed successful-completion notification wording to “Finished”.
- Moved first-launch trust instructions next to the download links, with numbered Privacy & Security steps.

## 1.1.4 — 2026-10-15

- Updated the running-job clock glyph to the supplied shorter, finer strokes.
- Changed the default indicator window to one hour. Existing saved selections are preserved.

## 1.1.3 — 2026-10-15

- Installed the final approved three-circle application icon throughout the app and public presentation.
- Updated the downstream arrow and simplified the menu bar tooltip.
- Added pointing-hand cursors and hover feedback to panel links and action controls.
- Enlarged waiting/created center dots slightly.
- Preserved the dynamic menu bar status indicator.

## 1.1.2 — 2026-10-15

- Matched indicator tooltip durations to the Preferences labels.
- Gave filled and outlined menu bar dots the same outer size.
- Added downstream pipeline circles after an arrow, with job inspection and pipeline links.
- Included nested and cross-project downstream jobs in progress without double-counting shared pipelines.
- Reported unavailable downstream details without claiming full progress.

## 1.1.1 — 2026-10-15

- Corrected running stage/job circles to use the filled blue clock appearance.
- Removed white fills from neutral job circles and replaced created-job arrows with a gray center dot.
- Added a configurable menu bar indicator window, defaulting to 120 minutes.
- Ordered indicator slots by pipeline creation time and left unused slots as white outlines.
- Kept recent completion colors until expiry and the running total independent of the window.

## 1.1.0 — 2026-10-15

- Added four settings tabs, launch-at-login support, and signed software update support.
- Added separate pipeline-started and completion notification preferences.
- Added notification choices and update checks to the indicator’s context menu.
- Updated application branding and project-name formatting.
- Opened OAuth sign-in in the default browser and hid sign-in controls while connected.
- Simplified the idle indicator to three empty circles without a count.

## Earlier local development builds

Implemented GitLab OAuth/PAT connections, project monitoring, pipeline/stage/job views, completion notifications, and menu bar status indicators. These builds were not public GitHub releases.
