# Bardiya Alizadeh · Farland_game

[English](https://github.com/FarlandGame) | [日本語](https://github.com/FarlandGame/FarlandGame/blob/main/docs/README.ja.md) | [فارسی](https://github.com/FarlandGame/FarlandGame/blob/main/docs/README.fa.md)

I'm **Bardiya Alizadeh**, also known as **Kabir** and **Farland_game**. This page brings together my software projects and creative work.

## Featured work

### [Farland Auto Clicker](https://github.com/FarlandGame/Farland-Auto-Clicker)

**[Download for Windows](https://github.com/FarlandGame/Farland-Auto-Clicker/releases/latest/download/Farland-Auto-Clicker.zip)** · [Explore the source code](https://github.com/FarlandGame/Farland-Auto-Clicker) · [日本語の説明](https://github.com/FarlandGame/Farland-Auto-Clicker/blob/main/docs/README.ja.md) · [توضیحات فارسی](https://github.com/FarlandGame/Farland-Auto-Clicker/blob/main/docs/README.fa.md)

Farland Auto Clicker is a Windows desktop application created by **Bardiya Alizadeh (Kabir), known as Farland_game**. Its defining feature is the way automation begins: **each physical mouse click starts its own one-second burst of additional clicks**. It is designed for people who want to decide when a burst starts through their own mouse input, while controlling the left and right buttons independently. The application combines this behavior with a Persian interface, customizable controls, saved preferences, and a ready-to-run Windows executable.

#### How your clicks become additional clicks

Enable the clicker, then click the left or right mouse button. The original physical click is delivered normally, and the program schedules additional clicks for that same button over the following second. For example, with the left side set to **20 CPS**, one physical left click schedules **20 additional left clicks**. Including the physical click, that interaction requests 21 clicks in total, subject to the target application's input handling.

A second physical click starts another burst, even if the first is still running. Two such left clicks schedule 40 additional clicks across their overlapping one-second windows. This means the setting describes **each individual burst**, rather than a global limit on all overlapping activity. When no new physical clicks occur, no new bursts are created; already scheduled bursts continue until they finish or you stop the clicker.

#### What makes the workflow different

A familiar [repeat-until-stopped workflow](https://www.opautoclicker.com/) runs a repeated sequence after activation. Farland Auto Clicker's distinction is **physical-click-triggered bursts**, with separate settings for each side.

| Interaction | Repeat-until-stopped workflow | Farland Auto Clicker |
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
