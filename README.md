# ToDo-App mit Node.js und Docker

## Über das Projekt

Bei diesem Projekt handelt es sich um eine einfache ToDo-Anwendung mit Node.js.
Die App kann entweder direkt auf dem Computer oder über Docker gestartet werden.

Für das Projekt werden folgende Programme und Technologien verwendet:

- Node.js
- npm
- Git und GitHub
- Docker
- Docker Compose
- Visual Studio Code

## Voraussetzungen

Bevor das Projekt gestartet werden kann, sollten folgende Programme installiert sein:

- Git
- Node.js inklusive npm
- Docker Desktop
- Visual Studio Code

## Projekt herunterladen

Das Repository wird zuerst von GitHub auf den eigenen Computer geklont:

```bash
git clone https://github.com/dzenansamedsacirovic/docker-nodejs-sample.git
```

Danach wechselt man in den Projektordner:

```bash
cd docker-nodejs-sample
```

## Node.js-Pakete installieren

Die benötigten Pakete werden mit folgendem Befehl installiert:

```bash
npm install
```

## App lokal starten

Die ToDo-App kann lokal mit diesem Befehl gestartet werden:

```bash
npm run dev
```

Danach ist die Anwendung im Browser unter folgender Adresse erreichbar:

```text
http://localhost:3000
```

## Docker-Image erstellen

Damit die Anwendung in einem Container ausgeführt werden kann, wird zuerst ein Docker-Image erstellt:

```bash
docker build -t todo-app .
```

Die vorhandenen Images können danach kontrolliert werden:

```bash
docker image ls
```

## App mit Docker starten

Mit folgendem Befehl wird aus dem Image ein Container gestartet:

```bash
docker run --name todo-container -p 3000:3000 todo-app
```

Die ToDo-App ist danach ebenfalls unter folgender Adresse erreichbar:

```text
http://localhost:3000
```

Mit diesem Befehl können laufende Container angezeigt werden:

```bash
docker ps
```

## Container stoppen und entfernen

Der laufende Container kann mit folgendem Befehl gestoppt werden:

```bash
docker stop todo-container
```

Danach kann der Container entfernt werden:

```bash
docker rm todo-container
```

Das Docker-Image bleibt dabei bestehen.

## Docker Compose verwenden

Die Anwendung kann auch mit Docker Compose gestartet werden:

```bash
docker compose up --build
```

Wenn der Container im Hintergrund laufen soll:

```bash
docker compose up -d
```

Mit folgendem Befehl kann der Status kontrolliert werden:

```bash
docker compose ps
```

## Änderungen übernehmen

Wenn der Quellcode geändert wurde, kann das Image neu gebaut werden:

```bash
docker compose up -d --build
```

Dadurch werden die aktuellen Änderungen in das Docker-Image übernommen.

## Docker Compose stoppen

Die Compose-Umgebung kann mit folgendem Befehl beendet werden:

```bash
docker compose down
```

## Autor

Dzenan-Samed Sacirovic