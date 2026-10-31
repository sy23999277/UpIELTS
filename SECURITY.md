# Security

## 官方下载

UpIELTS 只通过以下位置发布：

https://github.com/sy23999277/UpIELTS/releases

- 包名：`com.jiubei.words`
- 当前版本：`2.9`
- APK SHA256：`07ed69034401c6c1d522c5a093039b8b57a04b858251227fbe54cff33e662611`

如果你从其他网站、群聊或网盘下载 APK，请视为不可信。其他渠道的安装包可能被二次打包或加入恶意代码。

## 校验下载文件

Windows PowerShell：

```powershell
Get-FileHash .\UpIELTS-2.9.apk -Algorithm SHA256
```

Android 终端：

```bash
sha256sum UpIELTS-2.9.apk
```

结果应等于上面的 SHA256。

## 更新安全

- App 内更新只读取 `https://github.com/sy23999277/UpIELTS` 的 Release。
- 下载后会校验 `latest.json` 中的 SHA256。
- Android 还会校验 APK 签名；签名不同则拒绝覆盖安装。
- 签名证书 SHA256：`76:1B:E3:A5:A6:A1:28:8C:92:DC:A9:CE:AB:9E:67:AF:D7:55:16:29:66:88:67:1D:5E:3D:1C:D4:48:90:20:AA`

## 报告安全问题

请不要在公开 Issue 中贴出可直接利用的攻击细节。

优先使用仓库的 **Security → Report a vulnerability**（GitHub Security Advisory）私下报告；如果该功能未开启，可以开一个不含敏感细节的 Issue，说明“需要私下联系”。

## 维护者检查清单

- GitHub 已开启 2FA。
- 保存 2FA 恢复码。
- 签名密钥和密码配置只保存在本机/离线备份，不进入 Git。
- 发布前确认 APK 来自官方构建，并重新计算 SHA256。
- 不在任何 Issue、截图、日志中暴露 keystore、密码、Token。

## 2FA 开启步骤

1. GitHub → 右上角头像 → **Settings**。
2. **Password and authentication**。
3. **Enable two-factor authentication**。
4. 用身份验证器 App 扫码，保存恢复码。

> 本文件只说明安全实践，不构成法律或安全担保。
