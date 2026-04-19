<div align="center">

<img src="your-aegis-logo-url-here" alt="Aegis Logo" width="120" height="120" style="border-radius: 50%;"/>

# Aegis — Bot

**The core Discord bot powering Aegis. 🛡️**

[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Bun](https://img.shields.io/badge/Bun-latest-fbf0df?style=for-the-badge&logo=bun&logoColor=black)](https://bun.sh)
[![Seyfert](https://img.shields.io/badge/Seyfert-latest-5865F2?style=for-the-badge)](https://github.com/tiramisulabs/seyfert)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-16-336791?style=for-the-badge&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

[![Discord](https://img.shields.io/badge/Support_Server-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/3SzpJEXUcV)
[![Invite Aegis](https://img.shields.io/badge/Invite_Aegis-57F287?style=for-the-badge&logo=discord&logoColor=white)](https://discord.com/oauth2/authorize?client_id=1495395864833949767)

</div>

---

## 📖 About

This repository contains the core bot for **Aegis** — a powerful, all-in-one Discord moderation bot. Built with TypeScript, Seyfert, and Bun for maximum performance and type safety.

---

## ✨ Features

- 🔨 **Moderation** — Ban, kick, warn, mute & timeout with full audit trails
- 🛡️ **Anti-Nuke** — Real-time detection of mass bans, channel deletions, and permission abuse
- 🤖 **Automod** — Smart spam, link, invite, caps & bad word filtering
- 📋 **Logging** — Detailed logs for every action in your server
- 🎵 **Music** — High quality music playback with queue management
- 📣 **YouTube Alerts** — Notifications for new videos, shorts & livestreams
- 🖥️ **Dashboard Integration** — Fully manageable via the Aegis web dashboard

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Language | TypeScript |
| Runtime | Bun |
| Bot Framework | Seyfert |
| Database | PostgreSQL |
| ORM | Drizzle |

---

## 🚀 Getting Started

### Prerequisites

- [Bun](https://bun.sh) `>= 1.0`
- [PostgreSQL](https://www.postgresql.org/) `>= 15`
- A [Discord Application](https://discord.com/developers/applications) with a bot token
- A [YouTube Data API v3](https://console.cloud.google.com/) key

### Installation

1. **Clone the repository**

```bash
git clone https://github.com/your-org/bot.git
cd bot
```

2. **Install dependencies**

```bash
bun install
```

3. **Set up environment variables**

```bash
cp .env.example .env
```

Fill in your `.env` file:

```env
# Discord
DISCORD_TOKEN=your_bot_token_here
DISCORD_CLIENT_ID=your_client_id_here
DISCORD_CLIENT_SECRET=your_client_secret_here

# Database
DATABASE_URL=postgresql://user:password@localhost:5432/aegis

# YouTube
YOUTUBE_API_KEY=your_youtube_api_key_here
```

4. **Push the database schema**

```bash
bun run db:push
```

5. **Start the bot**

```bash
# Development
bun run dev

# Production
bun run start
```

---

## 📁 Project Structure

```
bot/
├── src/
│   ├── commands/
│   │   ├── moderation/     # ban, kick, warn, mute, timeout
│   │   ├── antinuke/       # antinuke configuration
│   │   ├── music/          # play, queue, skip, stop, etc.
│   │   ├── notifications/  # youtube alert setup
│   │   └── utility/        # ping, help, info
│   ├── events/             # Discord gateway event handlers
│   ├── lib/
│   │   ├── antinuke/       # Anti-nuke detection logic
│   │   ├── automod/        # Automod engine
│   │   ├── music/          # Music player logic
│   │   └── youtube/        # YouTube polling & notifications
│   ├── db/
│   │   ├── schema.ts       # Drizzle schema definitions
│   │   └── index.ts        # Database client
│   └── index.ts            # Bot entry point
├── .env.example
├── drizzle.config.ts
├── package.json
└── tsconfig.json
```

---

## 💬 Commands

### Prefix: `$`

**Moderation**

| Command | Description |
|---|---|
| `$ban @user [reason]` | Ban a member |
| `$kick @user [reason]` | Kick a member |
| `$warn @user [reason]` | Warn a member |
| `$mute @user [duration]` | Mute a member |
| `$timeout @user [duration]` | Timeout a member |
| `$warnings @user` | View a member's warnings |

**Music**

| Command | Description |
|---|---|
| `$play [song]` | Play a song |
| `$queue` | View the music queue |
| `$skip` | Skip the current song |
| `$stop` | Stop music and clear queue |
| `$volume [1-100]` | Adjust the volume |
| `$lyrics` | Show lyrics for the current song |

> All commands are also available as Discord slash commands.

---

## 🤝 Contributing

Contributions are welcome! Please open an issue first to discuss what you'd like to change.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📜 Legal

- [Terms of Service](https://gist.github.com/AlexxDevvz/941b3e36ceef8e0d198103f2a3a4b9f1)
- [Privacy Policy](https://gist.github.com/AlexxDevvz/31f2487e97426e6f60dce0f862660fd5)

---

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

<div align="center">

*Built with ❤️ by the Aegis team*

</div>
