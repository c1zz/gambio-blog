# Release-Angebot und Versionshistorie

Seit dem 11. November 2026 steht in dieser Testphase nur das aktuelle geprüfte Release je Modul im öffentlichen Download- und Updateangebot. Ältere Releases und ihre angehängten Installer, Prüfsummen und Signaturdateien wurden entfernt. Das bedeutet nicht, dass jede ältere Version einen schweren Fehler enthielt: Auch abgelöste Teststände wurden aus dem Angebot genommen, damit die Auswahl eindeutig bleibt.

Tags und Commit-Historie bleiben unverändert. Frühere Dateien einschließlich damaliger Installer sind dadurch weiterhin über die Git-Historie einsehbar; die Bereinigung entfernt die Release-Downloads und ihre Einträge im Updateangebot. Alte Workflow-Läufe oder Tags dürfen nicht erneut zur Veröffentlichung zurückgezogener Pakete verwendet werden. Bereits veröffentlichte Pakete werden niemals unter derselben Versionsnummer mit anderen Bytes ersetzt.

Aktuelles Release: **[v0.48.15-rc.1](https://github.com/c1zz/gambio-blog/releases/tag/v0.48.15-rc.1)**. Es bleibt ein Release Candidate mit dokumentierten Prüfgrenzen. Für eine vorhandene Installation zuerst sichern und den aktuellen Updateweg aus der [Installationsanleitung](INSTALLATION.md) verwenden. Sehr alte Stände ohne integrierten Updater benötigen den aktuellen Root-Installer; bei beiden Modulen zuerst den Blog aktualisieren.

## Dokumentierte wichtige Korrekturen

| Frühere Version / Verhalten | Korrektur | Bedeutung |
|---|---|---|
| Blog 0.44.0: Blog-Schreibaktionen prüften Adminstatus und CSRF, aber nicht die nativen Schreib-/Löschrechte | [0.45.0](https://github.com/c1zz/gambio-blog/blob/v0.45.0-rc.1/RELEASE_NOTES.md) | Sicherheitsrelevante Rechteprüfung für eingeschränkte Adminzugänge ergänzt. |
| Blog 0.47.1: Bei vollständiger Datenlöschung blieben Einstellungen für Update-Hinweise zurück | [0.47.2](https://github.com/c1zz/gambio-blog/blob/v0.47.2-rc.1/RELEASE_NOTES.md) | Vollständige Löschung umfasst auch diese Einstellungen; normale Deinstallation erhält weiterhin Inhalte. |
| Blog 0.47.0: Sortierung nach technischem Veröffentlichungszeitpunkt führte bei Importen zu unerwarteter Reihenfolge | [0.47.1](https://github.com/c1zz/gambio-blog/blob/v0.47.1-rc.1/RELEASE_NOTES.md) | Einstellbare Reihenfolge, standardmäßig neuestes Artikeldatum zuerst. |

Diese konkret dokumentierten Befunde sind keine pauschale Aussage über jede historische Version. Die aktuelle Version enthält die Korrekturen. Historische Testergebnisse gelten nur für den dort genannten Prüfumfang; sie sind kein unabhängiges Codeaudit.

## Am 11. November 2026 aus dem Release-Angebot entfernt

Die Links führen zur erhaltenen Versionshistorie, nicht zu einem empfohlenen Installationspaket. Die damaligen Release-Beschreibungen sind zusätzlich als [historische Metadaten](release-history.json) archiviert; darin enthaltene Downloadhinweise sind überholt.

| Version | Ursprünglich veröffentlicht (UTC) | Status |
|---|---|---|
| [v0.48.3-rc.1](https://github.com/c1zz/gambio-blog/tree/v0.48.3-rc.1) | 2026-11-11 | Abgelöst; Release-Downloads entfernt |
| [v0.48.0-rc.1](https://github.com/c1zz/gambio-blog/tree/v0.48.0-rc.1) | 2026-11-11 | Abgelöst; Release-Downloads entfernt |
| [v0.47.4-rc.1](https://github.com/c1zz/gambio-blog/tree/v0.47.4-rc.1) | 2026-11-11 | Abgelöst; Release-Downloads entfernt |
| [v0.47.3-rc.1](https://github.com/c1zz/gambio-blog/tree/v0.47.3-rc.1) | 2026-11-10 | Abgelöst; Release-Downloads entfernt |
| [v0.47.2-rc.1](https://github.com/c1zz/gambio-blog/tree/v0.47.2-rc.1) | 2026-11-10 | Abgelöst; Release-Downloads entfernt |
| [v0.47.1-rc.1](https://github.com/c1zz/gambio-blog/tree/v0.47.1-rc.1) | 2026-11-10 | Abgelöst; Release-Downloads entfernt |
| [v0.47.0-rc.1](https://github.com/c1zz/gambio-blog/tree/v0.47.0-rc.1) | 2026-11-10 | Abgelöst; Release-Downloads entfernt |
| [v0.46.1-rc.1](https://github.com/c1zz/gambio-blog/tree/v0.46.1-rc.1) | 2026-11-10 | Abgelöst; Release-Downloads entfernt |
| [v0.46.0-rc.1](https://github.com/c1zz/gambio-blog/tree/v0.46.0-rc.1) | 2026-11-10 | Abgelöst; Release-Downloads entfernt |
| [v0.45.0-rc.1](https://github.com/c1zz/gambio-blog/tree/v0.45.0-rc.1) | 2026-11-10 | Abgelöst; Release-Downloads entfernt |
| [v0.44.0-rc.1](https://github.com/c1zz/gambio-blog/tree/v0.44.0-rc.1) | 2026-11-09 | Abgelöst; Release-Downloads entfernt |
| [v0.43.0-rc.1](https://github.com/c1zz/gambio-blog/tree/v0.43.0-rc.1) | 2026-11-09 | Abgelöst; Release-Downloads entfernt |
| [v0.42.0-rc.2](https://github.com/c1zz/gambio-blog/tree/v0.42.0-rc.2) | 2026-11-09 | Abgelöst; Release-Downloads entfernt |
| [v0.40.2-rc.1](https://github.com/c1zz/gambio-blog/tree/v0.40.2-rc.1) | 2026-11-07 | Abgelöst; Release-Downloads entfernt |

Am 11. November 2026 wird auch **v0.48.4-rc.1** nach Veröffentlichung und Downloadprüfung des neuen Stands abgelöst. Seine Beschreibung ist in [release-history.json](release-history.json) gesichert; Tag und Commit bleiben erhalten.
