# c1zz-blog für Gambio · 0.45.0-rc.1

Dieses Update behebt die Befunde des lokalen Audits und vereinheitlicht die Verwaltung.

- Blogaktionen prüfen jetzt native Schreibrechte zusätzlich zu Anmeldung und CSRF. Das Entfernen von Artikeln, Kategorien, Beispielinhalten und Medien benötigt zusätzlich Löschrechte.
- Darstellungsänderungen bleiben bei Speicherfehlern erhalten. Der ursprüngliche Versionsvergleich schützt weiterhin vor dem Überschreiben paralleler Änderungen.
- Speicherbuttons werden nur bei Änderungen aktiv. Der Vorschauhinweis zeigt ungespeicherte Änderungen nur dann an, wenn welche vorhanden sind.
- Kompakte, gut sichtbare Speicherleisten, gestaltete Dateiauswahl, deutlicher Shortcode und hervorgehobene Sperrhinweise.
- Mobil erscheint das Kategorienmenü aufklappbar oberhalb. Die Vorschau lässt sich per Klick und Tastatur öffnen; Tablet und Desktop unterstützen weiterhin die seitliche Darstellung.
- Der Modulordner heißt jetzt `GXModules/c1zz/c1zzblog`. Der Installer übernimmt den bisherigen Ordner `StandaloneBlog`; unbekannte Dateien, Symlinks und doppelte Ordner blockieren die Übernahme.

Bei installiertem KI-Modul **zuerst Blog 0.45.0, anschließend KI 0.10.0** aktualisieren. Während dieses gemeinsamen Updates die KI-Verwaltung nicht verwenden. Interne Tabellen- und Controllerkennungen bleiben für vorhandene Daten erhalten. Keine Änderungen an Gambio-Kerndateien.

Vor dem Update Datenbank, Medien und Module zusammen sichern. Nur `c1zz-blog-install-0.45.0.php` in den Shopordner hochladen und den geführten Ablauf starten. Der Installer entfernt sich nach erfolgreichem Abschluss. [Installation](docs/INSTALLATION.md) · [Teststand und Grenzen](docs/KOMPATIBILITAET.md).
