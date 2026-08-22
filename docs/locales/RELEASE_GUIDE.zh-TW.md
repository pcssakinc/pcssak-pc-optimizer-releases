# PCssak 0.8.0 未簽署免費搶先體驗指南

[English README](../../README.md) · [已知限制](../KNOWN-LIMITATIONS.md) ·
[發行資產標準](../RELEASE_ASSET_STANDARD.md) · [支援](../../SUPPORT.md)

## 狀態

第一個公開測試版現已作為 Windows x64 不可變 GitHub Prerelease
[v0.8.0](https://github.com/pcssakinc/pcssak-pc-optimizer-releases/releases/tag/v0.8.0)
發佈。

- 版本：`0.8.0`
- 套件：`PCSSAK_0.8.0_x64_Portable.zip`
- 格式：免安裝可攜式 ZIP
- 簽署：免費搶先體驗階段刻意不進行程式碼簽署
- SHA-256：`88d9e2012b329242ab2903268f46ec5b4a6f69d06582d262cf706704cd0406aa`

Windows 可能顯示「未知的發行者」、SmartScreen 或安全軟體警告。程式碼簽署、
發行者驗證、外部法律審查、SmartScreen 信譽與完整 Windows 實機矩陣均已延後，
並非 `PASS`。

## 執行前檢查

1. 僅從本儲存庫的官方 Releases 頁面下載。
2. 確認正確的套件名稱，並將 SHA-256 與 `SHA256SUMS.txt` 比對。
3. 檔案缺失、遭重新命名或雜湊不符時請勿執行。
4. 掃描壓縮檔與解壓縮目錄，且只解壓縮到使用者擁有的資料夾。
5. 若無法驗證來源、完整性、警告或行為，請停止使用並回報。

使用者按下 **檢查更新** 後，PCssak 會顯示狀態。如果有新版本，使用者可以另外按下
官方下載頁面按鈕來開啟該頁面。頁面不會自動開啟，PCssak 也不會自動下載、執行、
安裝或復原此套件。

請移除隱私資料後，透過
[GitHub Issues](https://github.com/pcssakinc/pcssak-pc-optimizer-releases/issues)
回報可重現的非安全問題。可被利用的漏洞請使用本儲存庫的
[私密安全回報途徑](../../SECURITY.md)，不要建立公開 Issue。
