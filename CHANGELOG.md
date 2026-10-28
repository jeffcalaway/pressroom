# Changelog

## 1.2.0 — 2026-10-28

- **Add several projects at once.** Add Several… finds every WordPress site in a folder (such as ~/Sites or MAMP's htdocs) or in Local, detects each one's environment, and adds the ones you choose, then scans them.
- **Update several projects at once.** Update Projects… on the Updates page applies updates to the projects you choose, one at a time, each with its usual backups, checks, and report. Updates that need a ZIP or a license are left out unless you include them, so it can run unattended.

## 1.1.2 — 2026-10-28

- The sidebar can't be squeezed narrower than its header: the PressRoom name and "WordPress Update Center" always fit on one line each.

## 1.1.1 — 2026-10-28

- In Compare's Custom mode, the first site is now blue and the second red.

## 1.1.0 — 2026-10-28

- Compare has no page limit: add as many pages as you like. The 10-page limit applies only to the pages checked after updates.
- Compare opens on **Custom**: compare any two addresses, no project needed. Pick it again from the project menu any time.
- A project's Compare list now starts empty. **Import Project Pages** adds its homepage and pages to check in one click.
- The sidebar button no longer looks squeezed on macOS 26 and later.
- Simpler sorting on the Projects page: one **Sort by** menu lists every order by name ("Name, A to Z", "Name, Z to A", "Recently scanned first", and so on), replacing the separate reverse button that changed the menu's options.
- The Projects list fits a narrow window: "Sort by" stays on one line, and project names keep their room (the Environment and Last Scan columns step aside until the window is wider).

## 1.0.0 — 2026-10-28

The first public release.

- **Easy install.** PressRoom comes as a DMG: open it and drag PressRoom into Applications.
- **A welcome tour** the first time you open PressRoom: what it does, how updates work, notifications and other choices to make up front, and a way to add your first project. See it again from Help › Welcome Tour.
- **WP-CLI installs itself.** If your Mac doesn't have WP-CLI, PressRoom downloads the official copy for its own use when you add a project or edit its environment, and checks it before using it. No password, and nothing else on your Mac changes.
- **A new README** with screenshots and plain-language walkthroughs of every feature.
- The Welcome screen now explains that updates run only when you choose them, each with a backup and checks afterward.
- **Updates itself.** PressRoom checks for new versions, shows an orange dot on its menu bar icon when one is ready, and installs it in a few seconds from the icon's right-click menu (**Update to PressRoom…**) or **PressRoom › Check for Updates…**. Updates are checked to be genuine PressRoom builds before they're installed. Turn on automatic downloads in Settings › Updates.
- Compare: tell it CSS selectors to ignore, such as sliders or chat widgets, and they're hidden on both environments so they don't count as differences.
- **Menu bar icon.** See what PressRoom is working on, with progress, from the menu bar; turn notifications on or off, open Settings, or quit. Right-click it for a quick menu, including Quit. Hide it from its own menu, and bring it back in Settings.
- Choose Light, Dark, or System appearance, and have PressRoom open at login (off by default), in Settings › General.
- **Notifications.** PressRoom tells you when a scan, update run, integrity scan or cleanup, or comparison finishes, or when a run needs you. Choose which in Settings, and override them per project (or turn them off) in each project's settings.
- Compare: choose sections per page, alongside or instead of the whole page; clear the preset pages in one click; compare against any address with Custom; Cancel discards a comparison in progress; and Review is now the main button once results are in.
- Screenshots and comparisons are deleted automatically after 14 days (adjustable in Settings), and can be deleted all at once.
- A friendlier project switcher, with each project's theme screenshot.
- **Compare environments.** A new Compare section shows your pages on two environments side by side, such as your local site and staging: how they look on desktop and phone, how different each one is, and which JavaScript errors only one of them throws. Add any page just for comparing, or focus on parts of pages, like the header or a form, by their CSS selector. Server addresses are filled in from wp-cli.yml, GitLab, or WP Engine when possible, and you can type one in. It only loads pages, like a visitor would.
- **Browser checks with your screenshots.** Pages are now captured at phone width as well as desktop (you can turn this off per project), and PressRoom flags JavaScript errors that appear after a run, naming the plugin or theme whose script threw them. In the review, drag over things that change on their own, like sliders or dates, to leave them out of comparisons, or list CSS selectors in project settings to hide them before every screenshot.
- **Safer update runs.** Plugins that depend on another plugin now update after it, and are skipped if it didn't update. If your local site stops mid-run, PressRoom pauses with Retry instead of failing. A run you stopped, or one interrupted by quitting, can be resumed with one click. When a run pauses while you're in another app, a notification tells you why.
- Scanning and cleanup animations start smoothly instead of stuttering as they appear.
- When a server doesn't answer SSH, PressRoom explains the likely reason: for example, that the server is up but only accepts SSH from approved addresses, and that your VPN isn't connected.
- **Integrity checks and cleanup.** The Integrity section finds files left on your staging and production servers after they were removed from the repository, such as old plugin files and deleted themes, and shows the commit that removed each one. Scans only read. When you choose to clean up, PressRoom backs the files up to your Mac first, removes them, checks the site still loads, and lets you restore them with one click. PressRoom confirms on the server that everything is gone (and tells you exactly what isn't), shows fun animations while scanning and cleaning up, and deletes cleanup backups after 30 days (adjustable in Settings).
- **SSH setup built in.** If a server doesn't recognize your Mac yet, PressRoom creates an SSH key, copies it for you, opens your host's SSH Keys page, and tests the connection until it works.
- **Sign in with GitLab** in Settings (no setup needed), so PressRoom knows which version of your code each server runs. It's read-only: nothing on GitLab is ever changed.
- **Apply updates safely.** Review Updates lets you choose updates and confirm what will change and how it's protected. PressRoom then applies them one at a time: it checks Git for uncommitted work, copies each update's files first, exports the database, and verifies the site afterward (WordPress loads, the right version is installed, pages respond as before, no new PHP errors).
- Runs pause for a ZIP or a license when needed, with Set License, Retry Update, Use a ZIP Instead, Skip, and Stop.
- Clear results for every update, with the evidence behind any problem and one-click Restore Previous Files or Restore Database.
- Update history in each project, with recovery points kept for the last 10 runs (configurable in Settings).
- Choose extra pages to check after updates in each project's settings.
- A live progress bar shows how far an update run has come.
- Optional before-and-after screenshots of your key pages, compared in the app when the run ends (side by side, with a slider, or with changes highlighted), then deleted with one click. A playful camera animation shows progress while screenshots are taken. Screenshots wait until each page has fully loaded and finished styling, so nothing is caught half-styled.
- Bigger, easier switches for every on/off option. Only the switch itself toggles, and it animates between on and off.
- A scanning animation shows each step of a project scan as it happens, and Scan All on the Updates page shows every project's progress.
- On the Updates page, click anywhere on a project's header to open it; project headers stand out more from their updates.
- Update run folders are named by date, time, and project, so you can find a run in Finder.
- Reviewing screenshots is more fun: animated checkmarks, a "Looks good" sticker, and confetti when you finish.
- A cleaner Settings page.
- Adding pages to check is easier: paste full URLs (PressRoom keeps just the path), or choose pages from your site's published content by type (Pages, Posts, and so on), sorted A–Z or newest first. Content without pages of its own, such as testimonials, is left out automatically, and you can hide any other type. Archive pages and category, tag, and other term pages are listed too, and posts can be narrowed to one category or term. Clear All starts the list over. The homepage appears as the first page and can't be removed, and a counter shows how many of the 10 pages you've used, in the list and while choosing pages. In Choose Pages, pages already on your list can be turned off to make room, and the checked pages are shown at the top, where one click unchecks one (or checks it again).
- Fixed page checks for sites served over plain HTTP (most local sites), which were blocked and left updates only partly verified.
- The finalized PressRoom app icon, made in Icon Composer, so macOS renders it natively with its glass and lighting in Finder, the Dock, Launchpad, and the About panel. The sidebar, Welcome screen, and Settings › About use it too.
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
