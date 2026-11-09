<p align="center"><img src="docs/images/header.svg" alt="c1zz-blog für Gambio – Inhalte gestalten. Direkt im Shop." width="100%"></p>

<p align="center"><strong>Release Candidate · 0.43.0-rc.1 · MIT-Lizenz · Entwickelt von Mensch und KI</strong></p>

# Ein Blog, der zu deinem Gambio-Shop passt

Artikel schreiben, Kategorien pflegen und die Darstellung direkt im Shop gestalten: **c1zz-blog für Gambio** ist ein eigenständig installierbares Blogmodul für Gambio. Du brauchst keinen vorbereiteten Blog und keine SSH-Nacharbeiten.

**[Bilderrundgang mit 13 Ansichten](docs/BILDERRUNDGANG.md)** · **[Installer herunterladen](https://github.com/c1zz/gambio-blog/releases/download/v0.43.0-rc.1/c1zz-blog-install-0.43.0.php)** · **[Release & Prüfsummen](https://github.com/c1zz/gambio-blog/releases/tag/v0.43.0-rc.1)** · **[Installation](docs/INSTALLATION.md)** · **[Echtheit prüfen](SECURITY.md)**

> Dies ist ein **Release Candidate**. Bitte zuerst in einem Testshop prüfen und vor dem Einsatz den Shop sichern. Der interne Modulstand und der Dateiname lauten `0.43.0`; `rc.1` kennzeichnet diese Veröffentlichung.

**So sehen Besucher den Blog:** Die Desktopansicht zeigt Artikel, Kategorien und Seitennavigation im Malibu-Shoplayout – einschließlich Shopkopf und Seitenleiste.

[![Öffentliche Blogübersicht mit Shopkopf, Seitenleiste und Beispielartikeln](docs/images/blog-desktop.png)](docs/images/blog-desktop.png)

## Neu in diesem Release

Ein gemeinsamer **c1zz-systems-Stil** verbindet Blog und optionales KI-Modul: einheitliche Hinweisfelder, grüne Akzente, klare Aufklappbereiche und rote Entfernen-Aktionen. Die tatsächliche Blogversion steht neben dem Modulnamen. Eigene Tablet-/Mobilwerte sind deutlicher als Abweichungen von Desktop gekennzeichnet.

**Optional:** [c1zz-ki für Gambio](https://github.com/c1zz/gambio-ki) ergänzt Entwürfe und Themenideen direkt beim Artikel. Es hat einen eigenen Installer; der Blog funktioniert auch ohne KI-Modul.

## Was du damit machen kannst

| Inhalte | Darstellung | Betrieb |
|---|---|---|
| Artikel, Entwürfe und Vorschau | Liste, Grid, Slider und Magazin | Geführte Installation und Updates |
| Eigene Kategorien und Schlagwörter | Desktop, Tablet und Mobil getrennt | Versionen und Veröffentlichungstermine |
| Native visuelle Bearbeitung und HTML | Grafischer Editor mit Vorschau | Export und Import mit Bildern |
| Medienverwaltung und Beispielblog | Farben, Schriften, Karten und Navigation | SEO-Felder, Canonical und Sitemap |
| Übersicht und einzelne Artikelseiten | Konfigurierbare Shop-Seitenleiste | Daten behalten oder ausdrücklich löschen |

Du kannst Blogkarten auch über **`[c1zz_blog]`** in unterstützte CMS-Inhalte und Produktbeschreibungen einbinden. Der Bereich **Einbinden** erzeugt den passenden Shortcode mit eigenen Widgetoptionen.

## In Gambio integriert und gezielt deinstallierbar

**Das Modul nutzt Gambio-eigene Funktionen so weit wie möglich und fügt sich in die vorhandene Shopstruktur ein.** Dazu gehören die native Admin-Anmeldung und Zugriffskontrolle, der Formularschutz, der Gambio-Editor, das Modul-Center und die Aufgabenverwaltung. Öffentliche Blogseiten werden über Gambios Shoplayout ausgegeben; Domain und Shop-Unterverzeichnis stammen aus der Shopkonfiguration. Installation und Deinstallation verwenden die nativen Modul- und Cacheabläufe.

Der Modulcode liegt getrennt unter `GXModules/c1zz/StandaloneBlog/`. **Gambio-Kerndateien und fremde Module werden nicht verändert.** Blogartikel und Metadaten liegen in eigenen Tabellen, Bilder in einem eigenen Medienverzeichnis.

**Der geführte Deinstallationsablauf nimmt den Blog wieder aus dem Betrieb:** Öffentliche Darstellung, Verwaltung und Zeitplanung werden deaktiviert. Standardmäßig bleiben Inhalte und Medien für eine Wiederinstallation erhalten. Ihre vollständige Löschung erfordert eine zusätzliche ausdrückliche Bestätigung. Die Moduldateien bleiben auch dann vorhanden. Selbst gesetzte Bloglinks und eingefügte Shortcodes in Shopinhalten solltest du anschließend entfernen. Einzelheiten stehen unter [Deinstallation](docs/INSTALLATION.md#deinstallation).

## So arbeitest du mit dem Blog

**Artikel im Überblick:** Suche und Kategoriefilter helfen beim Finden. Die Statusspalte unterscheidet veröffentlichte Artikel und private Entwürfe; Bearbeitung, Freigabe und Termine sind direkt erreichbar.

[![Artikelverwaltung mit zehn Beispielartikeln, Kategorien, Status und Aktionen](docs/images/artikelverwaltung.png)](docs/images/artikelverwaltung.png)

**Inhalte schreiben:** Der native Gambio-Editor bietet Formatierung, Bilder und HTML-Ansicht. Darunter liegen **Entwurf speichern**, **Vorschau** und der Zugang zu **Veröffentlichung, Terminen und Versionen**. Der Ausschnitt zeigt den Inhaltsbereich; Titel, Kategorie und SEO stehen weiter oben im Formular.

[![Inhaltsbereich des nativen Gambio-Editors mit Formatierung und Entwurfsaktionen](docs/images/editor.png)](docs/images/editor.png)

**[Zum vollständigen Bilderrundgang →](docs/BILDERRUNDGANG.md)** Dort siehst du auch Einstieg, Kategorien, Artikeldaten und SEO, Freigabe und Termine, die öffentliche Artikelseite und die mobile Ansicht. Alle Bilder lassen sich in Originalgröße öffnen.

## In wenigen Schritten loslegen

1. Den PHP-Installer und `SHA256SUMS` aus demselben [Release](https://github.com/c1zz/gambio-blog/releases/tag/v0.43.0-rc.1) herunterladen und **vor der Ausführung prüfen**.
2. Nur `c1zz-blog-install-0.43.0.php` in den Shopordner neben `shop.php` und `admin/` hochladen. Dateinamen beibehalten.
3. Die Datei im Browser öffnen. Falls nötig, **Admin-Anmeldung öffnen** wählen. Gambio verarbeitet die Anmeldung in seinem eigenen Fenster; danach kehrt der Installer automatisch zurück.
4. Voraussetzungen und Paketprüfung kontrollieren, bei vorhandenen Daten die Sicherung bestätigen und die Einrichtung ausdrücklich starten.
5. Nach erfolgreichem Abschluss entfernt sich die hochgeladene Installationsdatei selbst. In der Blogverwaltung hilft **Einstieg** beim Anpassen an deinen Shop.

Das ZIP ist bereits in der PHP-Datei enthalten. Du musst kein zweites Archiv hochladen. Eine Neuinstallation startet leer; **Beispielartikel, Kategorien und Illustrationen kannst du danach bewusst hinzufügen**.

Die vollständigen Schritte, Voraussetzungen und Hinweise zu Updates stehen in der [Installationsanleitung](docs/INSTALLATION.md).

## Gestaltung und eigenes CSS am Element

Die grafische Darstellung und **Alle Einstellungen** bearbeiten dieselben Werte. Unter **Eigenes CSS** am ausgewählten Elementtyp bearbeiten visuelle Regler, Farbauswahl und CSS-Code dieselben Regeln. Geräteansicht, Hover und Tastaturfokus lassen sich getrennt gestalten; erst **Darstellung speichern** übernimmt die Änderungen. Du kannst etwa auf Desktop ein Grid und auf Mobil einen Slider verwenden, Bildplatzierung und Textabstände einstellen oder Farben und Schriftgrößen je Gerät anpassen.

**Vorschau und Einstellungen nebeneinander:** Hier ist im grafischen Editor eine **ungespeicherte Grid-Vorschau** geöffnet. Gerätewahl, Spaltenzahl und Artikelzahl sind direkt neben der Vorschau sichtbar. Die öffentliche Desktopaufnahme weiter oben zeigt die gespeicherte Gridansicht.

[![Grafischer Darstellungseditor mit Grid-Vorschau, Gerätewahl und Layoutoptionen](docs/images/darstellung.png)](docs/images/darstellung.png)

[![Eigenes CSS an Artikelkarten mit Regler, Farbauswahl und unmittelbarer Vorschau](docs/images/element-css.png)](docs/images/element-css.png)

**Blogadressen bleiben steuerbar:** Beim Pfadwechsel entscheidest du, ob die bisherige Adresse weiterleiten soll. Gespeicherte Weiterleitungen kannst du unter **Blogadresse** ändern oder löschen. Hilfetexte sind im gemeinsamen c1zz-systems-Stil hervorgehoben. Entfernen, Löschen und Zurücksetzen eigener Werte sind rot markiert.

Die Screenshots stammen aus dem lokalen GX26-Testshop mit Malibu und den optionalen Beispielinhalten (Modul 0.43.0, Aufnahme vom 09.11.2026). Der [Bilderrundgang](docs/BILDERRUNDGANG.md) zeigt auch den **mobilen Slider**. Das Aussehen hängt von deinem Theme und deinen Einstellungen ab.

## Was ist tatsächlich geprüft?

Der aktuelle Kandidat wurde lokal mit **Gambio 26.11.0, PHP 8.2.31, MariaDB 10.10 und Malibu** geprüft. Der neue Stand vereinheitlicht die Verwaltung, ergänzt die sichtbare Modulversion und macht vererbte Gerätewerte eindeutiger. Die aktuelle Frischinstallation und der Datenerhalt bei De-/Wiederinstallation werden im verlinkten Teststand dokumentiert. Die Anmelderückkehr in Firefox und Chromium wurde bereits mit 0.40.2 geprüft. Die GX4-Grundlage wurde zuvor mit **4.8.0.3 und 4.9.6.1** geprüft; das ersetzt keine erneute vollständige Abnahme des aktuellen Kandidaten auf diesen Versionen.

Die genaue Einordnung und offene Prüfungen stehen in [Kompatibilität & Teststand](docs/KOMPATIBILITAET.md). Es gibt keine pauschale Zusage für jedes Gambio-Release, jede PHP-Version oder jedes Theme.

## Herkunft und Sicherheit

- **SHA-256** erkennt Änderungen gegenüber dem veröffentlichten Vergleichswert.
- **Dieser Kandidat liegt in einem privaten Repository.** GitHub unterstützt hier keine Artifact Attestations; dieser Release enthält deshalb keinen kryptografischen Herkunftsnachweis. Prüfsummen sind kein Ersatz dafür. Bei öffentlichen Releases bleibt die Attestierung im Workflow verpflichtend.
- Das mitgelieferte Python-Werkzeug prüft und entpackt das eingebettete Paket **ohne PHP auszuführen**. So lässt sich auch der enthaltene Modulcode ansehen.
- Die Veröffentlichung enthält keine lokale Git-Historie, Shopsoftware, Datenbanksicherungen, Zugangsdaten oder Kundenbestände.

```bash
sha256sum --check SHA256SUMS
```

Was diese Prüfungen aussagen – und was sie nicht nachweisen – erläutert [SECURITY.md](SECURITY.md).

## Von Mensch und KI entwickelt

**Dieses Modul ist gemeinsam durch c1zz und KI-Unterstützung entstanden.** Anforderungen, Produktentscheidungen, Rückmeldungen und praktische Shoptests kamen von c1zz; KI unterstützte bei Implementierung, Fehlersuche, Tests und Dokumentation. Die Entwicklung war ein iterativer Prozess zwischen Mensch und KI.

Das wird bewusst offengelegt. KI-Unterstützung ersetzt weder nachvollziehbare Tests noch ein unabhängiges Sicherheitsreview. Dieses Projekt ist **kein offizielles Gambio-Produkt** und beansprucht keine Gambio-Zertifizierung.

## Feedback und Lizenz

Fehler und Verbesserungsvorschläge sind in den [Issues](https://github.com/c1zz/gambio-blog/issues) willkommen. Bitte Gambio-, PHP- und Theme-Version sowie die Schritte zum Reproduzieren angeben. Sicherheitslücken bitte [privat melden](SECURITY.md#sicherheitslücke-melden).

**MIT-Lizenz:** Nutzung, Anpassung und Weiterverteilung sind auch kommerziell erlaubt; den Lizenzhinweis bei Weitergabe beibehalten. [Vollständiger Lizenztext](LICENSE).
