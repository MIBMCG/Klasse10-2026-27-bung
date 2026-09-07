# Fehlerhilfe

## `fatal: not a git repository`

Du befindest dich wahrscheinlich nicht im Repository-Ordner.

```bash
pwd
ls
```

Unter PowerShell helfen entsprechend:

```powershell
Get-Location
Get-ChildItem
```

Wechsle anschließend mit `cd ORDNERNAME` in das Repository.

## `nothing to commit`

Prüfe:

```bash
git status
```

Vielleicht wurde die Datei nicht gespeichert oder die Änderung wurde schon committed.

## Änderung wird beim Commit nicht übernommen

Wahrscheinlich fehlt das Staging:

```bash
git add DATEI.md
git status
git commit -m "Sinnvolle Nachricht"
```

## Push wird abgelehnt

Häufig hat sich das Remote inzwischen verändert. Prüfe zuerst:

```bash
git status
git pull
```

Danach ggf. Konflikt lösen und erneut pushen.

## Merge-Konflikt

Nicht in Panik geraten. Git markiert die betroffenen Stellen. Entscheide, welche Inhalte bleiben sollen, entferne die Konfliktmarker und führe danach aus:

```bash
git add DATEI.md
git commit -m "Löse Merge-Konflikt"
git push
```

## Ich weiß nicht, was Git gerade erwartet

Fast immer ist der beste erste Befehl:

```bash
git status
```
