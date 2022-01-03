
Kommando | Beschreibung
-| - | - 
docker run hello-world	| Container starten
docker images | Lokale Images anzeigen
docker run -it ubuntu |	Container interaktiv starten
docker ps | Laufende Container anzeigen
docker ps -a | Auch beendete Container anzeigen
docker start container_id | Einen beendenten Container erneut starten
docker start -i container_id | Einen beendenten Container erneut interaktiv starten
docker run -d ubuntu sleep 30 | Container im Hintergrund starten, der sich nach 30 Sekunden beendet
docker run -d -p 8080:80 httpd | Container im Hintergrund mit Weiterleitung zum Port 8080 im Host starten
docker logs container_id | Logs auf Stdout und Stderr  zur Laufzeit und bei beendeten Containern anzeigen
docker logs -t container_id | Optional den Zeitstempel mit anzeigen
docker kill container_id | Container beenden
docker stop container_id | Container stoppen
docker rm container_id | Beendete Container löschen
docker run --rm -it ubuntu | Container automatisch löschen; Nachteil: keine Historie oder Logausgaben
docker container prune | Alle beendeten Container löschen
docker image prune | Nicht mehr benötigte Images löschen
docker system prune | Ganzes Hostsystem aufräumen

Optionen | Beschreibung
-| - | - 
-v "$(pwd):/hello"	| Angabe des Volumes host:container
-w /hello | Wechsel in das hello Verzeichnis im Container
npx express-generator | Aufruf des npx Kommandos
```
docker run -v "$(pwd):/hello" -w /hello node:lts-alpine npx express-generator
``



###### Quellen
[Docker - Tutorial (the native web GmbH)](https://www.youtube.com/watch?v=e1BOFzxgQQY&list=PL6QrD7_cU23li4myvLoicA663wx1bmzQi)