# c1zz-blog 0.48.15-rc.1

Die Bloggestaltung ist jetzt für Desktop, Tablet und Mobil genauer einstellbar. Die Suchlupe öffnet ein Overlay, ohne Überschrift und Artikel zu verschieben.

- **Gesamter Blog:** Prozentuale Breite und optionale Maximalbreite unter Layout steuern Überschrift, Kategorien, Suche, Liste, Grid, Slider, Magazin und Artikelseiten. 100 % und „Keine maximale Breite“ nutzen den verfügbaren Shop-Inhaltsbereich. Eingebundene Widgets behalten ihre eigene Breite.
- **Artikel:** Position und Ausrichtung des Artikelbilds sowie Textbreite je Gerät wählen. „Volle Breite (ohne Textbegrenzung)“ hebt die Textbegrenzung auf. Eigene Artikelfarben und Schrift für die Artikelüberschrift sind verfügbar.
- **Kategorien und Suche:** Kategorien vor oder nach der Überschrift; Suchlupe am Anfang oder Ende direkt in der Kategorienreihe, neben oder über der Überschrift beziehungsweise unter den Kategorien. Mobil bleibt die Lupe neben der Kategorienauswahl erreichbar. Ohne JavaScript bleibt ein GET-Suchformular nutzbar.
- **Suchgestaltung:** Eigene Farben, Schrift und begrenztes CSS für Suchfeld, Overlay und Ergebnisse; Vorschau für Blogkopf, Overlay und Treffer.
- **Admin:** c1zz-systems-Logo sowie einheitliche Dropdowns und Eingabefelder in Blog und KI. Der Widget-Generator zeigt nur Einstellungen an, die in Blogkarten wirken.

Bestehende Artikel, Bilder, Einstellungen und KI-Daten bleiben erhalten. Der aktuelle Prüfstand gilt für **Gambio 26.11.0 / PHP 8.2.31 / MariaDB 10.10 / Malibu**. Frische Installation, Speichern und Wiederladen der neuen Werte, normale Wiederinstallation, Updates mit Datenerhalt, isolierte Verhaltenstests und Browserprüfungen sind dokumentiert. [Prüfumfang und Grenzen](docs/KOMPATIBILITAET.md).

Zum Aktualisieren zuerst sichern, dann **Update / Aktualisieren → Testversionen berücksichtigen → Nach Updates suchen**. Bei beiden Modulen zuerst den Blog aktualisieren. Updates werden ausdrücklich vom Betreiber gestartet. Die Shopfunktion prüft Paketintegrität, noch keine kryptografische Herkunftssignatur. Der separate Herkunftsnachweis des Downloads ist über [SECURITY.md](SECURITY.md) prüfbar; er ersetzt kein unabhängiges Codeaudit.

Abschlussprüfung: 22 native Prüfungen nach frischer Installation beider exakten Pakete, 48 Prüfungen beim abschließenden Blogupdate und 79 isolierte Chromiumtests für Editor/DOM bestanden; weitere gezielte Darstellungsprüfungen siehe Testbericht.
