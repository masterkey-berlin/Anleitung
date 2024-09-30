# Anleitung für Versionierung eines Projektes
1. Initialisierung des Projekts mit Git
- Installiere Git entweder über einen Paketmanager, wie z.B. choco/brew/apt 
- Initialisiere das Verzeichnis als git-Repository mit `git init`
2. Einrichtung von Git:
- Identifiziere dich eindeutig, indem du die beiden Befehle `git config --global user.name "username"` und `git config --global user.email "email"`
- Das ist wichtig, damit deine Commits deinem Usernamen und deiner E-Mail-Adresse zugeordnet werden können
3. Verwaltung von Änderungen in Git
- Erstelle eine neue Datei mit `touch README.md` und füge diese zum Staging-Bereich mit `git add .` hinzu.
- Möchtest du diesen Stand committen, also eine neue Version erstellen, dann führe ein `git commit -m "..."`durch 
