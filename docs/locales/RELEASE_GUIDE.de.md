# PCssak 0.8.0 – Leitfaden für den unsignierten kostenlosen Early Access

[English README](../../README.md) · [Bekannte Einschränkungen](../KNOWN-LIMITATIONS.md) ·
[Standard für Release-Dateien](../RELEASE_ASSET_STANDARD.md) · [Support](../../SUPPORT.md)

## Status

Der erste öffentliche Test ist jetzt als unveränderliches GitHub-Prerelease
[v0.8.0](https://github.com/pcssakinc/pcssak-pc-optimizer-releases/releases/tag/v0.8.0)
für Windows x64 verfügbar.

- Version: `0.8.0`
- Paket: `PCSSAK_0.8.0_x64_Portable.zip`
- Format: portables ZIP, kein Installationsprogramm
- Signatur: im kostenlosen Early Access absichtlich unsigniert
- SHA-256: `88d9e2012b329242ab2903268f46ec5b4a6f69d06582d262cf706704cd0406aa`

Windows kann „Unbekannter Herausgeber“, SmartScreen- oder Virenschutzwarnungen anzeigen.
Signierung, Herausgeberprüfung, externe Rechtsprüfung, SmartScreen-Reputation und die
vollständige Windows-Testmatrix sind aufgeschoben und nicht `PASS`.

## Vor dem Ausführen

1. Laden Sie die Datei nur von der offiziellen Releases-Seite dieses Repositorys herunter.
2. Prüfen Sie den exakten Paketnamen und vergleichen Sie SHA-256 mit `SHA256SUMS.txt`.
3. Führen Sie fehlende, umbenannte oder nicht zum Hash passende Dateien nicht aus.
4. Scannen Sie Archiv und Zielordner und entpacken Sie nur in einen eigenen Benutzerordner.
5. Brechen Sie bei nicht überprüfbarer Herkunft, Integrität, Warnung oder Funktion ab.

Wenn der Benutzer **Nach Updates suchen** auswählt, zeigt PCssak den Status an. Ist eine
neuere Version verfügbar, kann der Benutzer zusätzlich die Schaltfläche zur offiziellen
Downloadseite drücken. Nichts wird automatisch geöffnet, heruntergeladen, ausgeführt,
installiert oder zurückgesetzt.

Melden Sie reproduzierbare, nicht sicherheitskritische Fehler nach Entfernung privater
Daten über [GitHub Issues](https://github.com/pcssakinc/pcssak-pc-optimizer-releases/issues).
Verwenden Sie für ausnutzbare Schwachstellen den [privaten Sicherheitsweg](../../SECURITY.md)
des Repositorys und kein öffentliches Issue.
