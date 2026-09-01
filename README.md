# StockWidget Releases

StockWidget Windows 商业版安装包发布仓库。

本仓库仅用于分发官方安装包、版本说明与校验信息，不包含商业版源代码。

## Downloads

请从 [GitHub Releases](https://github.com/Giiiiithuuuuub/StockWidget-Releases/releases)
页面下载最新正式版本。当前仓库初始化阶段尚无正式 Release。

## Verification

每个正式版本会提供 SHA-256 校验信息。下载后可在 PowerShell 中运行：

```powershell
Get-FileHash ".\StockWidget-Setup-x.y.z.exe" -Algorithm SHA256
```

将结果与对应版本提供的校验值逐字符核对。

## System

- Windows 10 / 11 x64
- current-user 安装
- 安装器当前可能未进行 Authenticode 签名；请核对来源与 SHA-256

## Updates

StockWidget 只在用户主动点击“检查更新”时查询本仓库的最新正式 Release。
应用不会自动下载或自动安装更新。

## Source

商业版源代码不在本公开发布仓库中。本仓库不接受或分发源代码包。

## Legal

第三方组件和图标许可摘要见 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)。
本仓库没有为 StockWidget 商业源代码授予开源许可。
