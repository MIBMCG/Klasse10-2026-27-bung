# Git-Cheatsheet

## Der wichtigste Arbeitszyklus

```text
GitHub -> clone/pull -> lokaler Arbeitsordner -> add -> commit -> push -> GitHub
```

| Befehl | Bedeutung | Typischer Einsatz |
|---|---|---|
| `git init` | aktuellen Ordner als neues lokales Git-Repository initialisieren | bei neuen lokalen Projekten |
| `git clone URL` | Repository vollständig lokal kopieren | einmal zu Beginn |
| `git status` | aktuellen Zustand anzeigen | sehr häufig |
| `git diff` | noch nicht gestagte Änderungen anzeigen | vor `git add` |
| `git add DATEI` | Datei für nächsten Commit stagen | vor jedem Commit |
| `git add .` | alle passenden Änderungen im aktuellen Bereich stagen | mit Vorsicht |
| `git commit -m "Nachricht"` | gestagte Änderungen als Version speichern | nach sinnvoller Änderung |
| `git log --oneline` | Commit-Historie kompakt anzeigen | Verlauf prüfen |
| `git pull` | Änderungen vom Remote holen und integrieren | vor Arbeitsbeginn / vor Push |
| `git push` | eigene Commits zum Remote übertragen | nach Commits |
| `git branch` | lokale Branches anzeigen | Orientierung |
| `git switch -c NAME` | neuen Branch erstellen und dorthin wechseln | neue Aufgabe |
| `git switch NAME` | Branch wechseln | zwischen Arbeitsständen wechseln |
| `git merge NAME` | angegebenen Branch in aktuellen Branch integrieren | gezieltes Zusammenführen |
| `git restore DATEI` | ungestagte lokale Änderung an Datei verwerfen | nur wenn wirklich gewollt |
| `git restore --staged DATEI` | Datei aus der Staging Area nehmen, Änderung aber behalten | versehentlich gestagte Datei |
| `git stash` | noch nicht committe Änderungen vorübergehend beiseitelegen | kurzfristig sauberen Arbeitsstand benötigen |
| `git stash pop` | zuletzt beiseitegelegte Änderungen wieder anwenden | nach einem Stash |
| `git branch -d NAME` | bereits integrierten lokalen Branch löschen | nach abgeschlossenem Merge |
| `git fetch` | Remote-Informationen holen, ohne direkt zu mergen | fortgeschrittene Kontrolle |
| `git remote -v` | konfigurierte Remotes und ihre Adressen anzeigen | Verbindung prüfen |
| `git show` | Details zu einem Commit anzeigen | Historie untersuchen |
| `git log --graph --oneline --all` | Branch- und Commitverlauf kompakt als Graph anzeigen | Überblick über mehrere Branches |

## Vier Zustände einer Änderung

1. **untracked / modified** - Datei ist neu oder verändert.
2. **staged** - Änderung liegt in der Staging Area (`git add`).
3. **committed** - Änderung ist lokal in der Versionsgeschichte gespeichert.
4. **pushed** - Commit ist auch im Remote-Repository auf GitHub vorhanden.

## Gute Commit-Nachrichten

Gut:

- `Ergänze Definition von Repository`
- `Korrigiere Markdown-Tabelle`
- `Füge Beitrag für Teamaufgabe hinzu`

Weniger gut:

- `Update`
- `Test`
- `asdf`

Eine Commit-Nachricht soll kurz sagen, **was** sich geändert hat.

## Häufig in älteren Anleitungen

Ältere Tutorials verwenden oft `git checkout`. Für das reine Wechseln von Branches nutzen wir in dieser Einheit das übersichtlichere `git switch`; für das Wiederherstellen von Dateien `git restore`.
