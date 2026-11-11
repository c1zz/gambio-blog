# Teststand und Grenzen

**Blog 0.48.3-rc.1**, 11. November 2026. KI 0.12.2 unverändert.

Das genaue eingebettete Blogpaket wurde frisch auf **Gambio 26.11.0 / PHP 8.2.31 / MariaDB 10.10 / Malibu** unter `/shop/` nativ installiert. **129 HTTP-/Datenprüfungen und 39 angemeldete Chromiumprüfungen** bestanden: Blog- und Produktsuche, Live-Vorschläge, Ausschluss privater/alter/gelöschter Fassungen, Einstellungen speichern, Modul deaktivieren, Tastaturbedienung, 320/390/768/1440 px und Ergebnisse ohne JavaScript. Die neue visuelle Suchvorschau wurde nativ mit Blogkopf, Ergebnisansicht, Bildschalter und Trefferzahl geprüft; sie lässt gespeicherte Einstellungen unverändert.

Danach wurde der exakte Root-Installer im bestehenden lokalen Migrationstestshop ausgeführt (Blog 0.48.2 → 0.48.3). **35 Prüfungen** bestätigen Abschluss, Installerentfernung, sämtliche Paketdateien und die Suche im vorhandenen Artikelbestand. Inhalte, Fassungen, Kategorien, Weiterleitungen, Medien, gespeicherte Darstellung, KI-Daten und Konfigurationsdateien bleiben erhalten. Weitere 30 lesende Browserprüfungen im aktualisierten Migrationsshop bestätigen die einzelne integrierte Lupe, Schließen per Außenklick und Thumbnails auf 320/390/1440 px. Der Haupttestshop erhielt kein Update.

Die ursprüngliche Migrationsdatenbank, Medien und Konfiguration blieben während des frischen Prüflaufs unverändert; Prüfdatenbank, Prüfbenutzer und Overlay wurden entfernt. Beim beauftragten Update ändern sich erwartungsgemäß Modulstand und native Laufzeit-/Cachedaten; keine pauschale Datenbankgleichheit behauptet.

Zusätzlich bestanden **53 isolierte Chromiumprüfungen** mit echten Smarty-Templates und Beispieldaten: visueller Bereich, ungespeicherte Werte beim Wechsel der Ansicht, Bild-/Kurztextschalter, mobile Liste, Öffnen/Schließen, nur eine sichtbare Lupe, integrierter Submitbutton, Außenklick, Escape, Tastatur-Submit und Darstellung ohne JavaScript. Die isolierte PHP-Suite (einschließlich 44 Suchchecks), zwei Builderprüfungen und die Syntaxprüfung des fertigen Installers bestanden. [Maschineller Prüfbericht](test-results.json).

Kein erneuter vollständiger GitHub-Update- oder Deinstallationslauf. Historischer Löschtest: [Blog 0.47.2 / KI 0.12.1](https://github.com/c1zz/gambio-blog/blob/v0.47.2-rc.1/docs/KOMPATIBILITAET.md). Keine neuen externen KI-Anbieteraufrufe. Die Suche liest veröffentlichte Fassungen stapelweise; noch kein Suchindex und kein Lasttest. Alternative Suchanbieter wie Findologic, andere Themes und andere Gambio-/PHP-Versionen sind für die Suche ungeprüft. Malibu blendet mobile Live-Vorschläge nativ aus.

Keine pauschale Kompatibilitätszusage und kein unabhängiges Codeaudit. Der Shop prüft Paketintegrität, weiterhin keine kryptografische Herkunftssignatur.
