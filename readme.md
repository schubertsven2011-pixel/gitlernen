# GitHub-Basics – einfach erklärt

**Git** ist ein Werkzeug, das Änderungen an Dateien merkt.  
**GitHub** ist eine Webseite, auf der du Git-Projekte speichern und mit anderen zusammenarbeiten kannst.

## Repository (Repo)

Ein Projekt auf GitHub heißt **Repository**, kurz **Repo**. Stell es dir wie einen Projektordner in der Cloud vor – inklusive Versionsverlauf.

## Wichtige Begriffe

| Begriff | Bedeutung |
| --- | --- |
| **Repository** | Das gesamte Projekt, zum Beispiel eine Website oder ein Spiel. |
| **Commit** | Ein gespeicherter Zwischenstand mit einer Nachricht, etwa: „Menü verbessert“. |
| **Branch** | Eine eigene Arbeitslinie. Du kannst etwas ausprobieren, ohne die Hauptversion kaputtzumachen. |
| **main** | Meist der Haupt-Branch: die stabile Version des Projekts. |
| **Issue** | Eine Aufgabe, Idee oder Fehlermeldung, zum Beispiel: „Der Login-Button funktioniert nicht.“ |
| **Pull Request (PR)** | Eine Anfrage, Änderungen aus einem Branch in `main` zu übernehmen. Andere können den Code ansehen und kommentieren. |
| **Merge** | Das Zusammenführen eines Pull Requests in den Haupt-Branch. |
| **Fork** | Deine eigene Kopie eines fremden Repositories auf GitHub. |
| **Clone** | Ein GitHub-Repository auf deinen PC herunterladen. |
| **Push** | Deine lokalen Änderungen zu GitHub hochladen. |
| **Pull** | Änderungen von GitHub auf deinen PC holen. |

## Was kannst du auf der GitHub-Webseite machen?

1. Ein neues Repository anlegen (`New repository`).
2. Dateien direkt bearbeiten oder hochladen.
3. Unter **Issues** Aufgaben, Ideen und Fehler sammeln.
4. Unter **Pull requests** Änderungen vergleichen, kommentieren und zusammenführen.
5. Unter **Actions** automatische Tests oder Veröffentlichungen ausführen lassen.
6. Andere Personen einladen und festlegen, wer etwas bearbeiten darf.

## Der normale Ablauf

```text
Issue erstellen
   ↓
Branch dafür anlegen
   ↓
Dateien ändern
   ↓
Commit erstellen
   ↓
Push zu GitHub
   ↓
Pull Request öffnen
   ↓
Prüfen / kommentieren
   ↓
Merge nach main
```

## Arbeiten im Terminal

```powershell
# Ein bestehendes GitHub-Projekt auf deinen PC holen
git clone https://github.com/NAME/PROJEKT.git

# In den Projektordner wechseln
cd PROJEKT

# Prüfen, was sich geändert hat
git status

# Einen neuen Arbeits-Branch erstellen und direkt wechseln
git switch -c mein-neues-feature

# Alle geänderten Dateien zum nächsten Commit vormerken
git add .

# Zwischenstand speichern
git commit -m "Kontaktformular hinzugefügt"

# Deinen Branch auf GitHub hochladen
git push -u origin mein-neues-feature
```

Danach zeigt GitHub meist einen Button wie **Compare & pull request**. Klicke darauf, schreibe kurz, was du geändert hast, und erstelle den Pull Request.

## Änderungen von anderen holen

```powershell
# Zum Haupt-Branch wechseln
git switch main

# Aktuellen Stand von GitHub herunterladen
git pull
```

## Mini-Spickzettel

```powershell
git status                 # Was ist verändert?
git add .                  # Änderungen vormerken
git commit -m "Nachricht"  # Änderungen speichern
git push                   # Zu GitHub hochladen
git pull                   # Von GitHub herunterladen
```

> **Tipp:** Arbeite für neue Sachen möglichst in einem eigenen Branch und ändere `main` nicht direkt. So sind Fehler leichter rückgängig zu machen und Pull Requests bleiben übersichtlich.
