# 自动点击 · Auto Click

[English](README.md) | **简体中文**

原生 macOS 区域自动点击工具。框选屏幕区域，设定点击间隔和运行时长，自动完成重复的鼠标左键单击。

## 安装

```sh
brew install --cask etanxing/tap/regionclick
```

要求 **Apple Silicon Mac、macOS 13 或更新版本**。安装后的应用名称为 **自动点击.app**，使用英文界面时也保留此名称。

更新已有安装：

```sh
brew update
brew upgrade --cask etanxing/tap/regionclick
```

也可从 [Releases](https://github.com/etanxing/regionclick-releases/releases/latest) 下载 ZIP，解压后将「自动点击.app」移入「应用程序」。每个版本均附带 SHA256 校验文件。

## 首次启动

```sh
open "/Applications/自动点击.app"
```

当前版本使用临时签名，尚未经过 Apple 公证。首次启动若被 macOS 拦截，请在「**系统设置 → 隐私与安全性**」中查看并手动允许。

在应用的「**设置**」页点击「**打开系统设置**」，然后在「**隐私与安全性 → 辅助功能**」中允许「**自动点击**」。首次授权后若未立即识别，请退出应用再重新打开。

## 使用

1. 点击「**框选区域…**」，在任意显示器拖动选择矩形；按 Esc 取消。
2. 选择「**区域中心**」或「**区域内随机**」。应用执行鼠标左键单击。
3. 设置「**点击间隔**」和「**运行时长**」，单位均为秒。
4. 点击「**开始**」。窗口会隐藏，倒计时 3 秒后开始点击。
5. 运行时长结束后自动停止，启动倒计时不计入运行时长。

**随时按 Command + Shift + 句号（⌘⇧.）停止。** 也可从菜单栏重新打开窗口，点击「停止」。关闭窗口后仍可通过菜单栏使用；退出应用会停止点击。运行时鼠标指针会移到点击位置。

点击间隔范围为 **0.05–3600 秒**，运行时长范围为 **1–86400 秒**。电脑睡眠经过的时间计入运行时长；唤醒时如果已经超时，应用会直接停止，不补发点击。显示器布局变化会停止运行并清除保存的区域。

## 语言与外观

- 通过可见的语言切换控件选择「**简体中文**」「**English**」或「**跟随系统**」。
- 在「**设置**」页选择「**浅色**」「**深色**」或「**跟随系统**」。
- 应用会记住语言、主题、点击参数和框选区域。

## 下载与反馈

- [最新版本](https://github.com/etanxing/regionclick-releases/releases/latest)
- [反馈问题](https://github.com/etanxing/regionclick-releases/issues)
- [Homebrew Tap](https://github.com/etanxing/homebrew-tap)

本公开仓库用于提供安装包、使用说明、版本记录和问题反馈。应用源码保存在私有仓库。
