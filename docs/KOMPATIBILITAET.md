# Teststand und Grenzen

**Blog 0.47.1-rc.1**, 10. November 2026. KI unverändert 0.12.0.

Gezielter Sortierungsfix im vorhandenen **Gambio 26.11.0, PHP 8.2.31, MariaDB 10.10, Malibu**, Shop-Unterverzeichnis `/shop/`:

- Exaktes neues Paket über den nativen Root-Installer von 0.47.0 aktualisiert; Installer entfernt, alle installierten Dateien gegen das Paket geprüft.
- 78 Artikel (65 öffentlich, 13 privat), 81 Fassungen und 100 Bilder erhalten.
- 101 native HTTP-/Datenprüfungen: alle drei Sortierungen, elf Übersichtsseiten ohne Lücken/Duplikate, sieben Kategorien, erste/mittlere/letzte Nachbarartikel, Speicherung der Auswahl, ungültige Werte und native CSRF-Ablehnung ohne Schreibwirkung.
- Isolierte PHP-Suite einschließlich 13 neuer Sortierungsfälle, 83 Geräte-/Seitenfensterprüfungen und 189 Darstellungsprüfungen bestanden. Zwei Builderprüfungen und Syntax von 88 PHP-Dateien bestanden.
- 18 automatisierte Chromiumprüfungen bestanden: tatsächliche Datumssortierung, übersetzte Auswahl und gespeicherter Standard, native Verwaltung sowie Artikelbilder auf Desktop/Mobil. Sortierauswahl zusätzlich visuell kontrolliert.

Die Sortierung liest veröffentlichte Metadaten und sortiert vor der Seitenauswahl in PHP. Dadurch werden keine datenbankspezifischen JSON-Funktionen oder Schemaänderungen benötigt. Der Speicherbedarf wächst mit der Anzahl öffentlicher Metadatensätze; ein neuer Lasttest mit sehr großen Blogs wurde nicht ausgeführt. Artikeltexte/Entwürfe werden für die Übersicht nicht geladen.

Kein weiterer vollständiger Shop-Neuaufbau und kein neuer nativer Erstinstallationstest für diesen gezielten Fix. Der frische GX26-Ausgangstest des Vorgängers bleibt im [Teststand von 0.47.0](https://github.com/c1zz/gambio-blog/blob/v0.47.0-rc.1/docs/KOMPATIBILITAET.md) dokumentiert. Die temporäre Migrationstestumgebung bleibt auf ausdrücklichen Nutzerauftrag für die laufende Migration verfügbar. Haupttestshop und Live-Shop wurden nicht verändert.

Keine Erweiterung der Freigabe auf GX5, Honeygrid, PHP 8.3, MySQL 8.4 oder weitere Versionen. Kein unabhängiger Penetrationstest. Die Herkunftssignatur wird im Shop nicht kryptografisch geprüft. [Maschinelle Ergebnisse und Paketprüfsumme](test-results.json).
