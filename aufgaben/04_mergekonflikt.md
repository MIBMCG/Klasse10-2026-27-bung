# Aufgabe 4 - Einen Merge-Konflikt erkennen und lösen

**Ziel:** Du verstehst, warum Merge-Konflikte entstehen und kannst einen einfachen Konflikt kontrolliert lösen.

> Diese Aufgabe wird zu zweit durchgeführt. Haltet euch genau an die Reihenfolge der Lehrkraft.

## A. Beide starten vom gleichen Stand

Beide Personen führen aus:

```bash
git switch main
git pull
git switch -c konflikt-DEINBENUTZERNAME
```

## B. Beide ändern dieselbe Zeile

Öffnet die euch zugewiesene Datei `konflikt/paar-XX.md` und ersetzt die Zeile mit dem Projektmotto jeweils durch **unterschiedliche** Formulierungen.

Danach jeweils:

```bash
git add konflikt/paar-XX.md
git commit -m "Ändere Projektmotto"
git push -u origin konflikt-DEINBENUTZERNAME
```

## C. Erster Branch wird gemergt

Person A erstellt einen Pull Request und lässt ihn nach `main` mergen.

## D. Person B aktualisiert und erhält den Konflikt

Person B führt im eigenen Branch aus:

```bash
git fetch origin
git merge origin/main
```

Git kann die konkurrierenden Änderungen nun möglicherweise nicht automatisch zusammenführen.

In der Datei erscheinen Konfliktmarker nach diesem Prinzip:

```text
<<<<<<< HEAD
meine Version
=======
andere Version
>>>>>>> ...
```

## E. Konflikt lösen

1. Entscheidet gemeinsam, welche endgültige Formulierung sinnvoll ist.
2. Entfernt **alle** Konfliktmarker.
3. Speichert die Datei.
4. Prüft den Zustand:

```bash
git status
```

5. Schließt die Konfliktlösung ab:

```bash
git add konflikt/paar-XX.md
git commit -m "Löse Konflikt beim Projektmotto"
git push
```

Danach kann auch der Pull Request von Person B wieder zusammengeführt werden.

## Reflexion

1. Warum konnte Git den Konflikt nicht selbstständig lösen?
2. Nenne zwei Verhaltensweisen, mit denen Teams unnötige Merge-Konflikte reduzieren können.
3. Warum ist ein Merge-Konflikt kein „Fehler von Git“?
