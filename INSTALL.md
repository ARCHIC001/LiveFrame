# 安装 LiveFrame 2.4.1

适用于 Apple 芯片 Mac（M1 及后续系列），macOS 13 Ventura 或更新版本。此安装包不适用于 Intel Mac。已内置 FFmpeg，无需安装 Homebrew、Python 或开发工具。

1. 打开 `LiveFrame-2.4.1-macOS-arm64.dmg`。
2. 将 `LiveFrame.app` 拖入同一窗口中的 `Applications` 文件夹。
3. 在「应用程序」中打开 LiveFrame，导入你的视频开始制作。
4. 安装完成后弹出磁盘映像。

更新已有版本时，请先导出当前作品，再退出旧版并替换应用。当前版本不持久化未导出的编辑草稿。

## 首次打开

本发行版使用 ad-hoc 签名，尚未使用 Apple Developer ID 签名和公证，因此首次下载后 macOS 可能提示开发者无法验证。确认文件来自本项目的 GitHub Releases 后，先尝试打开，再到「系统设置 → 隐私与安全性」查看该应用的「仍要打开」选项。无需关闭整个系统的 Gatekeeper。

Apple 官方说明：https://support.apple.com/zh-cn/102445

若提示文件损坏，先重新下载，并对照 Release 中的 `SHA256SUMS.txt` 检查完整性；不要忽略恶意软件告警。

## 导出与传输

- **Android**：得到一个内含 MP4 的动态 JPG。以文件原件传至手机的 `Pictures` / `DCIM`，由相册识别。不同厂商、系统和相册版本的兼容性需实机确认。
- **iOS**：得到一对匹配的 JPG + MOV。推荐在导出完成窗口点击「保存到照片」，通过 iCloud 照片同步至 iPhone。
- 也可导出普通 MOV 或循环 GIF。

模板控制时长和尺寸；左上角 Logo 切换 Android / iOS 时同步切换原生实况照片格式。

## 第三方组件

应用通过独立进程使用 FFmpeg 8.0.3 和 x264，采用 GPL-2.0-or-later 许可。对应完整源码、许可和重建脚本位于 `LiveFrame.app/Contents/Resources/ThirdParty`，也提供为 GitHub Release 的 `LiveFrame-2.4.1-ThirdParty-Sources.zip` 附件。LiveFrame 应用源码未在该仓库公开。

问题反馈：https://github.com/ARCHIC001/LiveFrame/issues
