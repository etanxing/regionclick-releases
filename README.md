# 轻点 · RegionClick

简单的 macOS 区域自动点击工具。原生 SwiftUI 设置页面，支持中文与英文、跟随系统或手动切换深浅主题，并记住你的选择。

## 安装

```sh
brew install --cask etanxing/tap/regionclick
```

Apple Silicon Mac，macOS 13 或更新版本。当前版本使用临时签名，尚未通过 Apple 公证。首次启动若被拦截，请在「系统设置 → 隐私与安全性」中查看并手动允许。

## 使用

1. 打开「轻点」，在设置页面打开系统辅助功能设置，允许轻点。
2. 点击「框选区域」，在任意一台显示器上拖动选择矩形，按 Esc 取消。
3. 选择点击区域中心，或在区域内随机点击。使用鼠标左键单击。
4. 设置点击间隔和运行时长（单位均为秒），点击开始。
5. 窗口会隐藏，3 秒后开始点击；倒计时不计入运行时长。到时自动停止。

**随时按 Command + Shift + 句号（⌘⇧.）停止**。也可从菜单栏打开窗口后停止。关闭窗口仍可从菜单栏重新打开；退出应用会停止点击。运行时鼠标将移到点击位置。

点击间隔范围为 0.05–3600 秒，运行时长范围为 1–86400 秒。运行时长基于单调时钟，包括电脑睡眠经过的时间；唤醒后若已超时会直接停止，不补发点击。显示器布局发生变化会停止运行并清除已保存区域。

首次授予权限后若系统仍未识别，请退出后重新打开轻点。

## 发布方式

与轻词一致：源码保存在私有仓库，公开仓库仅包含安装包、说明、版本记录及问题反馈。

- 私有源码：https://github.com/etanxing/regionclick
- 公开下载：https://github.com/etanxing/regionclick-releases
- Homebrew Tap：https://github.com/etanxing/homebrew-tap

```sh
bash scripts/test.sh
bash scripts/build.sh
bash scripts/package.sh
REGIONCLICK_TAP_DIR=/path/to/homebrew-tap bash scripts/release.sh
```

发布脚本要求源码和 Tap 工作区已提交，创建公开 Release、上传 ZIP 和 SHA256 校验文件，随后更新 Tap。安装包不包含源码。编译只需 Xcode Command Line Tools。

## English

A native macOS auto clicker. Select a region on any display, click its center or a random point inside it, and set an interval and a run duration in seconds. Starts after a three-second countdown and stops automatically. Press **Command + Shift + period** to stop globally. Grant Accessibility access in Settings before use. English and Simplified Chinese, light and dark themes, and saved preferences are included.

Requires Apple Silicon and macOS 13+. The app is ad-hoc signed and not notarized; macOS may require manual first-launch approval in Privacy & Security.

## Validation

Core tests cover coordinate conversion including negative display coordinates, random point bounds, invalid numeric settings, deadline behavior, and translation key coverage. UI snapshots are rendered in Chinese/English and light/dark. Posting clicks to other applications and the physical multi-display selection flow require a live Accessibility-authorized session; they are not covered by the automated core tests.
