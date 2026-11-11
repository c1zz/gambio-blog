# c1zz-blog 0.47.4-rc.1

Unter Darstellung sind für „Artikel pro Seite (Liste / Grid)“ jetzt **2, 3, 4, 6, 8, 9, 10, 12, 16, 18, 20 und 24** auswählbar. Die zusätzlichen Werte gelten für Desktop, Tablet und Mobil; bestehende Einstellungen bleiben erhalten.

Das exakte Paket wurde in einem frischen **GX26.11.0 / PHP 8.2.31 / MariaDB 10.10 / Malibu** unter `/shop/` nativ installiert. Geprüft wurden Dropdowns, Speicherung, Seitennavigation und ungültige Werte. Zusätzlich wurde der bestehende lokale Migrationstestshop von 0.47.3 auf 0.47.4 aktualisiert und auf Datenerhalt geprüft. [Prüfumfang und Grenzen](https://github.com/c1zz/gambio-blog/blob/v0.47.4-rc.1/docs/KOMPATIBILITAET.md).

Bestehende Installationen können unter **Update / Aktualisieren** nach neuen Versionen suchen. Für diesen Release Candidate muss **Testversionen berücksichtigen** aktiviert sein. Der Betreiber startet das Update selbst. Die Erstinstallation erfolgt mit dem einzelnen PHP-Installer; nach erfolgreichem Abschluss wird er entfernt.

Nur das Blogmodul erhält ein neues Paket; das KI-Modul bleibt bei 0.12.1. Kein erneuter vollständiger GitHub-Updatetest oder Deinstallationslauf für diese Auswahländerung. Die Shopfunktion prüft Integrität, keine kryptografische Herkunftssignatur. [Herkunft und Integrität prüfen](https://github.com/c1zz/gambio-blog/blob/v0.47.4-rc.1/SECURITY.md); kein unabhängiges Codeaudit.
