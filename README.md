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

## Dokument Erstellung

- Zum Erzeugen wird [MikTeX](https://miktex.org/) empfohlen.
- Zum Schreiben eignen sich verschiedne Editoren: [TeXStudio](https://www.texstudio.org/), [Texmaker](https://www.xm1math.net/texmaker/)
- Grafische Clients für die Versionsverwaltung: [git gui](https://git-scm.com/), [github desktop](https://desktop.github.com/)

manuelle Erstellung:
```bash
pdflatex main.tex
biber main
pdflatex main.tex
pdflatex main.tex
```

## Quellen
Die Vorlage wurde von folgender Implementierungen inspiriert:
- DHBW Heidenheim
- [programonaut/latex-template](https://github.com/programonaut/latex-template)
