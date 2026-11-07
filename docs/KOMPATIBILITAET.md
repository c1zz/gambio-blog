# Kompatibilität und Teststand

**Veröffentlichung:** `v0.40.2-rc.1` · **Modulstand:** `0.40.2` · **Stand:** 7. November 2026.

| Umgebung | Tatsächlicher Nachweis |
|---|---|
| Gambio 26.11.0, PHP 8.2.31, MariaDB 10.10, Malibu | Aktueller lokaler Testfall. Installer und Anmelderückkehr in Firefox und Chromium, native Rechte-/Statusprüfungen und Paketvorbereitung geprüft. Die lokale Screenshot-Umgebung enthält eine aktive Installation mit Beispielartikeln. |
| Gambio 4.8.0.3, Malibu | Frühere native Integrations- und Bedienprüfungen der GX4-Grundlage. Keine vollständige erneute Kandidatenabnahme behauptet. |
| Gambio 4.9.6.1, Malibu | Frühere native Installation und Bedienung durch den Betreiber bestätigt. Keine vollständige erneute Kandidatenabnahme behauptet. |
| Andere GX26-Releases, GX5, Honeygrid oder andere Themes | Für diesen Kandidaten keine allgemeine Freigabe aus den genannten Ergebnissen ableiten. |

Der aktuelle Anmelde-Fix wurde mit 32 isolierten Ziel-/Unterverzeichnis-/GET-Intentprüfungen, 39 Archivprüfungen, reproduzierbaren Buildertests und PHP-Syntaxkontrollen geprüft. Hinzu kommen 13 native HTTP-Prüfungen, 14 Chromium-Prüfungen für beide Installer-Einstiege und sechs Firefox-Prüfungen für den vollständigen Root-Einstieg. Das sind gezielte Prüfungen, keine Aussage über lückenlose Testabdeckung.

Installation, Update, Deinstallation und Wiederinstallation mit Datenerhalt wurden in der vorherigen 0.40.0-Routine nativ und im Browser geprüft. Der letzte Fix ändert die Rückkehr nach der nativen Anmeldung; er löst selbst keine Installation aus.

Die öffentliche Auslieferung wird zusätzlich in GitHub Actions statisch geprüft: vollständiger Installer-Hash, eingebettete Paketdateien, Pfade, Größen, Prüfsummen und PHP-Syntax. Diese CI ist kein Gambio-Integrationstest; Gambio selbst wird nicht mit ausgeliefert.

## Grenzen

- Die PHP-Version muss zum konkreten Gambio-Release passen. Für GX26 wurde PHP 8.2.31 verwendet; andere Kombinationen werden nicht pauschal zugesagt.
- Shop-Unterverzeichnisse wie `/shop/` und `/neueroeffnung/` sind im Code und in isolierten Prüfungen berücksichtigt. Der aktuelle Login-Ablauf ist nativ im Shop-Root geprüft; keine neue vollständige Unterverzeichnis-Abnahme behauptet.
- Für geplante Veröffentlichungen muss der native regelmäßige Gambio-Aufruf tatsächlich funktionieren.
- Individuelle Themes, Hosting-Regeln und zusätzliche Module können eigene Prüfungen erfordern.
- Es gibt keine offizielle Gambio-Zertifizierung und kein unabhängiges Sicherheitsaudit.
