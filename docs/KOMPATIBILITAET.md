# Teststand und Grenzen

**Blog 0.47.3-rc.1**, 10. November 2026.

Das exakte eingebettete Paket wurde in einem frischen **Gambio 26.11.0 / PHP 8.2.31 / MariaDB 10.10 / Malibu** unter `/shop/` nativ installiert. Die getrennte Prüfdatenbank und temporären Datei-Overlays wurden anschließend entfernt. Der bestehende Migrationsbestand und der Haupttestshop bleiben unverändert.

Geprüft wurden der Theme-Standard bei Installation, die native Speicherung eigener Abstände, die Grenzen 0 und 240 px, die Ablehnung ungültiger Werte ohne Änderung des gespeicherten Werts und die Rückkehr zum Theme-Standard. Blogübersicht, Kategorien und Artikelseiten geben den eigenen Wert aus; die Shopstartseite erhält keine solche Regel. Artikel, Entwürfe, Revisionen, Kategorien, Weiterleitungen und Medien bleiben erhalten.

Chromium prüfte die echten Admin-Steuerelemente, Tastaturbedienung, Synchronisierung von Regler und Zahl, Speicherstatus, Formularreset und den c1zz-Stil bei 390/768/1440 px. Die öffentliche Malibu-Seite verwendet den gespeicherten Abstand; ihre Mindesthöhe bleibt bestehen. Zusätzlich bestehen die isolierte PHP-Suite, zwei Builderprüfungen und 79 isolierte DOM-/Editorprüfungen. [Maschineller Prüfbericht](test-results.json).

Die zugrunde liegende CSS-Regel wurde zuvor mit 65 lesenden Browserprüfungen auf Übersicht, Artikel, Kategorie, Startseite und Produktseite untersucht. Breiten, Footer-Reserve und Mindesthöhe bleiben unverändert. Zusätzliche Theme-Abstände können weiterhin Leerraum erzeugen. Kein Nachweis für andere Themes oder Shopversionen.

Der vollständige GitHub-Updateablauf und die Deinstallation wurden für diese Darstellungsänderung nicht erneut geprüft. Der [Deinstallationsvergleich des Vorgängers](https://github.com/c1zz/gambio-blog/blob/v0.47.2-rc.1/docs/KOMPATIBILITAET.md) bleibt auf diesen Stand bezogen: eigene Tabellen und Update-Einstellungen werden bei bestätigter vollständiger Löschung entfernt; native inaktive Modulmarker, Sprachcache und Datenbankzähler bleiben bestehen.

Keine pauschale Zusage für andere Gambio-/PHP-/Theme-Versionen und kein unabhängiges Codeaudit. Der Shop prüft Paketintegrität, weiterhin keine kryptografische Herkunftssignatur.
