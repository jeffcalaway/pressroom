# Changelog

## Unreleased

- **Apply updates safely.** Review Updates lets you choose updates and confirm what will change and how it's protected. PressRoom then applies them one at a time: it checks Git for uncommitted work, copies each update's files first, exports the database, and verifies the site afterward (WordPress loads, the right version is installed, pages respond as before, no new PHP errors).
- Runs pause for a ZIP or a license when needed, with Set License, Retry Update, Use a ZIP Instead, Skip, and Stop.
- Clear results for every update, with the evidence behind any problem and one-click Restore Previous Files or Restore Database.
- Update history in each project, with recovery points kept for the last 10 runs (configurable in Settings).
- Choose extra pages to check after updates in each project's settings.
- A live progress bar shows how far an update run has come.
- Fixed page checks for sites served over plain HTTP (most local sites), which were blocked and left updates only partly verified.
- New official PressRoom app icon in Finder, the Dock, Launchpad, the About panel, and throughout the app.
- Plugins show their own icons, and themes show their screenshots.
- License checks for premium plugins, with a link to each plugin's license settings in your local site's admin when a license is missing, expired, or invalid.
- A Licenses list in each project's Updates tab, with a Set License button for each plugin. For an inactive plugin, whose license page doesn't exist yet, the button opens the Plugins page and explains what to activate first.
- Update plans show what will run unattended, where the run will pause for a ZIP or a license, and what's held back.
- License-Managed is no longer an update method: PressRoom now handles licenses automatically for every plugin. Plugins that used it switch to Update Normally and keep their notes and prepared ZIPs.
- Plugins and themes with a note show a "See note" tag, and their settings window links straight to the note.
- Reverse the Projects list's sort order with the button beside the Sort menu.
- A Composer tab lists the plugins and themes Composer installs.
- Simpler Updates tabs: Special Handling lists plugins and themes set to Never Update or Require Manual Package, or symlinked (Composer ones have their own tab), and updates blocked by the site's PHP or WordPress version appear under Needs Review.
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
