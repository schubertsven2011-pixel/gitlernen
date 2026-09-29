== GitHub-Basics – einfach erklärt ==

'''Git''' ist ein Werkzeug, das Änderungen an Dateien lokal nachverfolgt und sich merkt. 
'''GitHub''' ist eine webbasierte Plattform, auf der du Git-Projekte speichern, verwalten und gemeinsam mit anderen im Team daran arbeiten kannst.

---

== Repository (Repo) ==

Ein Projekt auf GitHub wird als '''Repository''' (kurz: '''Repo''') bezeichnet. Stell dir das wie einen zentralen Projektordner in der Cloud vor – inklusive lückenlosem Versionsverlauf.

---

== Wichtige Begriffe ==

{| class="wikitable sortable"
! Begriff !! Bedeutung
|-
| '''Repository''' || Das gesamte Projekt, zum Beispiel eine Website oder ein Software-Skript.
|-
| '''Commit''' || Ein gespeicherter Zwischenstand mit einer sprechenden Nachricht, etwa: <tt>„Menü verbessert“</tt>.
|-
| '''Branch''' || Eine eigene Arbeitslinie (Zweig). Du kannst in Ruhe etwas ausprobieren, ohne die stabile Hauptversion zu gefährden.
|-
| '''main''' || Meist der Standard-Haupt-Branch: die stabile und produktive Version des Projekts.
|-
| '''Issue''' || Eine Aufgabe, eine Idee oder eine Fehlermeldung (Bug), zum Beispiel: <tt>„Der Login-Button funktioniert auf Mobilgeräten nicht.“</tt>
|-
| '''Pull Request (PR)''' || Eine Anfrage, Änderungen aus einem Entwicklungs-Branch in den <tt>main</tt>-Branch zu übernehmen. Teammitglieder können den Code hier prüfen und kommentieren.
|-
| '''Merge''' || Das offizielle Zusammenführen eines Pull Requests in den Haupt-Branch.
|-
| '''Fork''' || Deine eigene, unabhängige Kopie eines fremden Repositories auf GitHub (z. B. zum Mitwirken an Open-Source-Projekten).
|-
| '''Clone''' || Das vollständige Herunterladen eines GitHub-Repositories auf deinen lokalen PC.
|-
| '''Push''' || Das Hochladen deiner lokalen Änderungen zu GitHub.
|-
| '''Pull''' || Das Herunterladen von Änderungen von GitHub auf deinen lokalen PC.
|}

---

== Was kannst du direkt auf der GitHub-Webseite machen? ==

# Ein neues Repository anlegen (<tt>New repository</tt>).
# Dateien direkt im Browser bearbeiten oder hochladen.
# Unter '''Issues''' Aufgaben, Ideen und Fehler im Team strukturieren und sammeln.
# Unter '''Pull requests''' Änderungen vergleichen, im Team besprechen, kommentieren und freigeben.
# Unter '''Actions''' automatisierte Workflows (z. B. automatisierte Tests oder Deployments) ausführen lassen.
# Personen einladen und granulare Rechte vergeben, wer das Repository lesen oder bearbeiten darf.

---

== Der normale Arbeitsablauf ==

<pre>
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
</pre>

---

== Arbeiten im Terminal ==

Um lokal mit einem Projekt zu arbeiten, nutzt du die folgenden Befehle:

<syntaxhighlight lang="powershell">
# Ein bestehendes GitHub-Projekt auf deinen PC klonen
git clone https://github.com/NAME/PROJEKT.git

# In den neu erstellten Projektordner wechseln
cd PROJEKT

# Prüfen, welche Dateien sich geändert haben
git status

# Einen neuen Arbeits-Branch erstellen und direkt dorthin wechseln
git switch -c mein-neues-feature

# Alle geänderten Dateien für den nächsten Commit vormerken
git add .

# Lokalen Zwischenstand mit einer Nachricht speichern
git commit -m "Kontaktformular hinzugefügt"

# Deinen lokalen Branch zum ersten Mal zu GitHub hochladen
git push -u origin mein-neues-feature
</syntaxhighlight>

Nach dem Push zeigt dir GitHub im Browser meist direkt einen Button wie '''Compare & pull request'''. Klicke darauf, beschreibe kurz deine Änderungen und erstelle den Pull Request.

=== Änderungen von anderen holen ===

<syntaxhighlight lang="powershell">
# Sicherstellen, dass du auf dem Haupt-Branch bist
git switch main

# Aktuellen, stabilen Stand von GitHub herunterladen
git pull
</syntaxhighlight>

---

== Mini-Spickzettel ==

{| class="wikitable"
! Befehl !! Kurzbeschreibung
|-
| <tt>git status</tt> || Was wurde verändert? (Übersicht)
|-
| <tt>git add .</tt> || Alle Änderungen für den nächsten Commit vormerken
|-
| <tt>git commit -m "Nachricht"</tt> || Änderungen lokal mit Beschreibung speichern
|-
| <tt>git push</tt> || Lokale Commits zu GitHub hochladen
|-
| <tt>git pull</tt> || Änderungen von GitHub herunterladen
|}

{{Box|Hinweis|Arbeite bei neuen Funktionen oder Korrekturen möglichst immer in einem '''eigenen Branch''' und ändere den <tt>main</tt>-Branch nicht direkt. Auf diese Weise lassen sich Fehler problemlos isolieren und rückgängig machen, und Pull Requests bleiben übersichtlich.|style=note}}
