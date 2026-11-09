# Installation, Update und Deinstallation

## Einbindung in die vorhandene Shopstruktur

Das Blogmodul verwendet Gambio-eigene Funktionen so weit wie möglich: Admin-Anmeldung, native Rechte- und Formularprüfungen, Editor, Modul-Center und Aufgabenverwaltung. Die öffentlichen Seiten laufen im Gambio-Shoplayout; Domain und Shop-Unterverzeichnis werden aus der Shopkonfiguration abgeleitet. Der geführte Installations- und Deinstallationsablauf nutzt Gambios Modulverwaltung und die erforderlichen nativen Cacheabläufe.

Der eigene Modulcode liegt unter `GXModules/c1zz/StandaloneBlog/`, Blogbilder unter `images/c1zz-blog/`. Artikel und Metadaten liegen in eigenen Modultabellen. Gambio-Kerndateien und fremde Module werden nicht verändert; die Shop-`.htaccess` wird nicht angepasst.

## Voraussetzungen

- Ein eingerichteter Gambio-Shop mit funktionierendem Theme und Rewrite-Regeln.
- Native Admin-Anmeldung und Schreibrechte im Modul-Center.
- Eine zum konkreten Gambio-Release passende PHP-Version. Der aktuelle GX26-Test erfolgte mit PHP 8.2.31.
- PHP-Erweiterungen ZIP, mysqli und DOM; für Bildverarbeitung GD mit JPEG-/PNG-Unterstützung. WebP benötigt den entsprechenden Decoder.
- Passende Schreibrechte für den eigenen Modulpfad, erforderliche Caches, das eigene Medienverzeichnis und den Shopordner zur späteren Installer-Entfernung.
- Ein beschreibbares temporäres Verzeichnis außerhalb des öffentlich erreichbaren Shop-/Document-Roots.

Nicht pauschal Verzeichnisse auf `777` setzen. Der Installer prüft Voraussetzungen und meldet betroffene Pfade.

## Datei prüfen und hochladen

