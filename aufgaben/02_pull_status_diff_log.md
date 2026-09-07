# Aufgabe 2 - Synchronisieren und Versionsgeschichte verstehen

**Ziel:** Du kannst lokale und entfernte Änderungen unterscheiden und ein Repository sicher synchronisieren.

## A. Eine Remote-Änderung erzeugen und holen

1. Öffne auf GitHub **deinen Übungsbranch**.
2. Bearbeite dort im Browser deine eigene Beitragsdatei und ergänze eine kurze Zeile.
3. Speichere diese Änderung auf GitHub als Commit direkt in deinem Übungsbranch.
4. Dein lokales Repository kennt diesen neuen Remote-Commit noch nicht. Hole ihn nun:

```bash
git status
git pull
```

Kontrolliere anschließend, ob die im Browser ergänzte Zeile auch lokal vorhanden ist.

## B. Eine Änderung untersuchen

Ergänze in deiner eigenen Datei einen neuen Abschnitt:

```markdown
## Mein wichtigster Git-Befehl

Der wichtigste Befehl ist für mich `git status`, weil ...
```

Führe **vor dem Staging** aus:

```bash
git status
git diff
```

Notiere, was dir Git anzeigt.

## C. Zweiten Commit erzeugen

```bash
git add beitraege/dein-benutzername.md
git diff --staged
git commit -m "Ergänze Erklärung zu git status"
git log --oneline -5
git push
```

## D. Historie lesen

Beantworte:

1. Welche Information enthält jede Zeile von `git log --oneline`?
2. Was hat `git pull` in Teil A zwischen GitHub und deinem lokalen Repository bewirkt?
3. Worin unterscheiden sich `git diff` und `git diff --staged`?
