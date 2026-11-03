<div align="center">

# ✦ Guild Board

**Your Genshin day on one board.**

A calm companion for Genshin Impact that sits beside the game on your desktop, keeps track of everything you would otherwise keep in your head, and never touches the game itself.

[![Latest release](https://img.shields.io/github/v/release/QL1STY/guild-board-releases?style=for-the-badge&color=a6751f&labelColor=3b4255&label=latest)](https://github.com/QL1STY/guild-board-releases/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/QL1STY/guild-board-releases/total?style=for-the-badge&color=a6751f&labelColor=3b4255)](https://github.com/QL1STY/guild-board-releases/releases)
[![Open source, MIT](https://img.shields.io/badge/open%20source-MIT-a6751f?style=for-the-badge&labelColor=3b4255)](https://github.com/QL1STY/guild-board)
![Windows 10 and 11](https://img.shields.io/badge/Windows-10%20%7C%2011-a6751f?style=for-the-badge&labelColor=3b4255)

### [⬇ Download the installer](https://github.com/QL1STY/guild-board-releases/releases/latest) · [▶ Try it in your browser](https://ql1sty.github.io/guild-board/demo/) · [Website](https://ql1sty.github.io/guild-board/)

<sub>Free · no ads, no account needed · about 160 MB · no administrator rights · updates itself · your data stays on your PC</sub>

<br>

<img src="https://ql1sty.github.io/guild-board/shots/board.png" alt="The Guild Board dashboard on a made-up account: timers, commissions, resin, resets, expeditions, pinned achievements, a clock and notes" width="900">

<sub>The Board, on a made-up account. Every card is a widget you can move, resize, add or remove.</sub>

</div>

<br>

This repository holds Guild Board's installers. The source code is at **[QL1STY/guild-board](https://github.com/QL1STY/guild-board)**, under the MIT licence.

## New in 1.0.0

- **Open source.** The whole app is public, and so are the tests that check its promises.
- **Import without the game.** Import reads your wishes and the game's history with your HoYoLAB login, so you no longer open Wish History or Feedback in the game first.
- **Freshness at a glance.** Characters, Pulls and Ledger show one small ring that tells you how fresh the data is and that it updates by itself.
- **A clearer Characters bar**, with a switch between a character's Profile and Planner.
- **Friends see less.** They see only whether you are in game and for how long, never that Guild Board is open or when your PC is on.
- **Smooth animations** at your monitor's full rate, if you switch them on, and Discord sign-in without an e-mail address.

## What it does

### 🧭 The Board: your day at a glance

Widgets for **timers**, **today's commissions**, **Resin** and when it is full, **daily and weekly resets**, **expeditions**, **pinned achievements**, **notes**, a **clock** on server time, a **quick timer**, the **daily check-in** and six for your pulls. When something is ready you get a **Windows notification**, and while you play, a short line over the game.

### ✦ Pulls: pity, savings and a plan

Your wish history, the **pity** of every banner, your **luck** against a typical player, a **savings ledger** of the pulls you hold and the ones the next version gives, and a **planner** that says how likely you are to get the characters you want.

<p align="center"><img src="https://ql1sty.github.io/guild-board/shots/pulls.png" alt="The Pulls page: the banners running now, the pity of each banner, the savings ledger and the planner" width="860"></p>

### 🏆 Achievements

The full list with progress counters, stages and **pins**, a "look it up" link on every card, and a check for new achievements from Paimon.moe's public list when you ask. The primogems still to earn are counted for you.

<p align="center"><img src="https://ql1sty.github.io/guild-board/shots/achievements.png" alt="The Achievements page: categories on the left, achievement cards with their progress on the right" width="860"></p>

### 📊 Stats and the Ledger

Chests, achievements, play time, days played and primogems, each against the period before. There is a **play-time calendar**, **when you play** by the hour, and **primogems by source**. The **Ledger** keeps the game's own history of primogems, crystals, resin and artifacts.

<p align="center"><img src="https://ql1sty.github.io/guild-board/shots/stats.png" alt="The Stats page: summary tiles, a play-time calendar and charts of primogems and play time" width="860"></p>

### 🗡 Characters

A page for every character you own, built from your account: stats, weapon, artifacts with what to keep or replace, talents and constellations. A **planner** works out what each one needs for the levels you choose.

### 🖥 The overlay

Press **Ctrl+Alt+G** and a panel of your widgets appears over the game. Press it again and it is gone. It is a window of Guild Board's own, laid over the screen, not a hook into the game.

<p align="center"><img src="https://ql1sty.github.io/guild-board/shots/overlay.png" alt="The overlay open over the game's screen, with a quick timer, timers, commissions and a clock" width="860"></p>

### 🔧 And the rest

- **Backlog**: every region and area with what is left to explore, the missing oculi, and open Archon Quests.
- **The interactive map**: HoYoLAB's official Teyvat map inside Guild Board, in tabs you can name and keep.
- **Gift codes**: redeem one or several, with a note when a new livestream code appears. A code is redeemed only when *you* press the button.
- **Friends**: optional, with a Discord sign-in. Compare stats and see who is in game.
- **Screenshot gallery**, **backups** you can move to another PC, **start with Windows**, and a **What's new** card after every update.

<br>

## Hands off the game

Guild Board is built around a short list of promises. They are written into its [tests](https://github.com/QL1STY/guild-board/blob/main/tests/test_handsoff.py), and the tests fail if the code ever breaks one.

| It never | |
|---|---|
| **touches the game's files or settings** | It never writes there. It reads the game's log and the history links in its web cache only when you press **Import** and your HoYoLAB login cannot be used for it. |
| **touches the game's process** | No handle, no memory, no hooks, no injection. All it learns is *whether the game is running*, from the Windows process list. |
| **sends input to the game, or captures its screen** | The overlay is a separate window, not a layer inside the game. |
| **talks to anyone it does not need** | `hoyolab.com`, `hoyoverse.com` and `mihoyo.com`, plus Paimon.moe's public achievement list when you ask, this repository to look for updates, and, only if you sign in to Friends, Guild Board's own server. |
| **changes your account** | It reads. The two exceptions happen only when *you* press the button: redeeming a gift code, and claiming the daily check-in reward. |

Your HoYoLAB login is stored **only on your PC**, encrypted for your Windows user. It is never written to a log or a backup, and it is never sent anywhere but HoYoverse.

<br>

## Getting started

1. **[Download the installer](https://github.com/QL1STY/guild-board-releases/releases/latest)** (`Guild.Board.Setup.<version>.exe`) and run it. No administrator rights are needed.
2. **Read the first-run page.** It lists exactly what is read and what is never done, and asks you to acknowledge the risk below.
3. **Log in to HoYoLAB** in Guild Board's own window, or choose **demo data** to look around first.
4. Wait for the first sync, and the Board fills in.

> Guild Board is not code-signed by Windows yet, so SmartScreen may ask you to confirm on first run. Choose **More info → Run anyway**. To check the installer first, compare its SHA-256 with the one on the release page, or run `gh attestation verify "Guild.Board.Setup.<version>.exe" --repo QL1STY/guild-board`, which shows the exact commit of the source that GitHub built it from.

**Updating** is automatic. Guild Board looks here twice a day and offers the new version with one button. It installs only an update that carries the release key's signature. An update or an uninstall leaves your data alone.

<br>

## An honest word about risk

Guild Board reads your account through HoYoLAB with your own login. That is low-risk, but **not zero-risk**. Any third-party access is technically against HoYoverse's Terms of Service, and if action were ever taken, it would plausibly be against the HoYoLAB account rather than the game account. The developer of the most widely used tool of this kind says that no user has ever reported a ban. Guild Board only reads, apart from the two presses above. It keeps your login encrypted, and it shows you all of this before it does anything.

<br>

## Questions

<details>
<summary><b>Is it a cheat or a bot?</b></summary>

No. It does not read or change the game's memory, does not send input, does not capture the screen and does not change a single file in the game's folder. It reads your HoYoLAB data and your wish and game histories, which HoYoverse lets your login read.
</details>

<details>
<summary><b>Which servers does it work with?</b></summary>

It is built for the global servers and HoYoLAB. Other regions are untested.
</details>

<details>
<summary><b>Can it log in to the game, or change my password?</b></summary>

No. The saved HoYoLAB login cannot log in to the game, change your password or show your email address.
</details>

<details>
<summary><b>Where is my data?</b></summary>

In a folder of your own on your PC (`%LOCALAPPDATA%\GuildBoard`). Nothing is uploaded unless you sign in to Friends. What that sends, and what it never sends, is in the [privacy notice](https://github.com/QL1STY/guild-board/blob/main/PRIVACY.md). Use **Settings → Backups** to move your data to another PC.
</details>

<details>
<summary><b>Something is wrong, or I have an idea.</b></summary>

Open an [issue](https://github.com/QL1STY/guild-board/issues) in the source repository. Mention your version from **Settings → About**, and what you expected to happen.
</details>

<br>

<div align="center">

<sub>Guild Board is an unofficial, fan-made tool. It is not affiliated with, endorsed by or connected to HoYoverse or COGNOSPHERE. Genshin Impact, HoYoLAB and Teyvat are trademarks of their owners. Screenshots show a made-up account, not a real one.</sub>

</div>