1. Aus dem [Release](https://github.com/c1zz/gambio-blog/releases/tag/v0.42.0-rc.2) den PHP-Installer und `SHA256SUMS` herunterladen. Das automatisch von GitHub angebotene **Source code**-Archiv ist für die Installation nicht nötig.
2. Vor dem Hochladen die [Prüfsumme prüfen](../SECURITY.md). Für diesen privaten Kandidaten ist kein kryptografischer Herkunftsnachweis verfügbar.
3. Nur `c1zz-blog-install-0.42.0.php` in den Shopordner hochladen, in dem auch `shop.php` und `admin/` liegen. Bei einem Shop unter `/shop/` ist dessen Unterordner gemeint.
4. Im Browser `https://dein-shop.example/c1zz-blog-install-0.42.0.php` öffnen; ein Shop-Unterverzeichnis entsprechend voranstellen. Den Versionsdateinamen beibehalten.

Das enthaltene ZIP wird vor der Übernahme geprüft und nur vorübergehend privat geöffnet. Es soll kein separates Blog-ZIP im öffentlichen Shopordner liegen.

## Anmeldung und Einrichtung

Ohne passende Adminsitzung erscheint **Als Admin anmelden**. **Admin-Anmeldung öffnen** öffnet Gambios `login_admin.php` in einem eigenen Fenster. Zugangsdaten werden ausschließlich dort eingegeben. Sobald dieselbe Browsersitzung als Admin mit Modul-Schreibrechten erkannt wird, schließt das Anmeldefenster und der Installer setzt automatisch fort.

Bereits angemeldete Admins gelangen direkt zur Prüfung. Ohne JavaScript oder bei blockierten Anmeldefenstern den nativen Anmeldelink in einem neuen Tab öffnen und danach im Installer **Anmeldung abgeschlossen – weiter** wählen.

Bei einer Neuinstallation den freien Blogpfad wählen, beispielsweise `blog` oder `magazin`. Die Einrichtung beginnt erst nach der ausdrücklichen Startbestätigung. Die fünf Schritte laufen automatisch in einer festen Fortschrittsanzeige; Fehler stoppen den Ablauf. Ursache beheben und **Erneut versuchen** wählen. Erfolgreiche Schritte sind wiederholungssicher.

Nach erfolgreicher Abschlussprüfung entfernt sich die hochgeladene Installerdatei. Für ein Update wird später der neue Installer erneut hochgeladen.

## Den Blog an deinen Shop anpassen

Der sichtbare Modulname lautet **c1zz-blog für Gambio**, auch im GX26-Modul-Center. Die dort angezeigte Version stammt aus dem installierten Paket.

In der Blogverwaltung führt **Einstieg** durch die ersten Schritte:

1. Optional den Beispielblog mit drei Kategorien, neun öffentlichen Artikeln, einem privaten Entwurf und drei Illustrationen hinzufügen.
2. Unter **Darstellung** Layout, Karten, Bilder, Navigation, Schriften, Farben und Seitenleiste einstellen. Desktop, Tablet und Mobil haben getrennte Möglichkeiten.
3. Eigene Kategorien und Artikel anlegen. Entwürfe und öffentlicher Stand bleiben getrennt.
4. SEO-Felder und Blogadresse prüfen und erst nach der Kontrolle veröffentlichen.

Unveränderte Beispielartikel lassen sich gesammelt in den Papierkorb verschieben. Bearbeitete oder eigene Inhalte werden davon nicht pauschal entfernt.

## Eigenes CSS am Element

Unter **Darstellung → Visuell** ein Blogelement wählen und **Eigenes CSS** öffnen. Eigenschaften, Regler, Farbauswahl und CSS-Code bearbeiten dieselben Deklarationen mit Vorschau. Eine Regel gilt für alle Blogelemente dieses Typs, beispielsweise alle Artikelkarten. Gerätebereiche und Normal-/Hover-/Fokuszustand sind getrennt wählbar. Deaktivieren behält den Code; Zurücksetzen ist rückgängig zu machen. Erst das Speichern der Darstellung verändert die öffentliche Ausgabe.

Der Codeeditor nutzt die vorhandenen Gambio-CodeMirror-Dateien; ohne sie bleibt die Codeeingabe verfügbar. Erlaubt sind CSS-Deklarationen innerhalb der vorgegebenen Blogelemente. Eigene Selektoren, `@`-Regeln, externe URLs und CSS-Variablen werden nicht übernommen. Die Begrenzung auf den Blog schützt die umgebende Shopdarstellung.

## Blogadresse und Einbinden

Unter **Blogadresse** lässt sich der URL-Pfad ändern. Beim Pfadwechsel legt die Checkbox **Bisherige Blogadresse als Weiterleitung behalten** fest, ob die alte Adresse erhalten bleibt. Gespeicherte Weiterleitungen lassen sich hier einzeln ändern oder löschen. Bearbeitet wird die frühere Adresse; Ziel ist stets der aktuelle Blogpfad, einschließlich Artikel-, Kategorie- und Seitenpfaden. Bereits im Browser gespeicherte 301-Weiterleitungen können nach dem Löschen noch wirken; bei der Kontrolle ein frisches Browserprofil verwenden. Hosting- oder Coming-soon-Regeln werden nicht automatisch verändert.

Unter **Einbinden** erzeugt der Generator `[c1zz_blog]` für unterstützte CMS-Seiten und Produktbeschreibungen. Widgets besitzen eigene begrenzte Darstellungsoptionen. Nur öffentliche Artikel werden ausgegeben; private Entwürfe bleiben privat.

## Veröffentlichungen planen

Die Aufgabe erscheint in Gambios Aufgabenverwaltung. Ein aktiver Eintrag allein richtet keinen Server-Cronjob ein: Der regelmäßige native Gambio-Aufruf muss beim Hosting tatsächlich laufen. Fremde Cronjobs werden nicht verändert.

## Updates

Vorher Datenbank, vorhandenen Modulcode und Blogmedien zusammen sichern. Ein Blogexport ist eine zusätzliche portable Sicherung und ersetzt keine vollständige Shopsicherung.

Den neuen versionierten Installer hochladen, öffnen, Sicherung bestätigen und die geprüfte Aktualisierung starten. Nicht vorher deinstallieren. Inhalte und Medien bleiben erhalten. Unbekannte oder veränderte alte Installer-/Paketdateien können den Start blockieren; sie werden nicht blind entfernt.

## Deinstallation

**Deinstallation starten** öffnet den geführten Ablauf. Ohne zusätzlichen Löschhaken werden Darstellung, Verwaltung und Zeitplanung deaktiviert; Artikel, Entwürfe, Versionen, Kategorien, Einstellungen und Medien bleiben für eine Wiederinstallation erhalten.

Die rote, zunächst ausgeschaltete Checkbox zur vollständigen Datenlöschung ist eine getrennte ausdrückliche Entscheidung. Mit ihr werden die eigenen Blogdaten und Bilder unwiderruflich entfernt. Datenbankstruktur- und Dateiänderungen sind nicht vollständig transaktional; deshalb vorher sichern. Der Modulcode bleibt für eine erneute Installation vorhanden.

Nach der Deinstallation werden die öffentlichen Blogseiten auch bei erhaltenen Daten nicht mehr angezeigt. Selbst gesetzte Bloglinks in der Shopnavigation sowie eingefügte `[c1zz_blog]`-Shortcodes in CMS-Inhalten oder Produktbeschreibungen solltest du anschließend entfernen. Diese eigenen redaktionellen Einbindungen werden nicht automatisch aus Shopinhalten gelöscht. Bei einer Wiederinstallation vorhandene Veröffentlichungstermine bewusst neu planen.

## Unterstützung

Bei Problemen Gambio-, PHP- und Theme-Version sowie den betroffenen Schritt angeben. Keine Zugangsdaten, Sitzungstokens, Datenbankexporte oder privaten Entwürfe in öffentliche Issues einfügen.
