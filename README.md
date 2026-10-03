# Achievement Display

**English** | [繁體中文](README.zh-TW.md)

A small custom achievement system: when a player takes a parkour reward item they unlock an achievement, announced with a server-wide title, chat broadcast, sound and a DiscordSRV message.

> This repository has two editions of the same script: **繁體中文 (zh-TW)** is the original used on the author's Traditional Chinese server, and **English** is a full translation (commands, messages and variable names) with the same features.

## Features

- Two parkour achievements, each unlocked once per player
- Title + toast sound for everyone online, a chat broadcast and a Discord broadcast
- `/achievements` lists what a player has unlocked
- Admin commands to grant or reset achievements
- Reusable `showAchievement(player, title, description)` function for your own achievements

## Requirements

- [Paper](https://papermc.io/) server (developed on Paper 26.2 / Minecraft 26.2)
- [Skript](https://github.com/SkriptLang/Skript) (developed on 2.16.2)
- [DiscordSRV](https://github.com/DiscordSRV/DiscordSRV) (optional, for the Discord announcement)

## Installation

1. Install the plugins listed under [Requirements](#requirements).
2. Download **one** edition:

   | Edition | File(s) |
   |---|---|
   | English | [`en/achievement-display.sk`](en/achievement-display.sk) |
   | 繁體中文 (original) | [`zh-TW/成就顯示.sk`](zh-TW/%E6%88%90%E5%B0%B1%E9%A1%AF%E7%A4%BA.sk) |

3. Copy the `.sk` file(s) into `plugins/Skript/scripts/` on your server.
4. Run `/sk reload achievement-display` (use the file name you copied) or restart the server.

> [!IMPORTANT]
> Install **only one** edition. Both editions are the same script in different languages - loading both makes them clash or run twice.

## Commands

| Command (English edition) | zh-TW edition | Description | Permission |
|---|---|---|---|
| `/achievements`<br>alias: `/achievement` | `/成就`<br>aliases: `/achievement` | Show your achievements | everyone |
| `/resetachievements <player>` | `/重置成就 <玩家>` | Reset a player's achievements | OP |
| `/giveachievement <player> <id>` | `/給予成就 <玩家> <成就ID>` | Grant `parkour.beginner` or `parkour.master` | OP |

## Configuration

- Achievements are unlocked by clicking the reward items of [skript-parkour-reward-chest-refill](https://github.com/Im-Tim-mI/skript-parkour-reward-chest-refill): a compass named `§bParkour Adept` and a nether star named `§bParkour Expert` (zh-TW edition: `§b跑酷能手`, `§b跑酷高手`). Rename them in both scripts together.

## Notes

- Without DiscordSRV the `discord broadcast` console command simply fails; delete that line if you don't use DiscordSRV.
- Progress is stored in `{achievement.parkour.*::<uuid>}`, the same in both editions.

## Related projects

- [skript-parkour-reward-chest-refill](https://github.com/Im-Tim-mI/skript-parkour-reward-chest-refill) - Parkour Reward Chest Refill
- [skript-special-item-lock](https://github.com/Im-Tim-mI/skript-special-item-lock) - Special Item Lock

## License

**MIT + Commons Clause** - see [LICENSE](LICENSE) for the full text.

- ✅ You may use, copy, modify and share this script.
- ✅ You **may** install and run it - including modified versions - on Minecraft servers that charge money or are run for profit.
- ❌ You may **not** sell the script itself or modified versions of it, directly or indirectly, or require payment to obtain its files or source code.

Copyright (c) 2026 廷廷小教室、廷廷的家（Tim945）
