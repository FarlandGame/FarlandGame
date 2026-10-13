# Bardiya Alizadeh · Farland_game

[English](https://github.com/FarlandGame) | [日本語](https://github.com/FarlandGame/FarlandGame/blob/main/docs/README.ja.md) | [فارسی](https://github.com/FarlandGame/FarlandGame/blob/main/docs/README.fa.md)

I'm **Bardiya Alizadeh**, also known as **Kabir** and **Farland_game**. This page brings together my software projects and creative work.

## Featured work

### [Vexland_Manhunt](https://github.com/FarlandGame/Vexland_Manhunt)

**A complete Minecraft Runner-versus-Hunter experience, co-created by [Bardiya Alizadeh (Kabir) · Farland_game](https://github.com/FarlandGame) and [Ali · Alivexor](https://github.com/Alivexor).**

Vexland_Manhunt brings match setup, team roles, the opening chase, tracking, progression, rewards, results, and administration into one Paper server plugin. Runners try to defeat the Ender Dragon while Hunters try to eliminate the final Runner. The plugin supports multiple Runners and keeps the chase moving through deaths, respawns, dimension changes, and reconnects. Its `/mhgui` control center lets administrators manage a match through menus, with localized messages and guidebooks for the players.

#### Downloads and compatibility

| Plugin release | Download | Target environment |
| --- | --- | --- |
| **1.9.11** — current supplied build | [VexLandManhunt-1.9.11-.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.9.11/VexLandManhunt-1.9.11-.jar) | Paper **1.21.11**, Java **21** |
| **1.6.4** — earlier build | [VexLandManhunt-1.6.4.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.6.4/VexLandManhunt-1.6.4.jar) | Paper **1.21.11**, Java **21** |

**1.6.4 and 1.9.11 are plugin version numbers.** Both supplied builds declare Minecraft API `1.21.11` and Java 21 class files. These are server plugins for Minecraft Java Edition. [Paper's version-specific Java requirements](https://docs.papermc.io/paper/getting-started/) also list Java 21 for Paper 1.21.11. No additional plugin dependency is declared in the supplied descriptors.

These are **original personal-server builds with creator-specific elevated administrative access**, preserved exactly as supplied. The guide below covers the public Manhunt controls.

#### The Manhunt experience

- **Runner and Hunter teams:** assign online players to either side. A match needs at least one Runner and a Hunter or an unassigned online player. Surviving Runners continue if a teammate dies; a fallen Runner becomes a Hunter unless that death ends the match.
- **Cinematic match start:** inventories and game modes are prepared, teams are introduced, and a roulette chooses the Runner head start. Hunters are frozen during that countdown, with title and sound feedback. The head start is randomized; administrators can release Hunters early.
- **Target-selecting tracker compass:** Hunters receive a special compass. Right-click it to choose a Runner from the target menu and change the target during the chase. Across dimensions, tracking follows the relevant portal route until direct tracking becomes possible. Hunters receive their tracker again after respawning.
- **Progress displays:** bossbars and match information follow Runner equipment and progression through Nether resources, blaze rods, pearls, Eyes of Ender, the stronghold, and the End. The newer build adds finer stages and dragon-health-aware progress visuals.
- **Rewards for Runner kills:** when a Runner kills a Hunter during an active match, a progression-aware weighted reward pool of 50 entries is used. Animated rolls, double/triple rewards, streak announcements, and rare-item celebrations are included.
- **Victory and results:** the final Runner's death gives Hunters victory; defeating the Ender Dragon gives Runners victory. Match-end titles, celebrations, kill/death information, and temporary-item cleanup are included. The newer build also reports MVP, damage, and distance results.
- **Team communication and utilities:** private teammate messages with `/teammsg`, a 54-slot disposable trash inventory with `/trash`, and personal night vision with `/nv`.
- **Administration through menus:** roles, start/reset, early Hunter release, friendly fire, server lock, teleport-all, heal/feed, language, protection settings, status, and guidebooks are available through the control center. Freezing and a full reset help prepare the next match.
- **Localized guides:** Runner, Hunter, and administrator books explain objectives, tracker use, deaths, setup, and commands. Version 1.9.11 gives players a role-aware guide through `/mhhelp`.
- **Paper Anti-Xray integration:** menu controls configure Paper's world-level protection; changes need a server restart to take effect.

#### What is new in 1.9.11?

These changes were identified by comparing the two supplied builds, including their metadata, message resources, and compiled classes.

| Addition or change | Behavior in 1.9.11 |
| --- | --- |
| **Smart Hunter Kit V3** | Adaptive respawn kits consider Runner equipment, teams, and match context. The system aims to keep Hunter kits below the Runner equipment average and can be toggled with `/mhkit` or the GUI. |
| **Automatic Overworld Spawn** | Move world spawn near an eligible Overworld Runner at a chosen interval: off, 5, 10, 15, 20, or 30 minutes. The system selects a safe surface candidate and skips unsuitable cases. |
| **Pause and resume** | `/mhpause` freezes gameplay and match-related timers, tracking, and spawn movement; `/mhresume` continues. Paused time is offset from active match timing. |
| **Restart/crash recovery** | A recovery layer restores match state, roles, tracker targets, progress, reward/death timers, and reconnect state using primary/backup snapshots, periodic saves, and shutdown saves. |
| **Runner reconnect settings** | A configurable reconnect window replaces the earlier fixed 60-minute window. Fresh default: 15 minutes, with 10 seconds of rejoin protection. Server downtime is excluded; expiry can convert the Runner to a Hunter or finish the match. |
| **Expanded administration** | Change roles during a live match while preserving the final Runner; selected-player actions, team teleport/freeze, runtime resynchronization, and shortcuts improve match management. |
| **Confirmed settings reset** | Two clicks within eight seconds apply Smart Kit ON, auto spawn every 15 minutes, and reconnect 15 minutes. This differs from a fresh installation's auto-spawn OFF default. |
| **VexAC 3.0** | Movement, combat, AutoClick, velocity/knockback, and world-building checks; group/master controls, evidence logging, administrator alerts, and environment/lag exemptions. |
| **Ultra Deep Debug v4** | `/mhdebug` provides state-machine, GUI, synthetic kit/stress, language-placeholder, recovery round-trip, and integrity diagnostics. |
| **Expanded displays** | More progression detail, dragon-health visuals, MVP/damage/distance results, and TAB ping information. |
| **Command changes** | Adds `/mhkit`, `/mhspawn`, `/mhpause`, `/mhresume`, and `/mhdebug`; removes `/mhnone`; makes `/mhhelp` player/admin aware and adds `/trash` aliases. |
| **More localized messages** | Translation resources expand from 446 message keys per language to 683. |

VexAC's packaged checks cover Fly, Speed, Timer, Phase, Step, NoSlow, GroundSpoof, Reach, KillAura, AimAssist, wall-hit, BadPackets, AutoClick timing patterns, altered knockback, Scaffold, Tower, FastPlace, Nuker, and block reach. Its UI uses a monitor-only label, while compiled code also contains kick paths; confirm the actual moderation behavior on a test server before relying on that label. The earlier build contains legacy Anti AutoClick and Anti Fly controls instead.

#### Start using `/mhgui`

1. Install one supplied JAR on a Paper 1.21.11 / Java 21 server and restart fully.
2. Join as a trusted OP and run **`/mhgui`**.
3. Open **Player Roles** and click participant heads to assign at least one Runner and Hunter.
4. Review **Friendly Fire**, **Language**, **Smart Hunter Kit** and **Auto World Spawn**; switch off **Server Freeze**.
5. Click **Start Match**. Hunters right-click their compass to choose a Runner after release.
6. Use Pause/Resume in 1.9.11 or Reset Match to prepare another round.

**[Read the complete GUI guide and command reference](https://github.com/FarlandGame/Vexland_Manhunt#full-setup-and-use-with-mhgui)**

#### A playful challenge to Dream

A little Minecraft banter from Bardiya 😄

> "Sigh... Ali and I made a Manhunt plugin a hundred times better than Dream's, but Dream's scared and won't play ours!"

**Documentation languages (18):**

[English](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/README.md) · [日本語](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.ja.md) · [فارسی](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.fa.md) · [Deutsch](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.de.md) · [Français](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.fr.md) · [Español](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.es.md) · [Português (Brasil)](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.pt-BR.md) · [Italiano](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.it.md) · [Nederlands](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.nl.md) · [Polski](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.pl.md) · [Українська](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.uk.md) · [Türkçe](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.tr.md) · [Русский](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.ru.md) · [简体中文](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.zh-CN.md) · [繁體中文](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.zh-TW.md) · [한국어](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.ko.md) · [हिन्दी](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.hi.md) · [Bahasa Indonesia](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.id.md)

### [Farland_autcliker](https://github.com/FarlandGame/Farland_autcliker)

<!-- APP_DOCUMENTATION -->
**Documentation languages (18):**

[English](https://github.com/FarlandGame/Farland_autcliker/blob/main/README.md) · [日本語](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.ja.md) · [فارسی](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.fa.md) · [Deutsch](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.de.md) · [Français](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.fr.md) · [Español](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.es.md) · [Português (Brasil)](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.pt-BR.md) · [Italiano](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.it.md) · [Nederlands](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.nl.md) · [Polski](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.pl.md) · [Українська](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.uk.md) · [Türkçe](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.tr.md) · [Русский](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.ru.md) · [简体中文](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.zh-CN.md) · [繁體中文](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.zh-TW.md) · [한국어](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.ko.md) · [हिन्दी](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.hi.md) · [Bahasa Indonesia](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.id.md)

**[Download for Windows](https://github.com/FarlandGame/Farland_autcliker/releases/latest/download/Farland_autcliker.zip)** · [Explore the source code](https://github.com/FarlandGame/Farland_autcliker) · [日本語の説明](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.ja.md) · [توضیحات فارسی](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.fa.md)

Farland_autcliker is a Windows desktop application created by **Bardiya Alizadeh (Kabir), known as Farland_game**. Its defining feature is the way automation begins: **each physical mouse click starts its own one-second burst of additional clicks**. It is designed for people who want to decide when a burst starts through their own mouse input, while controlling the left and right buttons independently. The application combines this behavior with a Persian interface, customizable controls, saved preferences, and a ready-to-run Windows executable.

#### How your clicks become additional clicks

Enable the clicker, then click the left or right mouse button. The original physical click is delivered normally, and the program schedules additional clicks for that same button over the following second. For example, with the left side set to **20 CPS**, one physical left click schedules **20 additional left clicks**. Including the physical click, that interaction requests 21 clicks in total, subject to the target application's input handling.

A second physical click starts another burst, even if the first is still running. Two such left clicks schedule 40 additional clicks across their overlapping one-second windows. This means the setting describes **each individual burst**, rather than a global limit on all overlapping activity. When no new physical clicks occur, no new bursts are created; already scheduled bursts continue until they finish or you stop the clicker.

#### What makes the workflow different

A familiar [repeat-until-stopped workflow](https://www.opautoclicker.com/) runs a repeated sequence after activation. Farland_autcliker's distinction is **physical-click-triggered bursts**, with separate settings for each side.

| Interaction | Repeat-until-stopped workflow | Farland_autcliker |
| --- | --- | --- |
| Start additional clicks | Start the repeat sequence | Activate, then physically click |
| A new physical click | Not needed to keep repetition running | Starts its own additional burst |
| End a sequence | Stop the repeat sequence | Each burst completes its one-second schedule |

This comparison describes two workflows; individual auto clickers can offer additional modes. Farland's documented strengths are its trigger behavior and independent controls.

#### Independent left and right control

Set a different rate for each button, from **1 to 10,000 CPS**, and enable either side separately. For instance, you can configure 20 CPS on the left and 8 CPS on the right: a left click starts its left-button burst, while a right click starts an independent right-button burst. Disabling one side leaves that side's physical clicks working normally without creating new additional clicks.

#### Controls that fit your setup

Toggle activation with the main interface button or a chosen global hotkey: the middle mouse button, either side mouse button, F6–F9, Home, End, or Insert. **F12** provides an emergency stop and exits the application. Four themes—dark, light, purple, and blue—let you choose the appearance. Click rates, enabled sides, the hotkey, and the theme are saved for the next session. Invalid click-rate entries return to the previous valid value.

#### Handling repeated input carefully

The engine distinguishes physical mouse input from Windows-injected clicks, so its own generated clicks do not start new bursts. A scheduler manages overlapping bursts and sends high-rate clicks in small batches. **10,000 CPS is the configurable ceiling, not a measured speed guarantee**: actual delivery depends on the computer, Windows input processing, and the target application.

#### Download and explore

The public Windows ZIP includes the executable, source code, an interface preview, and English, Japanese, and Persian documentation. Extract it and open `Farland-Auto-Clicker/dist/Farland Auto Clicker.exe`; the packaged executable does not need a separate Python installation. The source targets Windows 10 or 11 and Python 3.10 or later, using Tkinter and the Windows API. The repository also includes six tests for scheduling, overlapping sides, cancellation, hotkeys, and injected-input filtering; they use simulated clicks.

**Built with:** Python · Tkinter · Windows API · PyInstaller

## Find me

### Channels and social links

| Platform | Channels / pages |
| --- | --- |
| GitHub | [FarlandGame](https://github.com/FarlandGame) |
| YouTube | [Farland_game](https://www.youtube.com/@Farland_game) · [Farland_animation](https://www.youtube.com/@Farland_animation) |
| Rubika channels | [farland_gam](https://rubika.ir/farland_gam) · [Farland_animatio](https://rubika.ir/Farland_animatio) |
| Rubika pages | [farland_game](https://rubika.ir/farland_game) · [Farland_animations](https://rubika.ir/Farland_animations) |
| Instagram | [farland_game](https://www.instagram.com/farland_game/) |
| Telegram channels | [Farland_gam](https://t.me/Farland_gam) · [Farland_animatio](https://t.me/Farland_animatio) |
| Twitch | [farlandgame](https://twitch.tv/farlandgame) |
| Kick | [farlandgame](https://kick.com/farlandgame) |
| Aparat | [Farland_Game](https://aparat.com/Farland_Game) |
| SoundCloud | [Bardiya Kabir](https://soundcloud.com/bardiya-kabir-798008614) |

### Telegram music bot

[Farland Music Bot](https://t.me/Farland_Music_bot) — Send a song's video link to our Telegram bot to find the track.

### Community and family

- **THE APEX:** [YouTube](https://www.youtube.com/@THE_APEX_MC) · [Telegram](https://t.me/+-3uY7eIZArVjZDE0)
- **Manhunt:** [Telegram group](https://t.me/+DAq20XrkPyZhNjVk)
- **My brother's channel:** [ArmiyaFabix on YouTube](https://www.youtube.com/@ArmiyaFabix)

### Support my work

[Donate via Reymit](https://reymit.ir/farland_game) ❤️
