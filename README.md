# LaTeX Vorlage für die DHBW Stuttgart, Fachbereich Technik

Dieses Repository enthält eine LaTeX Vorlage für dieverse wissenschaftliche Berichte im Bachelor Studium. \
Die Vorlage umfasst die Möglichkeit zum Erzeugen der T3_1000, T3_2000, T3_3000, T3_3100, T3_3200, T3_3300. \
Formatvorlage sind die [Leitlinien](https://www.dhbw.de/die-dhbw/dokumente#Dokumente_Technik) des Fachbereichs Technik.

## Strukturierung
- `main.tex`: Hauptdatei mit Einbindung aller Dateien
- `config/config.tex`: Einstellungen der Vorlage
- `config/header.tex`: Header mit Paketen und Einstellungen
- `content/chapters.tex`: Einbindung aller Kapitel, Empfehlung: pro Kapitel eine Datei
- `resources/cover.tex`: Titelseite
- `resources/restrictionNotices.tex`: Sperrvermerk
- `resources/declaration.tex`: Erklärung zur eigenständigen Erstellung
- `resources/genus`: Anmerkung zum Genus des Substantivs
- `resources/abstract.tex`: Abstrakt auf Deutsch und Englisch
- `resources/acronyms.tex`: Abkürzungen alphabetisch sortiert
- `resources/appendix.tex`: Anhang
- `resources/images/`: Ordner mit Bildern
- `.gitignore`: von der Versionsverwaltung ignorierte Dateien
- `.github/workflows/build.yml`: Github Workflow für automatisiertes Erstellen
- `.gitlab-ci.yml`: GitLab CI Pipeline für automatisiertes Erstellen

## Dokument Erstellung

- Eine LaTeX Distribution wird benötigt: [MikTeX](https://miktex.org/), [TeXLive](https://www.tug.org/texlive/)
- Zum Schreiben eignen sich verschiedne Editoren: [TeXStudio](https://www.texstudio.org/), [Texmaker](https://www.xm1math.net/texmaker/)
- Grafische Clients für die Versionsverwaltung: [git gui](https://git-scm.com/), [github desktop](https://desktop.github.com/)

manuelle Erstellung:
```bash
pdflatex main.tex
biber main
pdflatex main.tex
pdflatex main.tex
```

Für plattformunabhängiges/automatisiertes Erstellen eignet sich auch [docker](https://docs.docker.com/get-started/). Siehe hierzu `.github/workflows/build.yml` und `.gitlab-ci.yml`.

## Quellen
Die Vorlage wurde von folgender Implementierungen inspiriert:
- DHBW Heidenheim
- [programonaut/latex-template](https://github.com/programonaut/latex-template)

## Bekannte Bugs
- miktex muss auf neuestem Stand sein, sonst arbeitet `biber` nicht richtig
