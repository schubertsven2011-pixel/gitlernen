# GitHub-Grundbefehle – einfach erklärt

GitHub ist wie ein Online-Speicher für Programmier-Projekte.
Mit **Git** speicherst du Änderungen auf deinem Computer und lädst sie danach zu GitHub hoch.

## Neues Git-Projekt anlegen

Wenn dein Ordner noch kein Git-Projekt ist, öffne ihn in VS Code und führe im Terminal diese Befehle aus:

```bash
git init
git add .
git commit -m "GitHub Befehle erweitert"

git init macht aus dem Ordner ein Git-Projekt. Danach werden mit git add . alle Dateien ausgewählt und mit git commit
als erster Speicherpunkt gespeichert.

## Projekt herunterladen

git clone https://github.com/NAME/PROJEKT.git

Damit lädst du ein Projekt von GitHub auf deinen Computer. Den Link findest du auf GitHub unter dem grünen Button
Code.

## In den Projektordner gehen

cd PROJEKT

Damit wechselst du im Terminal in den Ordner des Projekts. Erst dann weiß Git, an welchem Projekt du arbeiten
möchtest.

## Schauen, was geändert wurde

git status

Dieser Befehl zeigt dir, welche Dateien du geändert hast. Du kannst nichts kaputtmachen, denn es wird nur
nachgeschaut.

## Eine Datei zum Speichern auswählen

git add README.md

Damit sagst du Git: „Diese Datei möchte ich gleich speichern.“
Wenn du alle geänderten Dateien auswählen möchtest, schreibst du:

git add .

## Änderung speichern

git commit -m "Ich habe die Anleitung verbessert"

Ein Commit ist wie ein Speicherpunkt in einem Spiel. Der Text zwischen den Anführungszeichen erklärt, was du gemacht
hast.

## Zu GitHub hochladen

git push

Damit lädst du deine gespeicherten Änderungen zu GitHub hoch. Danach können andere die neue Version online sehen.

## Neue Änderungen von GitHub holen

git pull

Damit lädst du Änderungen herunter, die andere Leute inzwischen zu GitHub hochgeladen haben. Mache das am besten,
bevor du selbst mit der Arbeit beginnst.

## Die wichtigsten Befehle zusammen

git pull
git status
git add .
git commit -m "Meine Änderung"
git push

Das ist der normale Ablauf: Erst aktualisieren, dann ändern, speichern und hochladen.


##it branch Listet alle Branches eines Git-Projekts auf.

git branch branch_name: Erstellt einen neuen Zweig.
git checkout branch_nameWird verwendet, um von einem Zweig zum anderen zu wechseln.
git merge branch_name: Wird verwendet, um Dateiänderungen von einem Zweig in einen anderen zu übertragen.
git branch -d branch_nameLöscht den angegebenen Zweig
