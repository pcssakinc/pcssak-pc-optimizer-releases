# PCssak 0.8.0 未簽署免費搶先體驗指南

[English README](../../README.md) · [已知限制](../KNOWN-LIMITATIONS.md) ·
[發行資產標準](../RELEASE_ASSET_STANDARD.md) · [支援](../../SUPPORT.md)

## 狀態

本次文件變更不會發佈標籤、Release、執行檔或壓縮檔。第一個公開測試版準備完成後，
將以 Windows x64 GitHub Prerelease 的形式提供。

- 版本：`0.8.0`
- 套件：`PCSSAK_0.8.0_x64_Portable.zip`
- 格式：免安裝可攜式 ZIP
- 簽署：免費搶先體驗階段刻意不進行程式碼簽署

Windows 可能顯示「未知的發行者」、SmartScreen 或安全軟體警告。程式碼簽署、
發行者驗證、外部法律審查、SmartScreen 信譽與完整 Windows 實機矩陣均已延後，
並非 `PASS`。

## 執行前檢查

1. 僅從本儲存庫的官方 Releases 頁面下載。
2. 確認正確的套件名稱，並將 SHA-256 與 `SHA256SUMS.txt` 比對。
3. 檔案缺失、遭重新命名或雜湊不符時請勿執行。
4. 掃描壓縮檔與解壓縮目錄，且只解壓縮到使用者擁有的資料夾。
5. 若無法驗證來源、完整性、警告或行為，請停止使用並回報。

更新檢查只會在使用者要求時開啟官方頁面。PCssak 不會自動下載、執行、安裝或
復原此套件。
