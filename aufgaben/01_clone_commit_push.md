# Aufgabe 1 - Vom GitHub-Repository zum ersten eigenen Commit

**Ziel:** Du kannst ein Repository klonen, eine Markdown-Datei verändern, die Änderung stagen, committen und pushen.

## A. Repository klonen

1. Kopiere auf GitHub über **Code -> HTTPS** die Repository-Adresse.
2. Öffne PowerShell oder Git Bash im gewünschten Arbeitsordner.
3. Führe aus:

```bash
git clone REPOSITORY-URL
cd REPOSITORY-NAME
git switch -c uebung-DEINBENUTZERNAME
git status
```

Du arbeitest damit auf deinem persönlichen Übungsbranch. Branches werden in Aufgabe 3 ausführlich erklärt; hier sorgt er zunächst dafür, dass sich parallele Pushes der Klasse nicht gegenseitig blockieren.

## B. Eigene Beitragsdatei anlegen

Erstelle im Ordner `beitraege` eine neue Datei. Verwende den von der Lehrkraft vereinbarten Benutzernamen:

```text
beitraege/dein-benutzername.md
```

Die Datei soll enthalten:

- eine Überschrift,
- den Satz „Git hilft dabei, Änderungen nachvollziehbar zu speichern.“,
- drei Stichpunkte dazu, was du dir von GitHub im Informatikunterricht versprichst,
- mindestens einen Git-Befehl als Inline-Code.

## C. Änderung prüfen und committen

```bash
git status
git diff
git add beitraege/dein-benutzername.md
git status
git diff --staged
git commit -m "Füge meinen ersten Markdown-Beitrag hinzu"
git log --oneline -5
```

> Hinweis: Bei einer ganz neuen, noch nicht gestagten Datei kann `git diff` zunächst leer bleiben. `git status` zeigt die Datei trotzdem als *untracked*. Nach `git add` zeigt `git diff --staged` den Inhalt, der in den Commit eingehen soll.

## D. Commit veröffentlichen

```bash
git push -u origin uebung-DEINBENUTZERNAME
```

Öffne anschließend GitHub im Browser und kontrolliere, ob dein Commit und deine Datei sichtbar sind.

## Reflexion

Erkläre in 2-3 Sätzen den Unterschied zwischen `git add`, `git commit` und `git push`.
