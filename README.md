# [Name der Action]

Diese GitHub-Action [beschreibt, was die Action tut].

## Beschreibung

Diese Action ist nützlich für [spezifischen Anwendungsfall der Action beschreiben]. Sie ermöglicht es [kurze Erläuterung der wichtigsten Funktionen und Schritte der Action].

## Eingaben

| Name              | Beschreibung                                                     | Erforderlich | Standardwert |
|-------------------|------------------------------------------------------------------|--------------|--------------|
| `input-name`      | Beschreibung des Eingabewerts                                    | Ja/Nein      | [Standardwert, falls zutreffend] |
| `input-name`      | Beschreibung des Eingabewerts                                    | Ja/Nein      | [Standardwert, falls zutreffend] |
| ...               | ...                                                              | ...          | ...          |

## Verwendung

Erstellen Sie eine Workflow-Datei (z. B. `.github/workflows/[workflow-name].yml`) und verwenden Sie diese Action wie folgt:

```yaml
name: [Name des Workflows]

on:
  push:
    branches:
      - main

jobs:
  [job-name]:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v2

      - name: [Name der Action]
        uses: ./
        with:
          input-name: "[Beispielwert]"
          input-name: "[Beispielwert]"
```

## Schritte im Workflow

    Installiere pypa/build: Installiert das build-Paket, das für den Bau des Python-Pakets benötigt wird.
    Baue ein Rad und eine Quell-Tarball: Baut das Paket und erstellt eine .whl- und eine .tar.gz-Datei im dist/-Ordner.
    Veröffentliche Paket auf TestPyPI: Nutzt die gh-action-pypi-publish, um die Paketdateien auf das angegebene TestPyPI-Repository hochzuladen.

## Erforderliche Berechtigungen

Um die Action erfolgreich auszuführen, muss ein Authentifizierungstoken in den Repository-Geheimnissen (secrets) gespeichert werden, um das Paket auf TestPyPI zu veröffentlichen.