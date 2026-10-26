# Changelog

## Unreleased

- New official PressRoom app icon in Finder, the Dock, Launchpad, the About panel, and throughout the app.
- Plugins show their own icons, and themes show their screenshots.
- License checks for premium plugins, with a link to each plugin's license settings in your local site's admin when a license is missing, expired, or invalid.
- A Licenses list in each project's Updates tab, with a Set License button for each plugin. For an inactive plugin, whose license page doesn't exist yet, the button opens the Plugins page and explains what to activate first.
- Update plans show what will run unattended, where the run will pause for a ZIP or a license, and what's held back.
- Symlinked plugins and themes are labeled "Symlinked" and left out of updates.
- Neater plugin lists: versions, statuses, and buttons line up in columns.
- Updated brand colors and a clearer selection indicator in update settings.
- Fixed the sidebar so choosing a section while a project is open shows that section.
- Fixed a rare hang when several WP-CLI commands finished at the same time.

## 0.2.0 — Update policies

- Choose how each plugin and theme may be updated: Update Normally, Never Update (with a reason), Require Manual Package, or License-Managed.
- Never Update is enforced everywhere: those components are listed as held back and never included in an update.
- Supply a vendor ZIP for premium plugins. PressRoom checks the archive's structure, plugin identity, and version before accepting it, without extracting it.
- Clearer statuses: "Up to date" only when the update source confirms it, plus Manual update required, Blocked by PHP or WordPress requirements, Managed by Composer, and No update source.
- Detects Composer-installed and Git-committed plugins and themes.
- Preview the update plan for a project, including what's held back and why.
- Scan history shows what changed between scans.

## 0.1.0 — First preview

- Add WordPress projects with a guided four-step setup.
- Automatic detection of LocalWP, MAMP / MAMP PRO, and custom PHP environments, with manual overrides.
- Read-only connection test with clear explanations and next steps.
- Scan core, plugins, and themes for updates, including updates that need a manual package.
- Projects dashboard with an attention summary, search, filters, and sorting.
- Project overview, updates, and settings; a combined Updates view; activity history.
- Light and dark appearance.
