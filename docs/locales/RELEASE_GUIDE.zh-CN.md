# PCssak 0.8.0 未签名免费抢先体验指南

[English README](../../README.md) · [已知限制](../KNOWN-LIMITATIONS.md) ·
[发布资产标准](../RELEASE_ASSET_STANDARD.md) · [支持](../../SUPPORT.md)

## 状态

本次文档变更不会发布标签、Release、可执行文件或压缩包。首个公开测试版准备完成后，
将以 Windows x64 GitHub Prerelease 的形式提供。

- 版本：`0.8.0`
- 软件包：`PCSSAK_0.8.0_x64_Portable.zip`
- 格式：免安装便携式 ZIP
- 签名：免费抢先体验阶段有意不进行代码签名

Windows 可能显示“未知发布者”、SmartScreen 或安全软件警告。代码签名、发布者验证、
外部法律审核、SmartScreen 信誉以及完整 Windows 实机矩阵均已延期，并非 `PASS`。

## 运行前检查

1. 仅从本仓库的官方 Releases 页面下载。
2. 确认准确的软件包名称，并将 SHA-256 与 `SHA256SUMS.txt` 比较。
3. 文件缺失、被改名或哈希不匹配时，请勿运行。
4. 扫描压缩包和解压目录，并且只解压到用户拥有的文件夹。
5. 如果无法验证来源、完整性、警告或行为，请停止使用并报告。

用户点击 **检查更新** 后，PCssak 会显示状态。如果有新版本，用户可以另外点击
官方下载页面按钮来打开该页面。页面不会自动打开，PCssak 也不会自动下载、运行、
安装或回滚此软件包。

请删除隐私信息后，通过
[GitHub Issues](https://github.com/pcssakinc/pcssak-pc-optimizer-releases/issues)
报告可重现的非安全缺陷。对于可被利用的漏洞，请使用本仓库的
[私密安全报告途径](../../SECURITY.md)，不要发布公开 Issue。
