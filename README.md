<p align="center"><img src="images/PressRoom.png" width="128" height="128" alt="PressRoom app icon"></p>

# PressRoom

A native macOS app for keeping WordPress projects updated, tested, and deployment-ready.

PressRoom finds the WordPress sites on your Mac, connects to them with the right PHP and WP-CLI, and shows which projects need attention, without changing your sites.

> [!NOTE]
> PressRoom is in early development. It discovers and explains updates, applies the ones you choose to your local sites with recovery points and verification, and helps you undo anything that goes wrong. GitLab and deployment-integrity features are on the way.

## What it does today

- **Add projects in a few clicks.** Choose a WordPress folder. PressRoom recognizes LocalWP, MAMP / MAMP PRO, Bedrock-style, and custom setups, and picks the PHP build your site actually uses.
- **Tests the connection safely.** Read-only checks of PHP, WP-CLI, the WordPress files, and the database, with plain-language guidance when something's off (for example, "LocalWP's database server may not be running").
- **Scans for updates.** Core, plugins, and themes, including updates that need a manually downloaded package. Partial scans are labeled as partial, never as "up to date."
- **Respects how each plugin should be maintained.** Mark plugins and themes Never Update or Require Manual Package. PressRoom enforces those choices, checks premium plugins' licenses automatically, detects Composer-managed and Git-committed components, and checks vendor ZIPs before accepting them.
- **Knows when a license needs attention.** For premium plugins like ACF PRO, SearchWP, WP All Import/Export Pro, Gravity Forms, and Elementor Pro, PressRoom tells you when no license is active or it has expired, and links straight to the license settings in your local site's admin.
- **Applies updates safely, one at a time.** Choose updates, review what will change and how it's protected, and let PressRoom apply them to your local site. Before each update it checks Git for uncommitted work and copies the files it will replace; it exports the database first; afterward it checks that WordPress loads, the right version is installed, your pages still respond, and no new PHP errors appeared.
- **Helps when something breaks.** Each update's report shows what passed, what failed, and what couldn't be checked, with the evidence (for example, the new PHP error from the plugin's own files). Restore Previous Files or Restore Database in one click.
- **Shows what needs you first.** A dashboard that highlights projects with updates, connection problems, or missing scans.
- **Changes your projects only when you ask.** Scans are read-only. Files change only when you apply or restore updates, and only on your local site. PressRoom's records and recovery points live in `~/Library/Application Support/PressRoom`. PressRoom never commits, pushes, or fetches with Git.

## Requirements

- macOS 14 Sonoma or later
- One of: [Local](https://localwp.com), [MAMP](https://www.mamp.info), or your own PHP and MySQL
- [WP-CLI](https://wp-cli.org) for MAMP and custom setups (Local includes it)

## Install

Download PressRoom, move **PressRoom.app** to Applications, and open it. Current builds are signed locally but not notarized; if macOS blocks the first launch, Control-click the app, choose **Open**, then confirm.

## Privacy

PressRoom runs entirely on your Mac. It has no account, analytics, or telemetry. When it checks for updates, WP-CLI contacts WordPress.org (and any plugin vendors your site is configured to use), just as your WordPress dashboard does. PressRoom also downloads the plugin icons those sources publish so it can show them; you can turn this off in Settings › Appearance.

License checks read only the license *status* premium plugins store in your site's database. PressRoom never reads, stores, or sends license keys.

## License

PressRoom is free to use, including professionally, under the [PressRoom Proprietary Freeware License](LICENSE.md). Third-party components are listed in [THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt). WordPress and the WordPress logo are trademarks of the WordPress Foundation. PressRoom is not affiliated with the WordPress Foundation, WP Engine, Local, MAMP, GitLab, or GitHub.
