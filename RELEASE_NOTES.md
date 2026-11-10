# c1zz-blog 0.47.1-rc.1

Die Blogübersicht sortiert jetzt standardmäßig nach **Artikeldatum, neueste zuerst**. Bisher entschied der technische Veröffentlichungszeitpunkt; bei gemeinsam importierten Artikeln führte das zu einer unerwarteten Reihenfolge.

Unter **Darstellung → Reihenfolge der Artikel** stehen drei Einstellungen zur Wahl:

- Artikeldatum: neueste zuerst (neuer Standard, auch beim Update)
- Artikeldatum: älteste zuerst
- Zuletzt veröffentlicht zuerst (bisheriges Verhalten)

Übersicht, Kategorien, Einbindungen, responsive Seiten und Vor-/Zurück-Navigation verwenden die gleiche Reihenfolge. Bei gleichem Artikeldatum entscheidet eine stabile interne ID. Nur veröffentlichte Fassungen werden berücksichtigt; private Entwürfe ändern die öffentliche Reihenfolge nicht. Artikel, Bilder, Kategorien und Fassungen bleiben erhalten. Keine Datenbankschemaänderung. Die KI-Erweiterung bleibt unverändert auf 0.12.0.

## Im Testshop aktualisieren

**Update / Aktualisieren → Auch Testversionen anzeigen → Nach Updates suchen.** Nach einer Sicherung **Jetzt aktualisieren** wählen. Kein erneuter Root-Upload nötig. Nach dem Update findest du die Auswahl direkt oben unter **Darstellung**.

Das exakte Paket wurde im bestehenden GX26.11.0-Migrationstestshop unter `/shop/` von 0.47.0 auf 0.47.1 aktualisiert und mit 78 Artikeln geprüft. Geprüft wurden alle drei Sortierungen über die gesamte öffentliche Seitennavigation, Kategorien, Nachbarartikel, Speichern und Formularschutz sowie der Datenerhalt. Isolierte PHP-Regressionsprüfungen und Builderprüfungen bestanden. [Genauer Teststand und Grenzen](docs/KOMPATIBILITAET.md).

Dies bleibt ein Release Candidate. Kein neuer vollständiger Shop-Neuaufbau, kein unabhängiges Codeaudit und keine zusätzliche Versions-/Theme-Freigabe. Der Shop prüft Paketintegrität; eine kryptografische Herkunftssignatur wird dort weiterhin nicht verifiziert.
