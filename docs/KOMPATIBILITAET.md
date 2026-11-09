# Kompatibilität und Teststand

**Veröffentlichung:** `v0.43.0-rc.1` · **Modul:** `0.43.0` · **Stand:** 9. November 2026.

Aktueller Testfall: **Gambio GX26.11.0, PHP 8.2.31, MariaDB 10.10 und Malibu**.

## Aktuelle Prüfungen

**Aktuelle gemeinsame Abnahme bestanden:** 48 Ablaufprüfungen und 17 Chromium-Prüfungen im frischen GX26-Shop. Beide tatsächlichen Installer wurden nativ ausgeführt und anschließend entfernt. Native De-/Wiederinstallation erhält Blogartikel, Kategorien und Bilder sowie gespeicherte KI-Vorschläge; KI-Zugangsdaten werden bei Deinstallation entfernt. Keine hängende 95-Prozent-Anzeige.

**Update im Haupttestshop bestanden:** sechs Browserprüfungen, beide Installer abgeschlossen und entfernt, alle 180 installierten Nutzdateien geprüft. Inhalte, Medien, Sortiment und verschlüsselte KI-Zugänge unverändert; lediglich der installierte Blogversionswert und seine Paketbelege wurden aktualisiert. 100 PHP-Dateien einschließlich beider Installer syntaktisch geprüft. 119 Anbieter-/Fehlerprüfungen mit simulierten Antworten erneut bestanden. Keine echten KI-Aufrufe für diese Release-Abnahme.


Die genauen Ergebnisse der gemeinsamen Release-Abnahme werden in `test-results.json` dokumentiert: beide fertigen Installer, frischer leerer Blog, getrennte KI-Installation, native De-/Wiederinstallation und Datenerhalt. Die einzige zusätzliche Shopumgebung wurde vollständig entfernt.

Zwei Builderprüfungen für reproduzierbare Pakete und unterschiedliche Release-Zeitstempel bestanden. Alle 152 eingebetteten Blogdateien sind mit Größe, Pfad und SHA-256 verifiziert. Der Admin-Stil wurde gemeinsam mit dem KI-Modul in 16 gezielten Browserprüfungen verglichen; Hinweise stimmen in Schrift, Abständen, Hintergrund und Rahmen überein. Weitere lesende Prüfungen bestätigen rote Entfernen-Aktionen und die Versionsanzeige auf Übersicht, Darstellung und Deinstallationsseite.

## Vorherige Nachweise

Für **0.42.0** bestanden 26 Paketintegritäts-, 39 Archiv-, 32 Login- und 82 Element-CSS-Prüfungen; 19 native Prüfungen zur Adressverwaltung, 12 Chromium-Prüfungen für Weiterleitungen, CSRF, Hilfetexte und Namen sowie 26 Chromium-Prüfungen für Element-CSS. Update von 0.41.0 mit nativen Schritten, Selbstentfernung und Bestandserhalt geprüft. Diese Ergebnisse werden als vorherige Nachweise geführt, nicht als erneute Vollprüfung von 0.43.0.

Die Anmelderückkehr in Firefox und Chromium wurde mit **0.40.2** geprüft. GX4.8.0.3 und GX4.9.6.1 mit Malibu sind ältere geprüfte Grundlagen; sie ersetzen keine Abnahme dieses Kandidaten auf diesen Versionen.

## Grenzen

- Keine allgemeine Zusage für andere GX26-Stände, GX5, Honeygrid oder andere Themes.
- Für diesen Kandidaten keine neue vollständige Prüfung in Shop-Unterverzeichnissen; ältere Unterverzeichnisprüfungen bleiben historische Nachweise.
- Geplante Veröffentlichungen benötigen einen tatsächlich laufenden nativen Gambio-Aufgabenaufruf.
- Eigene Hosting-Regeln, Themes und weitere Module können eigene Prüfungen erfordern.
- GitHub Actions prüft Paket und PHP-Syntax, ist aber kein Gambio-Integrationstest.
- Keine Gambio-Zertifizierung und kein unabhängiges Sicherheitsaudit.
