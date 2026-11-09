# Sicherheit und Echtheit prüfen

## Vor der Ausführung prüfen

Ein PHP-Installer ist ausführbarer Servercode. Die Prüfung muss **vor seinem ersten Aufruf** mit einem unabhängigen Werkzeug erfolgen. Eine manipulierte Datei könnte ihre eigene Selbstprüfung verändern.

Der kanonische Veröffentlichungsort ist **https://github.com/c1zz/gambio-blog**. Dateiname und Versionsnummer allein beweisen keine Herkunft.

### 1. Prüfsumme

Installer und `SHA256SUMS` aus demselben Release herunterladen:

```bash
sha256sum --check SHA256SUMS
```

Unter macOS: `shasum -a 256 -c SHA256SUMS`. Unter PowerShell: `Get-FileHash .\c1zz-blog-install-0.42.0.php -Algorithm SHA256` und den Wert mit `SHA256SUMS` vergleichen.

Die Prüfsumme erkennt eine Veränderung gegenüber dem Vergleichswert. Werden Datei und Prüfsumme gemeinsam ausgetauscht, reicht sie als Herkunftsnachweis nicht aus.

### 2. Kryptografischer Herkunftsnachweis

Der Release-Workflow attestiert die **gesamte unveränderte PHP-Datei**, einschließlich eingebettetem Archiv. Die Signatur verwendet die kurzlebige GitHub-Actions-/Sigstore-Identität; es liegt kein privater Signaturschlüssel im Repository.

Mit der GitHub CLI:

```bash
gh attestation verify c1zz-blog-install-0.42.0.php --repo c1zz/gambio-blog
```

Der erwartete Workflow ist `c1zz/gambio-blog/.github/workflows/release.yml`. Der Nachweis gehört zum jeweiligen Release-Tag. Als zusätzliches Release-Asset wird die Sigstore-Bundle-Datei veröffentlicht; zur [Offline-Verifikation](https://docs.github.com/en/actions/how-tos/secure-your-work/use-artifact-attestations/verify-attestations-offline) gehören auch die passenden Vertrauensdaten.

Dieser Nachweis bestätigt die Zuordnung der Datei zum GitHub-Release-Workflow. **Er ist kein unabhängiges Codeaudit, keine Identitätsprüfung einer natürlichen Person und keine Garantie für Fehlerfreiheit.** Der Workflow prüft einen bereitgestellten Installer; er behauptet keinen unabhängigen Neuaufbau aus einem separaten öffentlichen Entwicklungsrepository.

### 3. Archiv ansehen, ohne PHP auszuführen

Das ZIP liegt Base64-kodiert im Installer. Das ist ein Transportformat und keine Verschlüsselung. Der enthaltene eigene Modulcode ist damit einsehbar.

```bash
python3 tools/verify_release.py
python3 tools/verify_release.py --extract ./pruefung
```

Das Werkzeug führt kein PHP aus. Es prüft die vollständige Dateiprüfsumme, die Paketversion, das eingebettete ZIP, alle Dateiprüfsummen, Größen, Pfade und Symlink-Merkmale. Das Ausgabeziel muss neu sein. Diese lokale Prüfung ist von der kryptografischen Herkunftsprüfung zu unterscheiden.

## Schutzmaßnahmen im Installer

Native Admin-Anmeldung und Modul-Center-Schreibrechte, CSRF- und sitzungsgebundene Tokens schützen Änderungen. Anmeldestatus-Aufrufe sind nur lesend und reichen allein nicht zum Installieren. Paketpfade und Dateigrößen sind begrenzt; Symlinks und fremde Zielpfade werden abgelehnt. Der Installer tauscht nur den eigenen Modulordner aus und entfernt sich nach erfolgreicher Abschlussprüfung.

Die veröffentlichten Schutzmaßnahmen wurden gezielt getestet. Ein externer Penetrationstest oder eine unabhängige Sicherheitszertifizierung liegt nicht vor. Das Modul entstand mit KI-Unterstützung; diese Herkunft wird in der README offengelegt.

## Sicherheitslücke melden

Bitte unter **Security → Report a vulnerability** in diesem Repository privat melden: https://github.com/c1zz/gambio-blog/security/advisories/new

Reproduktionsschritte, betroffene Version und Auswirkung reichen zunächst aus. Keine produktiven Passwörter, Sitzungscookies oder Kundendaten übermitteln. Sicherheitsmeldungen gehören nicht in öffentliche Issues.

Für den Release Candidate besteht keine feste Reaktionszeit- oder Supportzusage. Neue Sicherheitsinformationen werden im Repository und gegebenenfalls in Releases dokumentiert.
