~# Git-Anleitung für Team-Entwickler

# 1. Initialisierung des Projekts mit Git

## 1.1 Git einrichten

- Zuerst muss Git auf jedem Rechner installiert werden:

  -Git installieren (https://git-scm.com/downloads)

## 1.2 Neues Git-Repository initialisieren

- Navigiere in den Projektordner und führe folgendes Kommando aus:

  git init

# 2. Einrichtung von Git

## 2.1 Git konfigurieren (Name und E-Mail)

Jeder Entwickler muss sich identifizieren:

bash

Code kopieren

git config --global user.name "Dein Name"

git config --global user.email "deine-email@example.com"

# 3. Verwaltung von Änderungen mit Git

## 3.1 Datei erstellen und hinzufügen

Eine neue Datei (z.B. README.md) erstellen und sie mit Git verfolgen:

bash

Code kopieren

echo "# Mein Projekt" > README.md

git add README.md

## 3.2 Änderungen committen

Die Änderungen werden mit einem Commit gespeichert:

bash

Code kopieren

git commit -m "Initial commit mit README.md"

# 4. Verbindung zu einem Remote-Repository

## 4.1 Remote-Repository erstellen

Ein neues Repository auf GitHub erstellen.

## 4.2 Remote-Repository hinzufügen

Das Remote-Repository lokal verknüpfen:

bash

Code kopieren

git remote add origin https://github.com/dein-benutzername/dein-repository.git

git push -u origin main

# 5. Synchronisieren von Änderungen

## 5.1 Änderungen pushen und pullen

Änderungen ins Remote-Repository hochladen:

bash

Code kopieren

git push

Änderungen vom Remote-Repository herunterladen:

bash

Code kopieren

git pull

## 5.2 Konflikte auflösen

Falls Konflikte auftreten, diese manuell bearbeiten, dann die Änderungen committen und pushen:

bash

Code kopieren

git add .

git commit -m "Konflikte gelöst"

git push

# 6. Branching und Feature-Entwicklung

## 6.1 Neuen Branch erstellen

Für die Entwicklung eines neuen Features einen separaten Branch erstellen:

bash

Code kopieren

git checkout -b feature/neues-feature

## 6.2 Änderungen im Branch vornehmen und committen

Änderungen vornehmen und regelmäßig committen:

bash

Code kopieren

git add .

git commit -m "Feature hinzugefügt"

# 7. Zusammenführen von Branches

## 7.1 Branch in den Haupt-Branch mergen

Zurück in den main Branch wechseln:

bash

Code kopieren

git checkout main

Den Feature-Branch in den main Branch mergen:

bash

Code kopieren

git merge feature/neues-feature

## 7.2 Pull Request

Alternativ kann ein Pull Request über GitHub erstellt werden, um den Feature-Branch zu mergen.

:wq
# Anleitung
