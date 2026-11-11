# c1zz-blog 0.48.4-rc.1

**Kategorien, Bilderverwaltung, gespeicherte Fassungen und Importvorschau verwenden jetzt denselben c1zz-Stil wie die Artikelliste.** Helle grüne Kopfzeilen, feine Linien und einheitliche Abstände ersetzen die verbliebenen nativen Tabellenstile. Kategorien bearbeiten und Fassungen ansehen erhalten passende Buttons; die Versionsnavigation erhält beschriftete Schaltflächen. Breite Listen bleiben auf schmalen Adminansichten horizontal scrollbar.

Die Regeln gelten gezielt für die Modultabellen. Artikeldaten und öffentliche Blogdarstellung werden dadurch nicht geändert. Das KI-Modul erhält mit **0.12.3** den synchronisierten gemeinsamen Admin-Stil.

Geprüft auf **GX26.11.0 / PHP 8.2.31 / MariaDB 10.10 / Malibu**: 15 fokussierte native Prüfungen nach frischer Installation, 35 Update-/Datenerhaltprüfungen und 34 Browserprüfungen nach dem Update des lokalen Migrationstestshops. Zuvor 32 Browserprüfungen der Tabellenfragmente, fünf Smarty-Kompilierungen; zusätzlich zwei Buildertests und Installer-Syntaxprüfung. [Prüfumfang und Grenzen](docs/KOMPATIBILITAET.md).

Unter **Update / Aktualisieren → Testversionen berücksichtigen → Nach Updates suchen** das Update nach einer Sicherung selbst starten. Kein erneuter vollständiger GitHub-Update- oder Deinstallationslauf. Die Shopfunktion prüft Paketintegrität, keine kryptografische Herkunftssignatur. [Herkunft und Integrität](SECURITY.md); kein unabhängiges Codeaudit.
