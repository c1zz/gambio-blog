# Teststand und Grenzen

**Blog 0.47.4-rc.1**, 11. November 2026.

Das exakte eingebettete Paket wurde in einem frischen **Gambio 26.11.0 / PHP 8.2.31 / MariaDB 10.10 / Malibu** unter `/shop/` nativ installiert. 41 gezielte HTTP-/Datenprüfungen prüfen die tatsächlichen Admin-Dropdowns, die Speicherung der neuen Werte für Desktop/Tablet/Mobil, Seitennavigation, die Ablehnung ungültiger Werte und Datenerhalt. Prüfdatenbank und temporäre Dateien sind entfernt.

Im bestehenden lokalen Migrationstestshop wurde das exakte Paket anschließend von 0.47.3 auf 0.47.4 aktualisiert. 53 Prüfungen bestätigen Paketintegrität, native Speicherung und Seitennavigation ohne doppelte Artikel zwischen den ersten beiden Seiten. Artikel, Entwürfe, Fassungen, Kategorien, Weiterleitungen, Medien und KI-Daten bleiben erhalten. Vorherige Darstellungseinstellungen wurden nach dem Test vollständig wiederhergestellt. Der Haupttestshop erhielt kein Update.

Beim Vergleich der gesamten ursprünglichen Shopdatenbank änderten sich native Anmeldefelder in `customers_info` sowie ein Besuchereintrag in `whos_online`. Deshalb wird kein bytegleicher Gesamtzustand behauptet. Sämtliche Modultabellen, Medien und Konfigurationsdateien blieben während des frischen Prüflaufs unverändert.

Zusätzlich bestanden die isolierte PHP-Suite, zwei Builderprüfungen und 79 isolierte Chromium-DOM-/Editorprüfungen. Die neuen Dropdowns wurden nativ über HTTP geprüft, ohne erneuten angemeldeten Chromiumlauf. [Maschineller Prüfbericht](test-results.json).

Der vollständige GitHub-Updateablauf und die Deinstallation wurden für diese Auswahländerung nicht erneut geprüft. Der [Deinstallationsvergleich von 0.47.2](https://github.com/c1zz/gambio-blog/blob/v0.47.2-rc.1/docs/KOMPATIBILITAET.md) bleibt auf diesen Stand bezogen.

Keine pauschale Zusage für andere Gambio-/PHP-/Theme-Versionen und kein unabhängiges Codeaudit. Der Shop prüft Paketintegrität, weiterhin keine kryptografische Herkunftssignatur.
