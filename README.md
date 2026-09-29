# 泡泡语言练习 · 安装包分发

本仓库仅用于分发 Android 安装包与应用更新清单，不包含应用源码或签名私钥。

## 安装与更新

安装包将在 [Releases](https://github.com/viosonlee/kid-game-release/releases) 发布。当前首个 Release 尚在准备上传。

- 首个版本：1.0.1（versionCode 2），调试版包名 `com.kidslanguage.companion.debug`。
- 首次需要手动覆盖安装；后续可在应用的家长设置中检查更新。
- 请保持同一包名与签名覆盖安装，不要先卸载旧版，以保留本机学习记录。
- 每个 Release 同时提供 `app-debug.apk` 和 `update-debug.json`，由应用校验版本、大小、SHA-256 和签名后调用 Android 安装器。

默认更新地址：

```text
https://github.com/viosonlee/kid-game-release/releases/latest/download/update-debug.json
```

首个包的发布标签为 `v1.0.1-2`。完成该 Release 上传并设为 Latest 后，默认更新地址生效。
