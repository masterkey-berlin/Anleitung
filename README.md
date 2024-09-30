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

- Dazu verwendet er den Befehl `git remote add origin ...` und kann dann nach einem `git push -u origin master` seine lokalen Änderungen pushen.
- Die anderen Entwickler können sich auch den upstream auf das Repo setzen, wenn sie als Collaborator hinzugefügt werden. Das funktioniert, indem der Entwickler, dem das Repository gehört, auf seinem Repository in Github auf Settings geht und dann unter Collaborators --> Add die Entwickler mit ihren Github-Namen hinzufügt.
5. Synchronisieren von Änderungen
- Zum Pushen führe folgenden Befehl aus `git push -u origin master` (einmal, danach reicht ein `git push`)
- Zum Pullen führe folgenden Befehl aus `git pull (--rebase, dann holen wir uns aktuelle Ändeurngen vom Master-Branch in unseren aktuellen Stand/Branch)
- Achtung: Wenn zwei Entwickler gleichzeitig an dem Repository arbeiten, dann versuche immer wieder die Änderungen mit zu integrieren --> immer wieder ein git pull --rebase durchführen!
6. Branching und Feature-Entwicklung
- Erstelle einen separaten Branch mit `git branch <neuerBranch>` oder direkt mit `git checkout -b <neuerBranch>` (damit switchen wir direkt auf den Branch
- Dort kannst du Veränderungen durchführen und musst diese regelmäßig committen.
- Für die ständige Integration verwende regelmäßig ein `git merge master`, um dir den aktuellen Hauptbranch in den aktuellen Feature-Branch zu ziehen und zu schauen, ob es Konflikte gibt.
7. Zusammenführen von Branches
- mit `git checkout master` gehe auf den main-Branch und führe ein `git merge <FeatureBranch>`durch. Wenn Konflikte entstehen, löse die manuell. Wenn du fertig bist, kannst du deinen Stand pushen.
- Alternativ: Pushe den Feature-Branch auf das Remote Repository und erstelle dort einen Pull Request ; Danke)
