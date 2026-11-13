# Vavoo Stream – Android

**Android app by Qu4k3** · ![version](https://img.shields.io/badge/version-1.3.7-8b3fd9) ![Android](https://img.shields.io/badge/Android-5.0%2B-3fdc8e) ![TV](https://img.shields.io/badge/Android%20TV-ready-5a8cff)

Live TV from Vavoo / Kool.to on your Android **phone, tablet and Android TV box** – a
complete TV app: preview window, programme guide, recordings, pause live TV, multi-view,
casting to your TV, parental control and four themes. Nothing to set up: open it and watch.

## Download

**[⬇ Download the latest VavooStream.apk](https://github.com/pQu4k3r/vavoo_android-releases/releases/latest)**

1. Open the latest release and download `VavooStream.apk`.
2. Open the file on your device and allow "install unknown apps" for your browser or file manager.
3. Android 5.0 or newer. Works with touch and with TV remotes (D-pad and colour keys).

The app checks for new versions and offers the update itself (Settings → Check for updates).
You can also follow releases automatically with [Obtainium](https://github.com/ImranR98/Obtainium):
add `https://github.com/pQu4k3r/vavoo_android-releases`.

## How it works

- **Channels** – the app reads the channel list from geil.to (all countries), and from Vavoo's
  catalog (vavoo.to, then kool.to) when geil.to is blocked or down. A channel that exists
  several times (`.b`, `.c`, `.s`, HD, HEVC, RAW, backup…) is shown as **one row**; when one source
  fails the next one is tried by itself.
- **Token** – geil.to's streams need none. For Vavoo's, which give one stream per token and block
  anonymous viewers after a few minutes, the app gets its own signature and renews it in the
  background while you watch, record or cast, so streams don't stop after 10 minutes. Multi-view tiles, recordings, the Android TV input and casting each get a
  token of their own, so one never cuts another.
- **geil.to → vavoo.to → kool.to** – when one is blocked or doesn't answer, the next is used automatically.
  Optional **Secure DNS** for providers that block the names.
- **Player** – Media3 / ExoPlayer with FFmpeg audio built in: Dolby (AC-3, E-AC-3), DTS and MP2 play
  even on devices that can't decode them. Automatic reconnects.
- **Programme guide** – daily data from epgshare01.online (several days ahead, a GitHub copy as
  fallback), matched to the channels by their guide id from geil.to, then by name rules (country prefixes, HD/HEVC tags, accents, spaces,
  numbers) and curated channel maps.
- **Playlist server** – other players (TiviMate, VLC, Kodi) get the channels and the guide from
  `http://127.0.0.1:4323/playlist.m3u`; the links go through the app, which keeps the token fresh.

## Screenshots

Real screenshots (Android emulator, live channels from the Vavoo catalog).

| Main menu | Channels with the preview window (Halo theme) |
| --- | --- |
| ![Main menu](screen/main.jpg) | ![Channels](screen/channels.jpg) |
| **Numbered channel lists** | **Channel list and mini guide over the stream** |
| ![Channel numbers](screen/channel-numbers.jpg) | ![Mini guide](screen/mini-guide.jpg) |
| **Player options** | **Programme guide** |
| ![Options](screen/options.jpg) | ![Guide](screen/guide.jpg) |
| **Multi-view: 4 channels at once** | **Pause live TV, stream info** |
| ![Multi-view](screen/multiview.jpg) | ![Pause live TV](screen/pause-live.jpg) |
| **Recordings & timers** | **Parental control** |
| ![Recordings](screen/recordings.jpg) | ![Parental control](screen/parental.jpg) |
| **Orbit theme** | **Settings** |
| ![Orbit theme](screen/theme-orbit.jpg) | ![Settings](screen/settings.jpg) |

## What's new in 1.3

**1.3.7** – the **player's infobar with the D-pad**: with the infobar shown ◀ ▶ go along its buttons
(Back, Fav, CH-, CH+, Options, Cast, List, Recall) and OK presses one – ▲ ▼ still change the channel;
the bottom buttons also reachable from an empty list.

**1.3.6** – **remotes without colour keys** (Fire TV, TIM Box…): DOWN at the end of a list moves onto
the colour buttons, ◀ ▶ choose, OK presses; the update window with ◀ ▶ and OK; Favourite in the
player's options. The infobar shows the **channel's logo** when Channel Logos is on.

**1.3.5** – channels now come from **geil.to** (no token needed, a guide id with each channel),
with vavoo.to and kool.to as fallbacks; **channel logos are back** (Vavoo's old logo server had
stopped answering); favourites, recent channels and timers carry over by themselves; geil.to in
Settings → Server.

**1.3.4** – recordings follow a stream server that restarts its numbering; safer DLNA casting
(service stop, several connections, time limit); picture-in-picture in the right shape for anamorphic
streams; PIN pause never brought back after a reboot; Android TV setup counts only the channels the TV
took; a locked channel is never cast before its PIN; smoother screens.

**1.3.0 – 1.3.3**

- **Programme guide for many more channels**: fresh daily guide data (several days ahead),
  smarter channel matching, a guide for the Balkans and Arabia too. Italy, the UK, Turkey,
  Portugal, Romania… went from almost no guide to between a quarter and two thirds of their channels.
- **Search finds what's on**: type a team or a show and get the channels showing it now.
- **Receiver-style remote**: OK shows the infobar, OK again the channel list; BACK closes the
  infobar first. In the player options LEFT / RIGHT change a value, OK lists them all.
- **Infobar**: progress of the programme on now and its minutes left; typing a number shows the
  channel it goes to; **0** goes back to the previous channel.
- **Pause live TV** shows *Paused* / *-0:48* on screen; **Record** stops at the programme's end.
- Audio track list with the chosen language kept on the next channels, sleep-timer warning,
  Chromecast that keeps playing, and many fixes.

## Features

**Watching**
- All Vavoo countries with flags (choose which are shown); countries with groups open as folders.
- **Preview window** in the lists – full screen continues the same stream, no restart.
- **One row per channel**: its sources (`.b`, `.c`, `.s`) are tried by themselves when one fails.
- **Favourites** with folders and your own order, **recently watched**, **search** (also by voice).
- Numbered lists: the number keys go to a channel, in the lists and in the player.

**Programme guide**
- Now / next everywhere, a full **guide grid**, and a **mini guide** beside the player's list.
- **Reminders** and **recordings** set from the guide.

**Recordings and pause live TV**
- **Record** the channel you watch or set a timer in the guide – in the background, screen off.
- **Pause live TV** up to 2 hours, move back and forth, BACK to return to live.

**Picture and sound**
- **Dolby / DTS sound on every device** (decoded by the app when the device can't),
  **audio passthrough** to an AV receiver, **match frame rate** on Android TV.
- Video quality (automatic, best, or a limit), **data saver** on mobile data, stream info,
  picture format, pinch to zoom, audio and subtitle tracks, sleep timer.

**Multi-view** – up to 4 channels at once, the highlighted one with sound.

**Android TV and remotes** – colour keys, MENU, INFO / EPG, number keys, CH+/CH-, RECALL,
media keys; hold OK for a menu on remotes without colour keys. Your favourites in the TV's own
channel list and guide, "Play next" on the home screen, voice: *"Play Rai 1 on Vavoo Stream"*.

**Phones and tablets** – tap to preview, tap again for full screen; swipe to zap, brightness and
volume at the edges; landscape, portrait or auto; **picture-in-picture**, **background audio**.

**Cast to a TV** – **DLNA / UPnP smart TVs** (Samsung, LG, Sony, Philips…, Kodi, VLC) and
**Chromecast**; the phone is the remote and casting goes on with the screen off.

**Family and other players**
- **Parental control**: a PIN for adult channels, chosen countries and the settings.
- **Backup / restore** of settings, favourites, recently watched, countries and timers.
- **Playlist server** for TiviMate, VLC, Kodi (`http://127.0.0.1:4323/playlist.m3u`), with the guide.

**Looks** – four themes (Prism, Halo, Orbit, Classic), large text option, **16 languages**:
English, Italian, German, French, Spanish, Portuguese, Polish, Turkish, Romanian, Dutch, Russian,
Greek, Croatian, Albanian, Bulgarian, Arabic.

**Reliable** – vavoo.to ⇄ kool.to switching when one is blocked, optional Secure DNS, the Vavoo
token kept fresh while you watch or record, automatic reconnects.

## Remote control

| Key | In the lists | In the player |
| --- | --- | --- |
| OK | Preview, OK again: full screen | Infobar, OK again: channel list |
| Hold OK | Menu with the colour keys' actions | Options |
| UP / DOWN, CH+ / CH- | Move in the list | Next / previous channel (LEFT / RIGHT too) |
| LEFT / RIGHT | – | In the options: previous / next value · paused live: 10 s back / forward |
| 0-9 | Go to that channel number | Go to that channel number (OK goes at once) |
| 0 / RECALL | – | Previous channel |
| INFO / EPG | Programme guide of the list | Infobar on / off |
| MENU | Menu | Options |
| Colour keys | The actions shown at the bottom | The actions shown at the bottom |
| No colour keys? | DOWN at the end of the list: the bottom buttons, ◀ ▶ and OK | Infobar shown: ◀ ▶ along its buttons, OK · hold OK: options |
| Play / Pause | – | Pause live TV / play |
| Rewind / Fast forward · Stop | – | 30 s back / forward · back to live |
| BACK | Back | Closes the infobar first, then leaves |

## Problems?

- **A channel doesn't play** – press OK to try again; its other sources are tried by themselves.
- **Nothing loads** – your provider may block Vavoo: turn on **Secure DNS** in the settings, or use a VPN.
- **No sound / no Dolby** – try the **audio passthrough** setting (on with an AV receiver, off with TV speakers).
- **Forgot the PIN** – clearing the app's data resets it (and the settings).


Anything else: in the app **Settings → Show Log → Share**, and send the log with a short description.

## Credits & license

- Android app: **Qu4k3**.
- Based on the Enigma2 plugin *Vavoo Stream Live* by **Lululla / Belfagor2005**.
- Guide data: epgshare01.online and the plugin's channel maps.
- License: [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) –
  non-commercial, attribution required, share-alike.
