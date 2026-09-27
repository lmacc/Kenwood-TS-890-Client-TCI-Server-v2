<img src="docs/images/icon.png" alt="" width="96" align="left">

# TS-890S Desktop Front Panel

**A front panel for the Kenwood TS-890S on your Windows PC or Mac — with a
TCI server built in.**

[![Download](https://img.shields.io/github/v/release/lmacc/Kenwood-TS-890-Client-TCI-Server-v2?label=Download)](https://github.com/lmacc/Kenwood-TS-890-Client-TCI-Server-v2/releases/latest)
![Windows 10 and 11](https://img.shields.io/badge/Windows-10%20%7C%2011-0078D4?logo=windows)
![macOS 13 and later](https://img.shields.io/badge/macOS-13%2B%20%C2%B7%20Apple%20silicon%20%26%20Intel-555555?logo=apple)
[![Donate](https://img.shields.io/badge/Donate-PayPal-00457C?logo=paypal)](https://www.paypal.com/donate/?business=9XVP453VRC5GC&no_recurring=0&item_name=Free%2C+and+always+will+be.+If+it%27s+earned+a+place+in+your+shack%2C+a+coffee+keeps+it+growing.+73%2C+Leslie+EI5GJB&currency_code=EUR)

<br clear="left">

![The front panel](docs/images/front-panel.png)

Every key, knob and meter is drawn to look and behave like the radio's own,
and the clusters of controls can be moved, resized, hidden and saved as
layouts of your own. CAT and audio come over the radio's USB cable; the
bandscope comes over your network, fast and smooth, because twenty sweeps a
second will not fit down a 115200-baud serial port.

## What it does

- **The radio's front panel on screen** — VFOs, band keys, modes, filters,
  split and TF-SET, RIT/XIT, AGC, NR, NB, notch, the meters, the radio's own
  menu, and more, all live and in step with the rig.
- **Bandscope and waterfall** over the LAN, with markers, passband dragging
  and click-to-tune.
- **Audio scope** — a measuring analyser for the receive and transmit audio:
  peak and average traces, holds to compare against, THD and S/N readings.
- **NR4** — spectral noise reduction on the computer, on top of the radio's
  own NR.
- **CW, RTTY and PSK31** — decode and send, with F1–F8 macros.
- **A logbook that feeds your logger** — log a QSO in two presses, with
  the S-meter reading of their signal, and it goes straight to Log4OM (or
  any logger that takes WSJT-X's QSOs). Logger closed? It waits, and sends
  when the logger is back.
- **FT8 alongside WSJT-X** — decodes shown on the bandscope, coloured by what
  is new to you.
- **TCI server** — logging and digital-mode programs such as Log4OM, WSJT-X
  and MSHV follow the radio over TCI.
- **CAT sharing** (Windows) — pass CAT through to another program on a virtual serial
  port, so the panel and your logger both work at once.
- **Recorder**, **keyboard shortcuts** for every key, and a full
  [user guide](#the-user-guide).

| | |
|---|---|
| ![Connections](docs/images/connections.png) | ![Working with Log4OM and WSJT-X](docs/images/tci-and-cat-sharing.png) |
| One window to set up: COM port, audio, bandscope, sharing. | Log4OM and WSJT-X following the radio while the panel runs. |
| ![NR4](docs/images/nr4.png) | ![Key bindings](docs/images/key-bindings.png) |
| NR4 noise reduction, with every control explained. | Put any key on the keyboard. |

## From the copy to the log

In CW, RTTY and PSK31, the decoded text, the macros and the log work as
one. Double-click a callsign in the copy and it lights up, with a menu
asking what it is: **the DX callsign**, which goes straight into the
macros, or their **report, name, QTH or locator** for the QSO you are
logging. So the station's details come off the screen, not off the
keyboard.

![CW decoding with the double-click menu](docs/images/cw-decode-and-logging.png)

*CW on 20m at 30 wpm, locked on at 23 dB S/N. LA8HGA has been
double-clicked in the copy and the menu offers to make it the DX callsign.
Below: the Call and RST boxes, the F1–F8 macro keys, EDIT and LOG.*

Then **LOG** — on the top bar, beside the macros, or Ctrl+L. The first
press opens the QSO with the frequency, band, mode, start time and their
S-meter reading already filled in, plus the call and your report from the
decode pane. The second press saves it. In SSB you type the call and the
report is made from the meter: S7 becomes 57.

Every QSO is kept in the application's own logbook and handed straight on
to your logging program, the same way WSJT-X hands over its own. That
means nothing to set up in Log4OM, N1MM Logger+ or MacLoggerDX. If your
logger isn't running, the QSO waits and goes the moment it starts. With
Log4OM, each QSO is checked in Log4OM's own logbook and only marked done
once it's really there.

![The Log QSO window and the Logbook](docs/images/logbook.png)

*Left: a QSO being logged on 40m, with their S7 signal already turned into
a 57 report. Right: the Logbook, where an earlier QSO shows "in your log",
confirmed by Log4OM, above the settings for the link to your logger.*

## Download and install

### Windows

1. From the
   [latest release](https://github.com/lmacc/Kenwood-TS-890-Client-TCI-Server-v2/releases/latest),
   download **`TS-890S-Desktop-<version>-setup.exe`**.
2. Run it. It installs for you alone without asking for an administrator, or
   for everybody on the computer if you choose that on its first page.
3. Start **TS-890S Desktop** from the Start menu. The user guide is there
   too.

> **"Windows protected your PC"?** The installer is not yet digitally
> signed, so Windows SmartScreen asks before running it the first time.
> Click **More info**, then **Run anyway**.

On the first run the Connections window opens by itself: set the radio's COM
port, its IP address for the bandscope, and tick **Audio in**.

A newer installer upgrades an older installation in place, and your settings
are kept. To remove it, use **Settings → Apps** like any other program.

**Prefer not to install?** Each release also has a portable
**`…-win64.zip`**. Extract the **whole** zip first (right-click, **Extract
All**) and run `ts890-usb.exe` from the extracted folder — run from inside
the zip, Windows copies the program out without the files it needs, and it
stops with *"Qt6Core.dll was not found"*.

### Mac

1. From the
   [latest release](https://github.com/lmacc/Kenwood-TS-890-Client-TCI-Server-v2/releases/latest),
   download **`TS-890S-Desktop-<version>-macos.dmg`**.
2. Open it and drag **TS-890S Desktop** onto the **Applications** folder
   beside it.
3. Open it from Applications.

> **"Apple could not verify…"?** The application is not yet signed with an
> Apple Developer ID, so macOS asks before opening it the first time.
> On **macOS 15 and later**: try to open it once and click **Done**, then go
> to **System Settings → Privacy & Security**, scroll down, and click
> **Open Anyway**. On **macOS 13 and 14**: Control-click it in Applications,
> choose **Open**, then **Open** again. Once only.

macOS then asks whether it may use the **microphone**: say yes. That is how
it hears the radio's USB audio, and without it the scopes and decoders are
silent. It may also ask about the **local network**, which is the LAN
bandscope.

On the first run the Connections window opens by itself. The radio's USB
ports appear as `cu.SLAB_USBtoUART…` or `cu.usbserial-…`; pick the lower of
the pair. To update, drag the new version over the old one; your settings
are kept.

### What it runs on

| | Windows | Mac |
|---|---|---|
| **System** | Windows 10 or 11, 64-bit | macOS 13 Ventura or later — 13, 14 Sonoma, 15 Sequoia and 26 Tahoe |
| **Hardware** | Any 64-bit (x64) PC | **Apple silicon** (M1, M2, M3, M4 and later) and **Intel** Macs — one download, native on both, no Rosetta |
| **Download** | `…-setup.exe` (or the portable `…-win64.zip`) | `…-macos.dmg` |
| **Not supported** | Windows 7 and 8, 32-bit Windows | macOS 12 and earlier, which includes Intel Macs that cannot be updated past macOS 12 |

Either way, you also need:

- The radio's USB cable to the computer, with the radio's USB driver
  (Silicon Labs CP210x) installed so its ports appear. On a Mac, if they do
  not appear, install Silicon Labs' CP210x driver for macOS.
- The radio's CAT speed at **115200** (menu 7-00).
- For the LAN bandscope: the radio on your network and its KNS user name and
  password. Without it everything else still works, with a slower bandscope
  over USB.

Sharing the radio's CAT port with another program over a virtual serial
port is a Windows feature. On a Mac, give other programs the built-in TCI
server instead. The logbook works with any logger that takes WSJT-X's QSOs,
such as MacLoggerDX or RUMlogNG.

## The user guide

A full guide comes with the download, written for somebody who has never
used the application before. Open it any time from **ABOUT → USER GUIDE**.
A taste of what's in it:

- **Up and running in one window.** COM port, audio, bandscope and sharing
  are all set in one place, and it opens by itself the first time you run
  the app. If the bandscope is ever empty, the scope itself tells you why.
- **Tune the way you like.** Drag the knob, roll the mouse wheel (Shift for
  fine steps), click or drag on the bandscope, Ctrl+wheel to zoom the span,
  or type a frequency on the keypad.
- **Band stacks that remember the mode.** Press and hold a band key for five
  slots per band, each keeping its frequency *and* the mode you worked it in,
  because 7.040 in CW and 7.040 in LSB are different places.
- **Work split without losing your place.** TF-SET lets you listen on your
  transmit frequency and move it. The R and T markers merge on the scope, and
  a marker is left where you came from. A red VFO B key moves your transmit
  frequency while the receiver stays on the pile-up.
- **A bandscope you can tame.** Drag the trace down and strong signals stop
  hitting the top while the noise floor stays put. Pause the picture, nudge
  the reference, pick a palette, and every choice is remembered.
- **See your own audio.** Nothing on the radio shows you what your audio
  looks like. The audio scope does: average and peak traces, THD, THD+N and
  S/N readings from a click on a peak, before-and-after holds to compare, and
  masks for 2.8k, 3.5k and 4k eSSB bandwidths.
- **NR4 on the computer.** Spectral noise reduction on what you hear, stacking with
  the radio's own NR, while the scopes and the recorder keep what the radio
  really sent.
- **FT8 with the band at a glance.** WSJT-X decodes land on the bandscope at
  the frequency they were heard: amber for a DXCC entity you've never worked,
  cyan for new on this band, and an **L** for LoTW users. **Set up for FT8**
  configures the rig in one press, and **Put it back** undoes exactly what it
  changed.
- **Log as you go.** Double-click a callsign, name or report in the decoded
  text to use it; LOG opens and saves a QSO in two presses, with the
  S-meter reading of their signal; and the Logbook shows every QSO arriving
  in your logger, or waiting for it to start.
- **The radio's menu, searchable.** Every row carries the rig's own menu
  number, and typing *115200* finds the baud rate. The network (KNS) settings
  have a page of their own.
- **Make it yours.** Arrange, resize and hide the clusters, save layouts (a
  contest one and a listening one), lock the window size, and put any key on
  the keyboard.
- **When something isn't working.** A troubleshooting table goes straight
  from the symptom to the most likely cause.

## Support

Free, and always will be. If it's earned a place in your shack, a coffee
keeps it growing. There's a **DONATE** key in the application's About box,
or use the button below.

<img src="docs/images/about.png" alt="The About box, with USER GUIDE and DONATE" width="420">

[![Donate with PayPal](https://img.shields.io/badge/Donate-PayPal-00457C?logo=paypal&style=for-the-badge)](https://www.paypal.com/donate/?business=9XVP453VRC5GC&no_recurring=0&item_name=Free%2C+and+always+will+be.+If+it%27s+earned+a+place+in+your+shack%2C+a+coffee+keeps+it+growing.+73%2C+Leslie+EI5GJB&currency_code=EUR)

73, Leslie EI5GJB

## Licence

Freeware — free to use, and free to pass on unchanged, but not for sale. See
[LICENSE](LICENSE). The application is distributed as a compiled program
only.

It is built on Qt, libspecbleach and KISS FFT, each under its own licence;
the notices are in the `licenses` folder of the download. The source of
libspecbleach, as built, is attached to each release.

Not made or endorsed by JVCKENWOOD. TS-890S and KENWOOD are trademarks of
JVCKENWOOD Corporation.
