# StockWidget Releases

StockWidget Windows 商业版官方发布仓库。

本仓库仅用于分发正式安装器、版本说明、静态更新清单与 SHA-256 校验信息，**不包含商业版源代码**。

## 下载

请从 [GitHub Releases](https://github.com/Giiiiithuuuuub/StockWidget-Releases/releases) 下载最新正式版本。

正式安装包命名：

```text
StockWidget-Setup-x.y.z.exe
```

## 安装与升级

- Windows 10 / 11 x64
- current-user 安装，不要求管理员权限
- 新版本可直接覆盖安装旧版本
- 用户配置、持仓账本、备份及当前 Windows 用户授权信息会保留

## SHA-256 校验

每个正式版本都会提供 SHA-256。下载后可在 PowerShell 执行：

```powershell
Get-FileHash ".\StockWidget-Setup-x.y.z.exe" -Algorithm SHA256
```

请将结果与对应 Release 以及 `latest.json` 中的校验值逐字符核对。

> 当前安装器可能未进行 Authenticode 签名。Windows SmartScreen 可能提示风险，请确认下载来源并核对 SHA-256，不建议为运行程序关闭系统安全功能。

## 更新检查

StockWidget 只在用户主动点击“检查更新”时联网，不自动下载或自动安装。

客户端读取本仓库 `main` 分支的静态更新清单：

```text
https://raw.githubusercontent.com/Giiiiithuuuuub/StockWidget-Releases/main/latest.json
```

`latest.json` 包含：

- `version`
- `url`
- `installer_url`
- `sha256`
- `notes`

发布新版本时，必须先完成 GitHub Release、安装包上传与 SHA-256 核验，**最后**更新 `latest.json`，避免客户端提前看到尚未就绪的版本。

## 源代码

商业版源代码维护在私有仓库，不在本公开发布仓库中。本仓库不接受或分发商业源码包。

## 法律与第三方组件

第三方组件和图标许可摘要见 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)。

本仓库没有为 StockWidget 商业源代码授予开源许可。
