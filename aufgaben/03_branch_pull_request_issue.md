# Aufgabe 3 - Branches, Issues und Pull Requests

**Ziel:** Du arbeitest an einer Änderung, ohne `main` direkt zu verändern, und lässt deine Änderung über einen Pull Request prüfen.

## A. Issue anlegen

Erstelle auf GitHub ein Issue mit dem Titel:

```text
Eigenen Glossarbeitrag per Pull Request ergänzen
```

Beschreibe darin:

- welchen Begriff du erklären möchtest,
- dass du die Datei `glossar/DEINBENUTZERNAME.md` anlegen wirst,
- wann die Aufgabe als erledigt gelten kann.

## B. Eigenen Branch erstellen

Zuerst sicherstellen, dass `main` aktuell ist:

```bash
git switch main
git pull
git switch -c glossar-DEINBENUTZERNAME
```

Prüfe:

```bash
git branch
git status
```

## C. Änderung durchführen

Lege die Datei `glossar/DEINBENUTZERNAME.md` an. Sie soll einen Git-Begriff, eine kurze Definition und ein kleines Anwendungsbeispiel enthalten.

Dann:

```bash
git diff
git add glossar/DEINBENUTZERNAME.md
git commit -m "Ergänze Glossarbeitrag zu ..."
git push -u origin glossar-DEINBENUTZERNAME
```

## D. Pull Request erstellen

Erstelle auf GitHub einen Pull Request von deinem Branch nach `main`.

Der Pull Request soll enthalten:

- einen aussagekräftigen Titel,
- eine kurze Beschreibung der Änderung,
- einen Verweis auf dein Issue, z. B. `Closes #12`, wenn die Issue-Nummer 12 lautet.

## E. Review

Prüfe den Pull Request einer anderen Person:

- Ist die Änderung fachlich sinnvoll?
- Ist Markdown korrekt?
- Ist die Commit-Nachricht nachvollziehbar?

Formuliere mindestens einen sachlichen Review-Kommentar. Danach wird der Pull Request gemäß Vorgabe der Lehrkraft gemergt.

## F. Nach dem Merge aufräumen (optional)

Nach erfolgreichem Merge kannst du lokal aufräumen:

```bash
git switch main
git pull
git branch -d glossar-DEINBENUTZERNAME
```

Den Remote-Branch kannst du über GitHub löschen oder mit `git push origin --delete glossar-DEINBENUTZERNAME`.

## Reflexion

Warum ist ein eigener Branch mit Pull Request in einem Teamprojekt oft sinnvoller als direkt auf `main` zu arbeiten?
