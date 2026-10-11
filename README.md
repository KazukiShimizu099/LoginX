# LoginX

<p align="center">
  **Automatic server login for Minecraft Fabric**
  <br>
  A lightweight client-side mod that remembers your server login and automatically sends `/login` when prompted.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Minecraft-1.21.11-8b5cf6?style=for-the-badge" alt="Minecraft 1.21.11">
  <img src="https://img.shields.io/badge/Loader-Fabric-6366f1?style=for-the-badge" alt="Fabric">
  <img src="https://img.shields.io/badge/License-MIT-a78bfa?style=for-the-badge" alt="MIT License">
</p>

<p align="center">
  <a href="../../releases/latest">Download LoginX</a> ·
  <a href="../../issues">Report an issue</a>
</p>

---

## Overview

LoginX automates the repetitive login process on cracked/offline-mode Minecraft servers that use AuthMe-style authentication plugins.

Instead of manually entering `/login <password>` every time you join, LoginX remembers the password you set and sends the login command when the server prompts you.

## Features

- **Automatic login** — Sends `/login` with your saved password when prompted.
- **Registration detection** — Supports common `/register <password> <password>` and `/register <password>` formats.
- **Chat and actionbar detection** — Can detect login prompts shown in chat, titles, or actionbars.
- **Multiple accounts** — Keeps separate saved logins for different Minecraft accounts on the same server.
- **In-game management** — Add, edit, or remove saved logins through the LoginX panel on the Multiplayer screen.
- **Encrypted password storage** — Uses AES-256-GCM encryption before writing saved passwords to disk.

## Compatibility

| Component | Requirement |
|---|---|
| Minecraft Java Edition | 1.21.11 only |
| Mod loader | Fabric |
| Fabric API | Required |
| Installation | Client-side |

Install a Fabric API release compatible with Minecraft 1.21.11.

## Installation

1. Install [Fabric Loader](https://fabricmc.net/use/installer/) for Minecraft 1.21.11.
2. Download a compatible [Fabric API version](https://modrinth.com/mod/fabric-api).
3. Download the LoginX `.jar` from [GitHub Releases](../../releases/latest).
4. Place both JAR files in your Minecraft `mods` folder.
5. Launch the Fabric profile for Minecraft 1.21.11.

## How to use

1. Join your server and register using the command required by that server, commonly `/register <password> <password>`.
2. LoginX detects supported registration prompts and saves the password you enter.
3. On future joins, LoginX can automatically send `/login <password>` when a supported login prompt appears.
4. To manage saved logins manually, open the Multiplayer screen and select the LoginX button.

Server plugins may use different commands or prompt wording, so automatic detection can vary between servers.

## Security and privacy

LoginX encrypts saved passwords using AES-256-GCM before writing them to disk. Passwords are not intentionally stored as plain text.

Encryption does not eliminate every security risk. Protect your operating-system account and Minecraft files, and only use LoginX on servers you trust. Never share your server passwords or your local game files with strangers.

## Important

LoginX is a client-side convenience mod. It does not bypass Mojang/Microsoft authentication or grant access to accounts or servers without valid credentials. It automates a server login command using a password you already know.

## License

LoginX is licensed under the MIT License. See [LICENSE](LICENSE) for details.
