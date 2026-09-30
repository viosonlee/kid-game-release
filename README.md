# 泡泡语言练习 · 安装包分发

本仓库仅用于分发 Android 安装包与应用更新清单，不包含应用源码或签名私钥。

## 安装与更新

[下载最新 APK](https://github.com/viosonlee/kid-game-release/releases/latest/download/app-debug.apk) · [查看所有版本](https://github.com/viosonlee/kid-game-release/releases)

当前已发布 1.0.1（`v1.0.1-2`）。

- 首个版本：1.0.1（versionCode 2），调试版包名 `com.kidslanguage.companion.debug`。
- 首次需要手动覆盖安装；后续可在应用的家长设置中检查更新。
- 请保持同一包名与签名覆盖安装，不要先卸载旧版，以保留本机学习记录。
- 每个 Release 同时提供 `app-debug.apk` 和 `update-debug.json`，由应用校验版本、大小、SHA-256 和签名后调用 Android 安装器。

默认更新地址：

```text
https://github.com/viosonlee/kid-game-release/releases/latest/download/update-debug.json
```

默认更新地址已生效。发布者将新的已签名 APK 和对应 JSON 更新到 `artifacts/` 并通过 SSH 推送 main 后，GitHub Actions 会校验签名与版本、自动发布到 Releases。

APK 通过 Git LFS 传入工作流，用户从 Releases 下载。无需在仓库上传签名私钥；历史 LFS 包占用账户存储额度，免费额度以 GitHub 官方计费说明为准。
