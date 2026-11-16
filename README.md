# 自动点击 · Auto Click

**English** | [简体中文](README.zh-CN.md)

A native macOS auto clicker. Select a screen region, choose a click interval and a run duration, and let the app handle repeated left clicks.

## Install

```sh
brew install --cask etanxing/tap/regionclick
```

Requires an **Apple Silicon Mac running macOS 13 or later**. The installed app is named **自动点击.app**, including when using the English interface.

To update an existing installation:

```sh
brew update
brew upgrade --cask etanxing/tap/regionclick
```

You can also download the ZIP from [Releases](https://github.com/etanxing/regionclick-releases/releases/latest), extract it, and move 自动点击.app to Applications. Each release includes a SHA256 checksum file.

## First launch

```sh
open "/Applications/自动点击.app"
```

The app is ad-hoc signed and has not been notarized by Apple. If macOS blocks the first launch, check **System Settings → Privacy & Security** and manually allow it.

In the app's **Settings** tab, click **Open System Settings**, then allow **自动点击** under **Privacy & Security → Accessibility**. If the permission is not recognized immediately, quit and reopen the app.

## Use

1. Click **Select region…** and drag a rectangle on any display. Press Escape to cancel.
2. Choose **Region center** or **Random in region**. The app sends single left clicks.
3. Set the **click interval** and **run duration**, both in seconds.
4. Click **Start**. The window hides and clicking begins after a three-second countdown.
5. Clicking stops automatically when the run duration ends. The countdown is separate from the run duration.

**Press Command + Shift + period (⌘⇧.) at any time to stop.** You can also reopen the window from the menu bar and click Stop. Closing the window keeps the app available in the menu bar; quitting stops clicking. While running, the pointer moves to each click position.

The interval range is **0.05–3600 seconds**, and the duration range is **1–86400 seconds**. Sleep time counts toward the duration. If the timer has expired when the Mac wakes, the app stops without sending catch-up clicks. Changes to the display layout stop the run and clear the saved region.

## Language and appearance

- Choose **English**, **简体中文**, or the system language using the visible language switch.
- In **Settings**, choose **Light**, **Dark**, or **System** appearance.
- The app remembers your choices, click settings, and selected region.

## Downloads and support

- [Latest release](https://github.com/etanxing/regionclick-releases/releases/latest)
- [Report an issue](https://github.com/etanxing/regionclick-releases/issues)
- [Homebrew Tap](https://github.com/etanxing/homebrew-tap)

This public repository contains downloads, documentation, release notes, and issue reports. The application source is maintained privately.
