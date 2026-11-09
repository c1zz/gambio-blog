# Kompatibilität und Teststand

**Veröffentlichung:** `v0.42.0-rc.1` · **Modulstand:** `0.42.0` · **Stand:** 9. November 2026.

| Umgebung | Tatsächlicher Nachweis |
|---|---|
| Gambio 26.11.0, PHP 8.2.31, MariaDB 10.10, Malibu | Aktueller lokaler Testfall. Installer und Anmelderückkehr in Firefox und Chromium, native Rechte-/Statusprüfungen und Paketvorbereitung geprüft. Die lokale Screenshot-Umgebung enthält eine aktive Installation mit Beispielartikeln. |
| Gambio 4.8.0.3, Malibu | Frühere native Integrations- und Bedienprüfungen der GX4-Grundlage. Keine vollständige erneute Kandidatenabnahme behauptet. |
| Gambio 4.9.6.1, Malibu | Frühere native Installation und Bedienung durch den Betreiber bestätigt. Keine vollständige erneute Kandidatenabnahme behauptet. |
| Andere GX26-Releases, GX5, Honeygrid oder andere Themes | Für diesen Kandidaten keine allgemeine Freigabe aus den genannten Ergebnissen ableiten. |

Für 0.42.0 bestanden: zwei reproduzierbare Buildertests, 26 Paketintegritäts-, 39 Archiv-, 32 Login- und 82 Element-CSS-Prüfungen. Im vorhandenen GX26-Shop bestanden 19 native Prüfungen zur Adressverwaltung, 12 Chromium-Prüfungen für Weiterleitungen, CSRF, Hilfetexte, Namen und Versionsanzeige sowie erneut 26 Chromium-Prüfungen für Element-CSS einschließlich öffentlicher Ausgabe ohne JavaScript und Wiederherstellung der ursprünglichen Einstellungen.

Das Update von 0.41.0 wurde über den tatsächlichen Root-Installer mit fünf nativen Schritten und Selbstentfernung geprüft (drei Browserprüfungen). Anschließend wurden ausschließlich der native Versionsbeleg und sein Paketmanifest ergänzt. Die installierten Moduldateien stimmen mit dem endgültigen Auslieferungspaket überein. Alle 152 Dateien des finalen Installers wurden zusätzlich in ein leeres temporäres Modulziel übernommen, erneut übernommen und per Hash geprüft; 81 PHP-Syntaxprüfungen bestanden. Artikel, Entwürfe, Versionen, Kategorien und Medien blieben gegenüber der Sicherung unverändert. Die Versionsanzeige wurde danach im echten GX26-Modul-Center geprüft.

Historischer Nachweis: 0.40.2 bestand zusätzlich 13 native HTTP-, 14 Chromium- und sechs Firefox-Prüfungen für die Anmeldung. Installation, Update, Deinstallation und Wiederinstallation mit Datenerhalt wurden mit der vorherigen 0.40.0-Routine nativ und im Browser geprüft. Für 0.42.0 wurde keine neue vollständige Frischinstallations- oder Deinstallationsabnahme durchgeführt.

Die öffentliche Auslieferung wird zusätzlich in GitHub Actions statisch geprüft: vollständiger Installer-Hash, eingebettete Paketdateien, Pfade, Größen, Prüfsummen und PHP-Syntax. Diese CI ist kein Gambio-Integrationstest; Gambio selbst wird nicht mit ausgeliefert.

## Grenzen

- Die PHP-Version muss zum konkreten Gambio-Release passen. Für GX26 wurde PHP 8.2.31 verwendet; andere Kombinationen werden nicht pauschal zugesagt.
- Shop-Unterverzeichnisse wie `/shop/` und `/neueroeffnung/` sind im Code und in isolierten Prüfungen berücksichtigt. Der aktuelle Login-Ablauf ist nativ im Shop-Root geprüft; keine neue vollständige Unterverzeichnis-Abnahme behauptet.
- Für geplante Veröffentlichungen muss der native regelmäßige Gambio-Aufruf tatsächlich funktionieren.
- Individuelle Themes, Hosting-Regeln und zusätzliche Module können eigene Prüfungen erfordern.
- Es gibt keine offizielle Gambio-Zertifizierung und kein unabhängiges Sicherheitsaudit.
