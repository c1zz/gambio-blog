# c1zz-blog 0.48.0-rc.1

Die vorhandene **Gambio-Shopsuche findet jetzt auch veröffentlichte Blogartikel**. Auf dem Desktop erscheinen Blogtreffer als eigene Gruppe in den Live-Vorschlägen; Produkte bleiben erhalten. Auf Mobilgeräten genügt das vorhandene Suchfeld: Enter öffnet die gemeinsame Ergebnisseite. Malibu blendet Live-Vorschläge mobil weiterhin nativ aus.

Unter **Darstellung → Alle Einstellungen → Suche** lassen sich Blogsuche und Live-Vorschläge einschalten sowie Liste/Grid, Trefferanzahl, Bilder und Kurztexte einstellen. Trefferkarten übernehmen Farben, Schrift und Abstände der Blogdarstellung; mobil erscheinen sie als Liste. Der Menülink heißt jetzt **c1zz-blog**.

Gesucht wird in Titel, Schlagwörtern, Kurztext und veröffentlichtem Artikeltext. Alle Wörter müssen vorkommen (3–120 Zeichen, höchstens acht Wörter). Treffer werden nach Relevanz, dann Artikeldatum sortiert. Entwürfe, alte Fassungen und Papierkorbinhalte bleiben ausgeschlossen. Produktfilter betreffen weiterhin nur Produkte.

Die exakten eingebetteten Pakete Blog 0.48.0 / KI 0.12.2 wurden frisch auf **GX26.11.0 / PHP 8.2.31 / MariaDB 10.10 / Malibu** unter `/shop/` installiert: 68 native HTTP-/Datenchecks und 19 Chromiumchecks bestanden. Danach wurden beide exakten Root-Installer im bestehenden lokalen Migrationstestshop ausgeführt: 31 Update- und Datenerhaltprüfungen bestanden. [Prüfumfang und Grenzen](docs/KOMPATIBILITAET.md).

Zum Aktualisieren **Update / Aktualisieren → Testversionen berücksichtigen → Nach Updates suchen** öffnen und das Update nach einer Sicherung selbst starten. Kein erneuter vollständiger GitHub-Updatetest oder Deinstallationslauf. Andere Suchanbieter, Themes und große Artikelbestände wurden nicht geprüft. Der Shop prüft Paketintegrität, keine kryptografische Herkunftssignatur. [Herkunft und Integrität](SECURITY.md); kein unabhängiges Codeaudit.
