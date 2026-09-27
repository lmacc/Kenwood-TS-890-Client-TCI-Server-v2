<img src="docs/images/icon.png" alt="" width="96" align="left">

# TS-890S Desktop Front Panel

**Control your Kenwood TS-890S from your Windows PC or Mac. It has a TCI
server built in.**

[![Download](https://img.shields.io/github/v/release/lmacc/Kenwood-TS-890-Client-TCI-Server-v2?label=Download)](https://github.com/lmacc/Kenwood-TS-890-Client-TCI-Server-v2/releases/latest)
![Windows 10 and 11](https://img.shields.io/badge/Windows-10%20%7C%2011-0078D4?logo=windows)
![macOS 13 and later](https://img.shields.io/badge/macOS-13%2B%20%C2%B7%20Apple%20silicon%20%26%20Intel-555555?logo=apple)
[![Donate](https://img.shields.io/badge/Donate-PayPal-00457C?logo=paypal)](https://www.paypal.com/donate/?business=9XVP453VRC5GC&no_recurring=0&item_name=Free%2C+and+always+will+be.+If+it%27s+earned+a+place+in+your+shack%2C+a+coffee+keeps+it+growing.+73%2C+Leslie+EI5GJB&currency_code=EUR)

<br clear="left">

![The front panel](docs/images/front-panel.png)

The keys, knobs and meters look and work like the ones on the radio. You
can move, resize and hide the groups of controls, and save your own
layouts. CAT control and audio go over the radio's USB cable. The bandscope
comes over your network, because the USB serial link is too slow for a
smooth scope.

## What it does

- **The radio's front panel on your screen.** VFOs, band keys, modes,
  filters, split, TF-SET, RIT/XIT, AGC, NR, NB, notch, the meters and the
  radio's own menu. It all stays in step with the rig.
- **Bandscope and waterfall** over your network. Click to tune, drag to
  tune, markers, and drag the filter edges.
- **Audio scope.** See your receive and transmit audio, with peak and
  average traces, THD and S/N readings.
- **NR4 noise reduction** on the computer, on top of the radio's own NR.
- **CW, RTTY and PSK31.** Decode and send, with F1 to F8 macros.
- **Logbook.** Log a QSO with two presses of the LOG key. It records their
  signal from the S-meter and sends the QSO to Log4OM, or any logger that
  takes QSOs from WSJT-X. If your logger is closed, the QSO waits and goes
  when the logger is running again.
- **FT8 with WSJT-X.** WSJT-X decodes show up on the bandscope, coloured
  if the country is new to you.
- **TCI server.** Log4OM, WSJT-X, MSHV and other programs can follow the
  radio over TCI.
- **CAT sharing (Windows only).** Share the radio's CAT port with another
  program through a virtual serial port, so both work at the same time.
- **Recorder**, **keyboard shortcuts** for every key, and a full
  [user guide](#the-user-guide).

| | |
|---|---|
| ![Connections](docs/images/connections.png) | ![Working with Log4OM and WSJT-X](docs/images/tci-and-cat-sharing.png) |
| All the setup in one window: COM port, audio, bandscope and sharing. | Log4OM and WSJT-X following the radio. |
| ![NR4](docs/images/nr4.png) | ![Key bindings](docs/images/key-bindings.png) |
| NR4 noise reduction, with every setting explained. | Put any key on the keyboard. |

## Logging from the decoded text

In CW, RTTY and PSK31 you can take the other station's details straight
from the decoded text. Double-click a callsign and a menu asks what it is.
Pick **Use as the DX callsign** and it goes into the Call box, ready for
your macros. You can also pick their **report, name, QTH or locator**, and
it goes into the QSO you are logging.

![CW decoding with the double-click menu](docs/images/cw-decode-and-logging.png)

*CW on 20m at 30 wpm. LA8HGA has been double-clicked and the menu is
offering to make it the DX callsign. Under the text are the Call and RST
boxes, the F1 to F8 macro keys, EDIT and LOG.*

Then press **LOG**. You'll find it on the top bar and beside the macros,
or use Ctrl+L.

- **First press:** the QSO opens with the frequency, band, mode, time and
  their S-meter reading already filled in. In CW, RTTY and PSK31 the call
  and your report come from the decode pane.
- **Second press:** the QSO is saved.
- **In SSB** you type the call, and your report is taken from the S-meter.
  S7 gives 57.

Every QSO is kept in the app's own logbook and sent on to your logging
program in the same way WSJT-X sends its QSOs. For Log4OM there is nothing
to set up. If Log4OM is not running, the QSO waits until it is. The app
also checks Log4OM's logbook, and marks the QSO as done only when it is
really in there.

![The Log QSO window and the Logbook](docs/images/logbook.png)

*Left: logging a QSO on 40m. Their S7 signal has already been turned into
a 57 report. Right: the Logbook. The earlier QSO says "in your log", which
means Log4OM has it.*

## Download and install

### Windows

1. Go to the
   [latest release](https://github.com/lmacc/Kenwood-TS-890-Client-TCI-Server-v2/releases/latest)
   and download **`TS-890S-Desktop-<version>-setup.exe`**.
2. Run it. It installs just for you and doesn't need an administrator. On
   its first page you can choose to install it for everyone on the computer
   instead.
3. Start **TS-890S Desktop** from the Start menu. The user guide is there
   too.

> **"Windows protected your PC"?** The installer isn't digitally signed
> yet, so Windows asks before running it the first time. Click **More
> info**, then **Run anyway**.

The first time you run it, the Connections window opens. Set the radio's
COM port and its IP address for the bandscope, and tick **Audio in**.

A newer installer updates the one you have, and your settings are kept. To
remove it, use **Settings → Apps** like any other program.

**Don't want to install it?** Each release also has a portable
**`…-win64.zip`**. Right-click it and choose **Extract All** first, then run
`ts890-usb.exe` from the folder you extracted. If you run it from inside the
zip it can't find its files and stops with *"Qt6Core.dll was not found"*.

### Mac (new in 2.2.0)

The Mac version is new. It is built and checked the same way as the Windows
version, but it hasn't been tried on many Macs yet. If you use it, please
let me know how it goes, good or bad, in
[Issues](https://github.com/lmacc/Kenwood-TS-890-Client-TCI-Server-v2/issues).

1. Go to the
   [latest release](https://github.com/lmacc/Kenwood-TS-890-Client-TCI-Server-v2/releases/latest)
   and download **`TS-890S-Desktop-<version>-macos.dmg`**.
2. Open it and drag **TS-890S Desktop** into the **Applications** folder.
3. Open it from Applications.

> **"Apple could not verify…"?** The app isn't signed by Apple yet, so the
> Mac asks before opening it the first time.
> On **macOS 15 or later**: try to open it once and click **Done**. Then go
> to **System Settings → Privacy & Security**, scroll down and click **Open
> Anyway**.
> On **macOS 13 or 14**: hold Control and click the app in Applications,
> choose **Open**, then **Open** again.
> You only have to do this once.

The Mac will then ask if the app can use the **microphone**. Say yes. That's
how it hears the radio's USB audio. Without it the scopes and decoders get
no sound. It may also ask about the **local network**. That's for the
bandscope, so say yes to that too.

The first time you run it, the Connections window opens. The radio's USB
ports show up with names like `cu.SLAB_USBtoUART` or `cu.usbserial-…`. Pick
the first of the two. To update later, drag the new version over the old
one. Your settings are kept.

### What it runs on

| | Windows | Mac |
|---|---|---|
| **System** | Windows 10 or 11, 64-bit | macOS 13 Ventura or later (13, 14 Sonoma, 15 Sequoia, 26 Tahoe) |
| **Computer** | Any 64-bit PC | Apple silicon Macs (M1, M2, M3, M4 and newer) and Intel Macs. One download works on both. |
| **Download** | `…-setup.exe`, or the portable `…-win64.zip` | `…-macos.dmg` |
| **Won't run on** | Windows 7 or 8, or 32-bit Windows | macOS 12 or older. That includes older Intel Macs that can't update past macOS 12. |

You also need:

- The USB cable from the radio to the computer, and the radio's USB driver
  (Silicon Labs CP210x) so its ports show up. On a Mac, if the ports don't
  appear, install the CP210x driver for macOS from Silicon Labs.
- The radio's CAT speed set to **115200** (menu 7-00).
- For the bandscope over the network: the radio on your network, and the
  KNS user name and password set on the radio. Everything else works
  without it, just with a slower bandscope over USB.

On a Mac there's no CAT sharing. Use the TCI server to connect other
programs instead. The logbook works with Mac loggers that take QSOs from
WSJT-X, such as MacLoggerDX and RUMlogNG.

## The user guide

The download comes with a full user guide, written for someone who has
never used the app before. You can open it any time from **ABOUT → USER
GUIDE**. Some of what it covers:

- **Setup in one window.** COM port, audio, bandscope and sharing are all
  in the Connections window, which opens by itself the first time. If the
  bandscope is ever empty, it tells you why.
- **Tuning.** Drag the knob, use the mouse wheel (hold Shift for small
  steps), click or drag on the bandscope, Ctrl+wheel to change the span, or
  type a frequency on the keypad.
- **Band stacks that remember the mode.** Hold a band key for five memories
  per band. Each one keeps the frequency and the mode you were using.
- **Split.** TF-SET lets you listen on your transmit frequency and move it.
  A marker shows where you came from. The VFO B key moves your transmit
  frequency while you keep listening to the pile-up.
- **Bandscope settings.** Pull the trace down so strong signals don't hit
  the top. Pause it, change the reference level, pick colours. It remembers
  all your choices.
- **Your own audio.** The audio scope shows what your transmit audio looks
  like, with THD and S/N readings, before-and-after comparisons, and masks
  for 2.8k, 3.5k and 4k eSSB widths.
- **NR4.** Noise reduction on the computer, on top of the radio's own NR.
  The scopes and the recorder still get the audio as the radio sent it.
- **FT8.** WSJT-X decodes show on the bandscope where they were heard.
  Amber is a new country, cyan is new on this band, and an **L** means they
  use LoTW. **Set up for FT8** sets the radio up in one press, and **Put it
  back** undoes it.
- **Logging.** How to pick details out of the decoded text, the LOG key,
  the Logbook, and connecting it to your logger.
- **The radio's menu.** Every setting shows the radio's own menu number, and
  you can search it. Type *115200* and it finds the baud rate.
- **Make it yours.** Move, resize and hide the groups of controls, save
  layouts, lock the window size, and put any key on the keyboard.
- **Troubleshooting.** A table that goes from the problem to the most
  likely cause.

## Support

It's free and it always will be. If it's earned a place in your shack, a
coffee keeps it going. There's a **DONATE** key in the app's About box, or
use the button below.

<img src="docs/images/about.png" alt="The About box, with USER GUIDE and DONATE" width="420">

[![Donate with PayPal](https://img.shields.io/badge/Donate-PayPal-00457C?logo=paypal&style=for-the-badge)](https://www.paypal.com/donate/?business=9XVP453VRC5GC&no_recurring=0&item_name=Free%2C+and+always+will+be.+If+it%27s+earned+a+place+in+your+shack%2C+a+coffee+keeps+it+growing.+73%2C+Leslie+EI5GJB&currency_code=EUR)

73, Leslie EI5GJB

## Licence

Freeware. It's free to use and free to pass on as long as you don't change
it, but it's not for sale. See [LICENSE](LICENSE). Only the finished program
is released, not the source code.

It uses Qt, libspecbleach and KISS FFT, which each have their own licence.
You'll find those in the `licenses` folder of the download. The source of
libspecbleach, as used, is attached to each release.

This app is not made or endorsed by JVCKENWOOD. TS-890S and KENWOOD are
trademarks of JVCKENWOOD Corporation.
