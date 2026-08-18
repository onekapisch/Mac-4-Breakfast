# Changelog

All notable changes to Mac 4 Breakfast. Format based on [Keep a Changelog](https://keepachangelog.com/). **[⬇️ Download the latest](https://www.mac4breakfast.app)**

## [0.3.15] - 2026-08-18
### Fixed
- **The menu-bar panel closes when you tell it to.** Clicking the icon while the panel was open could leave it sitting there, so it never quite worked as a toggle. The click that should close it now closes it.
- **No more blank panel.** Opening the panel again straight after closing it could show an empty window. The old panel was being tidied away a moment too late and took the new one's contents with it.
### Changed
- The $4.99 launch price ends on 31 August; Pro then returns to its regular $9.99. Licenses already purchased are unaffected.

## [0.3.14] - 2026-08-10
### Fixed
- **No more absurd time estimates.** macOS's own time-remaining is a rolling average that can lag far behind, showing 20 hours while you draw 13 watts. The app now cross-checks it against your live power draw and shows its own calculation when they disagree badly.
- **Sharper low-battery warnings.** The predictive alert uses the same corrected estimate, so a stale number can no longer delay a warning.

## [0.3.13] - 2026-08-06
### Fixed
- **No more background battery use.** Once the panel had been opened, an animation kept running invisibly behind it and quietly used CPU until the app was quit. Closing the panel now frees everything.
### Changed
- The panel now always opens on the Mac tab, instead of wherever you left it last.

## [0.3.12] - 2026-07-26
### Fixed
- **No more cut-off menu.** With the menu bar icon near the right edge of the screen, the panel could open past the edge and lose its last tab and buttons. It now always positions itself to fit.
### Changed
- Hold Command and drag the icon to move it anywhere in your menu bar. It stays where you put it.

## [0.3.11] - 2026-07-25
### Fixed
- **Your menu-bar metrics are back.** The percentage and your second metric could be cut off in the menu bar, leaving just the icon. The menu-bar item now sizes itself to whatever you have chosen to show. (A regression introduced in 0.3.10.)

## [0.3.10] - 2026-07-25
### Fixed
- **The menu-bar icon can no longer disappear.** After sleeping with the lid closed, or unplugging a monitor, the icon could vanish from the menu bar while the app kept running, with no way back except force-quitting it. Mac 4 Breakfast now looks after its own menu-bar icon and puts it straight back if macOS clears it away.

## [0.3.9] - 2026-07-23
### Changed
- **Meet your Energy Hero.** The power card is now a rich, glowing panel with a luminous charge line. While you're plugged in, it breathes gently, like the sleep light on older Macs.
- **A warmer Keep Awake.** The Keep Awake control gets a rich gold finish with a soft gloss, easier to spot and nicer to tap.
- **Genuinely great in Light Mode.** Every tab was rebuilt with real contrast and depth in Light Mode: no more washed-out colors or hard-to-read text.
### Fixed
- The Battery Health chart on the History tab no longer tints the area below the plot.

## [0.3.8] - 2026-07-22
### Changed
- **Keep Awake, reimagined.** Choose Off, Screen, or Lid Closed in a single tap, with the lid-closed thermal/battery safety net built right in. Replaces the old separate Keep Awake toggle and Wide Awake setup.
- **A calmer Mac view.** Temperature now sits in the header next to your charge %, and your charge level reads as a subtle color-coded fill behind the power card instead of a separate bar. Battery details (condition, health, cycles, capacity) moved into a collapsible row.
### Fixed
- **Clearer low-battery alerts.** Alerts for your iPhone, iPad and AirPods now warn in amber and turn red when it's urgent, instead of a hard-to-read blue.
- Temperature is back on the newest macOS beta, read from the SMC when Apple's own battery registry stops reporting it.
- Uptime now reflects real system uptime, not just the time your Mac has been awake.

## [0.3.7] - 2026-07-18
### Changed
- **Charging shows up instantly.** Plug in and the menu bar reacts right away instead of taking up to half a minute to catch up.
- **"Fully Charged" actually means it.** No more sitting on "Calculating…" at 100%. Your Mac now reports full exactly when macOS does.
- **See what you're running on.** The power card names your source, Power adapter or Battery, right next to the live voltage.
- Power settings moved to the end of the tab bar, next to Insights.

## [0.3.6] - 2026-07-14
### Added
- **Charging Comet, your way:** pick your pace, Slow, Normal or Fast, and one of six colors.
### Changed
- A new high-contrast backdrop keeps the comet reading clearly on any wallpaper, dark or bright.
- Settings reorganized into a cleaner, tabbed window: General, Menu Bar, Comet, Wide Awake and About.

## [0.3.5] - 2026-07-13
### Added
- **Wide Awake.** Keep your Mac working with the lid shut, with a safety net no other app has: it watches battery temperature and shuts itself off automatically if your Mac gets too hot in a bag or the battery runs low.
- Battery Shortcuts for Siri & automations: new actions for your percentage, health, cycles and temperature.

## [0.3.2] - 2026-07-11
### Added
- **German localization ("Jetzt auf Deutsch").** Every screen, alert, tip and setting hand-translated, using Apple's own German battery terminology. No machine-translation slop.
- A language switcher in Settings: English, Deutsch, or follow your Mac's system language.
### Changed
- Numbers now follow your region: decimal commas, tidy spacing and units, so the whole app feels local, not translated.

## [0.3.1] - 2026-07-07
### Fixed
- **Accurate on the macOS 27 beta.** Apple moved where battery values live in that beta, so health, condition and capacity could read as 0% or Unknown. They read correctly again now. Cycle count was never affected. The same fix protects iPhone/iPad battery readouts against similar changes down the line.

## [0.3.0] - 2026-07-04
### Added
- **Sleep Drain Detective.** Wake up to an answer: when your Mac loses charge overnight, it names the culprits and drops the verdict from the notch.
- **The Apps tab.** See every open app ranked by the energy it has burned since launch, and quit the expensive ones in a single tap.
- **Charging Comet, perfected.** Plug in and a comet sweeps the screen and lands on the notch in a bloom of light. Pick one, two or three laps in Settings.
- **Battery Report Card.** Export your battery's health, cycles and history as a PDF, CSV or JSON. It never leaves your Mac.

## [0.2.4] - 2026-06-28
### Added
- **Keep Awake.** Tap once to stop your screen from sleeping: ideal for downloads, presentations or long reads. Pick a timer of 30, 60 or 120 minutes, or leave it on until you turn it off, right from the Mac tab. A steaming mug appears in the menu bar while it's active.
### Changed
- Tidier popover: the full wordmark now sits along the bottom, and the version number moved into Settings.

## [0.2.3] - 2026-06-19
### Changed
- **Smarter overheating alerts.** The alert now triggers at a sensible battery-cell temperature and only when it *stays* hot, instead of firing during normal charging. (Apple's well-known 35 °C is a *room*-temperature limit, not a cell temperature.)
- **Set your own threshold** for the overheating alert, in °C or °F, right from the Power tab.
- **Calmer menu bar:** a warm battery is now a gentle amber hint; the red warning is reserved for when it's genuinely hot.

## [0.2.2] - 2026-06-17
### Added
- **Charging Comet:** a green light sweeps your screen's edge and traces the notch when you connect the charger. Toggle it in Settings.
### Changed
- Smart Alerts now queue politely instead of cutting each other off; iPhone/iPad low-battery alerts work on desktop Macs too.
- Reliability pass: a damaged data file is set aside instead of resetting your history; more work moved off the main thread; the energy list no longer shows Simulator internals.

## [0.2.1] - 2026-06-16
### Fixed
- **Much lighter on battery.** Live readings, the energy list and device scans now run only while the popover is open and stop the moment you close it; the menu bar updates on real changes instead of a constant timer. Idle CPU is ~0.

## [0.2.0] - 2026-06
### Added
- **Smart Alerts:** intelligent battery notifications that drop from the notch (unplug reminder, predictive low-battery, overheating).

[0.3.15]: https://www.mac4breakfast.app
[0.3.14]: https://www.mac4breakfast.app
[0.3.13]: https://www.mac4breakfast.app
[0.3.12]: https://www.mac4breakfast.app
[0.3.11]: https://www.mac4breakfast.app
[0.3.10]: https://www.mac4breakfast.app
[0.3.9]: https://www.mac4breakfast.app
[0.3.8]: https://www.mac4breakfast.app
[0.3.7]: https://www.mac4breakfast.app
[0.3.6]: https://www.mac4breakfast.app
[0.3.5]: https://www.mac4breakfast.app
[0.3.2]: https://www.mac4breakfast.app
[0.3.1]: https://www.mac4breakfast.app
[0.3.0]: https://www.mac4breakfast.app
[0.2.4]: https://www.mac4breakfast.app
[0.2.3]: https://www.mac4breakfast.app
[0.2.2]: https://www.mac4breakfast.app
[0.2.1]: https://www.mac4breakfast.app
[0.2.0]: https://www.mac4breakfast.app
