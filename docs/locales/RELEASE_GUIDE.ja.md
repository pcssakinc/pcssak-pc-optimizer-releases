# PCssak 0.8.0 未署名無料アーリーアクセスガイド

[English README](../../README.md) · [既知の制限](../KNOWN-LIMITATIONS.md) ·
[リリース資産基準](../RELEASE_ASSET_STANDARD.md) · [サポート](../../SUPPORT.md)

## 状態

最初の公開テスト版は、Windows x64 用の変更不能な GitHub Prerelease
[v0.8.0](https://github.com/pcssakinc/pcssak-pc-optimizer-releases/releases/tag/v0.8.0)
として公開されました。

- バージョン: `0.8.0`
- パッケージ: `PCSSAK_0.8.0_x64_Portable.zip`
- 形式: インストーラーを使用しないポータブル ZIP
- 署名: 無料アーリーアクセスでは意図的に未署名
- SHA-256: `88d9e2012b329242ab2903268f46ec5b4a6f69d06582d262cf706704cd0406aa`

Windows に「不明な発行元」、SmartScreen、またはウイルス対策の警告が表示される
場合があります。署名、発行元確認、外部法務レビュー、SmartScreen 評価、および
完全な Windows 実機テストは延期されており、`PASS` ではありません。

## 実行前の確認

1. このリポジトリの公式 Releases ページからのみダウンロードします。
2. 正確なパッケージ名を確認し、SHA-256 を `SHA256SUMS.txt` と比較します。
3. ファイルがない、名前が違う、またはハッシュが一致しない場合は実行しません。
4. 圧縮ファイルと展開先をスキャンし、ユーザー所有フォルダーにのみ展開します。
5. 出所や完全性を確認できない警告・動作があれば中止して報告してください。

ユーザーが **更新を確認** を押すと、PCssak は状態を表示します。新しいバージョンが
ある場合、ユーザーは別の公式ダウンロードページボタンを押して開くことができます。
ページは自動で開かず、このパッケージを自動でダウンロード、実行、インストール、
またはロールバックしません。

再現可能な一般的な不具合は、個人情報を削除してから
[GitHub Issues](https://github.com/pcssakinc/pcssak-pc-optimizer-releases/issues) で
報告してください。悪用可能な脆弱性は公開 Issue ではなく、リポジトリの
[非公開セキュリティ経路](../../SECURITY.md)を使用してください。
