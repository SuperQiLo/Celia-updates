# Celia 下载与更新

本仓库用于分发 **Celia Windows x64** 安装包和签名更新文件。源码开发在独立仓库进行。

当前预览版为 **0.2.2-rc.3**。请从 [Releases](https://github.com/SuperQiLo/Celia-updates/releases/latest) 下载以 `.exe` 结尾的安装程序。安装后可从桌面或开始菜单打开 **Celia**。

每个版本的公开文件包括：

- `celia-<版本>-win-x64-unsigned.exe`：安装程序。
- 对应的 `.exe.blockmap`：差分下载使用的块索引。
- `nightly.json`：带 Celia 发布签名的更新清单。

首次安装已配置更新渠道的版本后，后续版本可通过应用左下角更新入口下载，并在确认后安装和重启。也可从 **应用 → 检查更新** 主动检查。差分条件不满足时会下载完整安装包。

Celia 会在下载安装包前验证更新清单的发布签名，并校验下载结果。发布私钥不会上传到本仓库，也不会包含在安装包中。独立的发布签名不等同于 Windows Authenticode，未签名安装程序仍可能显示 Windows 提示。

本版本安装包的 SHA-256：

```text
44d42f3c14ae76a953608915f850a9c58e631821369d5d1d4fc8ac982d3844c0
```

---

This repository distributes Celia Windows x64 installers, blockmaps, and signed update metadata. The current preview is **0.2.2-rc.3**. Download the `.exe` installer from [Releases](https://github.com/SuperQiLo/Celia-updates/releases/latest), then open **Celia** from the desktop or Start menu.

Configured installations can use the in-app update control or **Application → Check for updates**. Update metadata is authenticated with Celia's release key before downloading. Downloads are checksum verified, and installation requires confirmation. Release signing does not grant Windows Authenticode trust. Publishing credentials and private keys are never distributed here.
