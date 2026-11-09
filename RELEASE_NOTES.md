# c1zz-blog für Gambio · 0.42.0-rc.2

Dieser Release Candidate ergänzt die Gestaltung direkt am Blogelement und macht frühere Blogadressen verwaltbar. Modulstand und Installerdateiname lauten **0.42.0**.

- **Eigenes CSS am Element:** Visuelle Regler, Farbauswahl und CSS-Code bearbeiten dieselben Regeln mit Vorschau. Gerätebereiche, Hover und Tastaturfokus sind getrennt wählbar. Ausgabe auf den Blog begrenzt; native Gambio-CodeMirror-Integration.
- **Weiterleitungen bearbeiten oder löschen:** Beim Pfadwechsel ist die Aufbewahrung der bisherigen Adresse optional. Gespeicherte Quellen können geändert und gelöscht werden; das Ziel bleibt die aktuelle Blogadresse. Bereits zwischengespeicherte 301-Antworten können im Browser nachwirken.
- **Hilfen sichtbar machen:** Gemeinsame blaue Hinweisfelder in der Verwaltung und an Eingaben.
- **Ein Name:** c1zz-blog für Gambio in Verwaltung, Installer und beiden Modul-Centern. Technische Modulkennungen bleiben für Updates erhalten.
- **Richtige GX26-Version:** Der Paketbau erzeugt den nativen Versionsbeleg aus der Modulversion. Dadurch zeigt GX26 0.42.0 statt des Fallbacks 1.0.0.
- **Dokumentation und Bilderrundgang:** 13 aktuelle Ansichten erklären Bedienung und Einbindung.

Das Modul verwendet Gambio-eigene Anmeldung, Rechte, Formularschutz, Editor, Modul-Center, Aufgabenverwaltung und Shoplayout so weit wie möglich. Es verändert keine Kerndateien. Die geführte Deinstallation deaktiviert den Blog und erhält standardmäßig Inhalte und Medien; deren vollständige Löschung ist eine separate ausdrückliche Entscheidung.

Nur `c1zz-blog-install-0.42.0.php` hochladen. Vor dem Update Datenbank, Moduldateien und Blogmedien sichern; nicht vorher deinstallieren. Die Prüfsumme gehört zu dieser Veröffentlichung. Das Repository ist privat; GitHub unterstützt den kryptografischen Herkunftsnachweis für diesen Repository-Typ nicht. Dieser Release enthält daher kein Sigstore-Bundle. Die Repository-Sichtbarkeit bleibt unverändert.

`rc.2` korrigiert den Veröffentlichungsablauf für das private Repository. Release-Kennzeichnung, Dokumentation und Quellarchiv verwenden einheitlich **0.42.0-rc.2**. Der Installer ist bytegleich zum geprüften Paket.

Gezielt geprüft im vorhandenen GX26.11.0/PHP8.2.31/MariaDB10.10/Malibu-Shop. Der [Teststand](docs/KOMPATIBILITAET.md) trennt aktuelle Ergebnisse von früheren vollständigen Abläufen. Kein neuer vollständiger Frischinstallations-/Deinstallationsnachweis und keine pauschale Freigabe für andere Versionen oder Themes.
