# PressRoom

A native macOS app for keeping WordPress projects updated, tested, and deployment-ready.

PressRoom finds the WordPress sites on your Mac, connects to them with the right PHP and WP-CLI, and shows which projects need attention, without changing your sites.

> [!NOTE]
> PressRoom is in early development (0.1.0). This release discovers and explains updates. Plugin update policies, protected updates, GitLab, and deployment-integrity features are on the way.

## What it does today

- **Add projects in a few clicks.** Choose a WordPress folder. PressRoom recognizes LocalWP, MAMP / MAMP PRO, Bedrock-style, and custom setups, and picks the PHP build your site actually uses.
- **Tests the connection safely.** Read-only checks of PHP, WP-CLI, the WordPress files, and the database, with plain-language guidance when something's off (for example, "LocalWP's database server may not be running").
- **Scans for updates.** Core, plugins, and themes, including updates that need a manually downloaded package. Partial scans are labeled as partial, never as "up to date."
- **Shows what needs you first.** A dashboard that highlights projects with updates, connection problems, or missing scans.
- **Stays out of your projects.** PressRoom stores its data in `~/Library/Application Support/PressRoom` and never writes inside your WordPress folders. Git details are read from `.git` files; PressRoom never commits, pushes, or fetches.

## Requirements

- macOS 14 Sonoma or later
- One of: [Local](https://localwp.com), [MAMP](https://www.mamp.info), or your own PHP and MySQL
- [WP-CLI](https://wp-cli.org) for MAMP and custom setups (Local includes it)

## Install

Download PressRoom, move **PressRoom.app** to Applications, and open it. Current builds are signed locally but not notarized; if macOS blocks the first launch, Control-click the app, choose **Open**, then confirm.

## Privacy

PressRoom runs entirely on your Mac. It has no account, analytics, or telemetry. When it checks for updates, WP-CLI contacts WordPress.org (and any plugin vendors your site is configured to use), just as your WordPress dashboard does.

## License

PressRoom is free to use, including professionally, under the [PressRoom Proprietary Freeware License](LICENSE.md). Third-party components are listed in [THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt). PressRoom is not affiliated with the WordPress Foundation, WP Engine, Local, MAMP, GitLab, or GitHub.
