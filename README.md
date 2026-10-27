# Server Monitoring Bot

Discord and Slack bots that report your server's system metrics, such as RAM usage, CPU load, uptime and disk usage.

**Languages:** [English](#english) · [Deutsch](#deutsch)

---

## English

### Table of contents

- [Commands](#commands)
- [Requirements](#requirements)
- [Discord bot setup](#discord-bot-setup)
- [Slack app setup](#slack-app-setup)

### Commands

| Discord        | Slack         | Description                                  |
| -------------- | ------------- | -------------------------------------------- |
| `/cpu`         | `/cpu`        | Current CPU usage                            |
| `/ram`         | `/ram`        | Current RAM usage                            |
| `/uptime`      | `/uptime`     | Server uptime and boot time                  |
| `/diskusage`   | `/diskusage`  | Disk usage                                   |
| `/systemload`  | `/systemload` | Load average (Linux/macOS only)              |
| `/processes`   | `/processes`  | Running processes sorted by CPU usage        |
| `/netstat`     | `/netstat`    | Connections per port, or details for a port  |
| `/who`         | `/serverwho`  | Currently logged-in users                    |

### Requirements

- Python 3.8 or newer
- `pip` and the `venv` module

```bash
sudo apt-get install python3 python3-pip python3-venv
```

### Discord bot setup

Example commands:

**`/ram`**

![RAM](example_pics/RAM.png)

**`/cpu`**

![CPU](example_pics/CPU.png)

**`/uptime`**

![Uptime](example_pics/uptime.png)

#### Installation

1. Download the Discord bot ZIP file from the [Releases page](https://github.com/Purzel149/Server_Monitoring/releases), or clone this repository and use `src/discordbot`.
2. Extract it to a folder of your choice on your server and open that folder.
3. Create a virtual environment and install the dependencies:

   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   pip install -r requirements.txt
   ```

4. Create a `.env` file in the same directory:

   ```env
   DISCORD_TOKEN=your_token_here
   ```

   Replace `your_token_here` with the bot token from the [Discord Developer Portal](https://discord.com/developers/applications).
5. Start the bot:

   ```bash
   python3 bot.py
   ```

> [!NOTE]
> Don't forget to invite the bot to your Discord server.

### Slack app setup

Example commands:

**`/ram`**

![Slack RAM](example_pics/slack_RAM.png)

**`/cpu`**

![Slack CPU](example_pics/slack_CPU.png)

**`/diskusage`**

![Slack disk usage](example_pics/diskusage.png)

#### Installation

1. Download the Slack app ZIP file from the [Releases page](https://github.com/Purzel149/Server_Monitoring/releases), or clone this repository and use `src/slackbot`.
2. Extract it to a folder of your choice on your server and open that folder.
3. Create a virtual environment and install the dependencies:

   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   pip install -r requirements.txt
   ```

4. Create a `.env` file in the same directory:

   ```env
   SLACK_TOKEN=your_bot_token_here
   SLACK_APP_TOKEN=your_app_level_token_here
   ```

   - `SLACK_TOKEN`: the bot token (`xoxb-...`) from the [Slack API portal](https://api.slack.com/apps).
   - `SLACK_APP_TOKEN`: the app-level token (`xapp-...`) required for Socket Mode.
5. Create the slash commands in your Slack app (`/cpu`, `/ram`, `/uptime`, `/diskusage`, `/systemload`, `/processes`, `/netstat`, `/serverwho`) and enable Socket Mode.
6. Start the app:

   ```bash
   python3 bot.py
   ```

The commands should now be available in your Slack workspace.

> [!WARNING]
> The bots do not restrict who can run commands. `/who`, `/netstat` and `/processes` expose server details, so only add the bot to servers or workspaces you trust.

---

## Deutsch

### Inhaltsverzeichnis

- [Befehle](#befehle)
- [Voraussetzungen](#voraussetzungen)
- [Discord-Bot einrichten](#discord-bot-einrichten)
- [Slack-App einrichten](#slack-app-einrichten)

### Befehle

| Discord        | Slack         | Beschreibung                                         |
| -------------- | ------------- | ---------------------------------------------------- |
| `/cpu`         | `/cpu`        | Aktuelle CPU-Auslastung                              |
| `/ram`         | `/ram`        | Aktuelle RAM-Auslastung                              |
| `/uptime`      | `/uptime`     | Laufzeit und Startzeitpunkt des Servers              |
| `/diskusage`   | `/diskusage`  | Festplattennutzung                                   |
| `/systemload`  | `/systemload` | Systemauslastung (nur Linux/macOS)                   |
| `/processes`   | `/processes`  | Laufende Prozesse, sortiert nach CPU-Auslastung      |
| `/netstat`     | `/netstat`    | Verbindungen pro Port oder Details für einen Port    |
| `/who`         | `/serverwho`  | Aktuell angemeldete Benutzer                         |

### Voraussetzungen

- Python 3.8 oder neuer
- `pip` und das Modul `venv`

```bash
sudo apt-get install python3 python3-pip python3-venv
```

### Discord-Bot einrichten

Beispiele für die Befehle:

**`/ram`**

![RAM](example_pics/RAM.png)

**`/cpu`**

![CPU](example_pics/CPU.png)

**`/uptime`**

![Uptime](example_pics/uptime.png)

#### Installationsanleitung

1. Lade die Discord-Bot-ZIP-Datei von der [Releases-Seite](https://github.com/Purzel149/Server_Monitoring/releases) herunter, oder klone dieses Repository und nutze `src/discordbot`.
2. Entpacke sie in einen Ordner deiner Wahl auf deinem Server und wechsle in diesen Ordner.
3. Erstelle eine virtuelle Umgebung und installiere die Abhängigkeiten:

   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   pip install -r requirements.txt
   ```

4. Erstelle im selben Verzeichnis eine `.env`-Datei:

   ```env
   DISCORD_TOKEN=dein_token_hier
   ```

   Ersetze `dein_token_hier` durch den Bot-Token aus dem [Discord Developer Portal](https://discord.com/developers/applications).
5. Starte den Bot:

   ```bash
   python3 bot.py
   ```

> [!NOTE]
> Vergiss nicht, den Bot auf deinen Discord-Server einzuladen.

### Slack-App einrichten

Beispiele für die Befehle:

**`/ram`**

![Slack RAM](example_pics/slack_RAM.png)

**`/cpu`**

![Slack CPU](example_pics/slack_CPU.png)

**`/diskusage`**

![Slack Festplattennutzung](example_pics/diskusage.png)

#### Installationsanleitung

1. Lade die Slack-App-ZIP-Datei von der [Releases-Seite](https://github.com/Purzel149/Server_Monitoring/releases) herunter, oder klone dieses Repository und nutze `src/slackbot`.
2. Entpacke sie in einen Ordner deiner Wahl auf deinem Server und wechsle in diesen Ordner.
3. Erstelle eine virtuelle Umgebung und installiere die Abhängigkeiten:

   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   pip install -r requirements.txt
   ```

4. Erstelle im selben Verzeichnis eine `.env`-Datei:

   ```env
   SLACK_TOKEN=dein_bot_token_hier
   SLACK_APP_TOKEN=dein_app_level_token_hier
   ```

   - `SLACK_TOKEN`: der Bot-Token (`xoxb-...`) aus dem [Slack-API-Portal](https://api.slack.com/apps).
   - `SLACK_APP_TOKEN`: der App-Level-Token (`xapp-...`), der für den Socket Mode benötigt wird.
5. Lege die Slash-Befehle in deiner Slack-App an (`/cpu`, `/ram`, `/uptime`, `/diskusage`, `/systemload`, `/processes`, `/netstat`, `/serverwho`) und aktiviere den Socket Mode.
6. Starte die App:

   ```bash
   python3 bot.py
   ```

Die Befehle sollten nun in deinem Slack-Workspace verfügbar sein.

> [!WARNING]
> Die Bots schränken nicht ein, wer Befehle ausführen darf. `/who`, `/netstat` und `/processes` zeigen Serverdetails an. Füge den Bot daher nur zu vertrauenswürdigen Servern oder Workspaces hinzu.
