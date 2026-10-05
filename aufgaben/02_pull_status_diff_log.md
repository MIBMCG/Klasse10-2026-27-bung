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
A: Der Befehl git pull lädt neue Änderungen von GitHub herunter und fügt sie sofort in meinem lokalen Repository ein.
Kontrolliere anschließend, ob die im Browser ergänzte Zeile auch lokal vorhanden ist.

## B. Eine Änderung untersuchen

Ergänze in deiner eigenen Datei einen neuen Abschnitt:

```markdown
## Mein wichtigster Git-Befehl

Der wichtigste Befehl ist für mich `git status`, weil er den aktuellen Stand meines Projektordners und des Staging-Bereichs anzeigt. 
```
Der Befehl git diff zeigt die Unterschiede zwischen verschiedenen Zuständen meines Codes an. 
Führe **vor dem Staging** aus:

```bash
git status
git diff
```

Notiere, was dir Git anzeigt.
Git zeigt den aktuellen Zustand meines Arbeitsverzeichnisses an. 
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

Welche Information enthält jede Zeile von `git log --oneline`?
Jede Zeile von ´git log --online´ zeigt eine kompakte Zusammenfassung eines Commits, bestehend aus zwei Hauptinformationen. Commit Hash und Commit Nachricht. 

Was hat `git pull` in Teil A zwischen GitHub und deinem lokalen Repository bewirkt?
Der Befehl git pull lädt neue Änderungen von GitHub herunter und fügt sie sofort in meinem lokalen Repository ein.

Worin unterscheiden sich `git diff` und `git diff --staged`?
Der Befehl git diff zeigt die Änderungen im Arbeitsverzeichnis, die noch nicht für den nächsten gespeicherten Schnappschuss (Commit) vorgemerkt sind und git diff –staged zeigt alle Änderungen an, die bereits mit git add bereitgestellt wurden.
