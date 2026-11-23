# Bitty

Bitty is a small macOS terminal with tabs, split panes, and configurable themes.
Each pane runs its own shell and keeps it alive when you switch tabs.

Bitty is a rewrite of [justty](https://github.com/0x96f/justty) in Go using MyGo.
Bitty adds a few features and improvements.

- Split a tab into side-by-side or stacked terminal panes.
- Drag tabs to reorder them.
- Play optional sounds for terminal notifications and zsh command results.
- Get a warning before closing sessions with background or stopped jobs.

This repository hosts Bitty releases only.

## Installation

Bitty requires macOS 15.6 or later. The release build is a universal app for
Apple silicon and Intel Macs.

### Install from GitHub Releases

1. Download `Bitty-macos.zip` from [Bitty releases](https://github.com/0x96f/bitty-releases/releases).
2. Extract the ZIP and move `Bitty.app` into Applications.
3. Open Bitty from Applications.

### Install with Homebrew

Install from the shared Forge tap. Use a GitHub CLI login with read access to
`0x96f/bitty-releases`, which hosts the release ZIP.

```sh
gh auth status
brew install --cask 0x96f/forge/bitty
```

You can also authenticate the ZIP download by setting
`HOMEBREW_GITHUB_API_TOKEN` to a fine-grained token with Contents read access
to `0x96f/bitty-releases` when installing or upgrading.

### First launch

Bitty releases use a self-signed certificate. The Homebrew cask clears
quarantine on the installed app bundle. For a manual ZIP install, macOS may
block the first launch. If you trust your download, try opening Bitty once, then go to
**System Settings → Privacy & Security** and choose **Open Anyway** for Bitty.
Follow the confirmation prompts. [Apple Support](https://support.apple.com/en-us/102445)

Bitty opens a terminal and creates or migrates
`~/.config/bitty/settings.yaml` when needed. Press `⌘T` for a new tab or
`⌘D` to split the current pane.

### Update or uninstall

For a ZIP install, quit Bitty and replace the app in Applications with the
new version. To uninstall, move the app to Trash. If you installed with
Homebrew, use the corresponding command.

```sh
brew upgrade --cask 0x96f/forge/bitty
brew uninstall --cask 0x96f/forge/bitty
```
