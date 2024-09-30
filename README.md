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
- Mit `git status` überprüfen wir, welche Files bisher schon zur Staging-Area hinzugefügt worden sind.
4. Verbindung zu einem Remote-Repository
- Du hast bereits einen Github-Account angelegt.
- Du musst eine Verbindung zwischen deinem lokalen Rechner und deinem Github-Account herstellen. Führe dazu folgende Scrhitte durch:
- Generiere dir einen SSH-Key mit dem Befehl `ssh-keygen -t ed25519 -C "E-Mail"`. Du wirst nach dem Pfad gefragt, wo es gespeichert werden soll
- Gib hier den Standard ein. Setze kein Passwort. Mit cat musst dir den public-Key des generierten Keys asgeben lassen.
- Den kopierten Schlüssel fügst du unter Settings --> SSH Keys ein.
- Der Entwickler erstellt ein Repository auf Github (Profil --> Neues Repo erstellen ...). Er möchte sein lokales Git-Repository mit dem remote-REpository synchronisieren
- Dazu verwendet er den Befehl `git remote add origin ...` und kann dann nach einem `git push -u origin master` seine lokalen Änderungen pushen   
