# Changelog

All notable changes to Mac 4 Breakfast. Format based on [Keep a Changelog](https://keepachangelog.com/). **[⬇️ Download the latest](https://www.mac4breakfast.app)**

## [0.2.3] — 2026-06-19
### Changed
- **Smarter overheating alerts.** The alert now triggers at a sensible battery-cell temperature and only when it *stays* hot, instead of firing during normal charging. (Apple's well-known 35 °C is a *room*-temperature limit, not a cell temperature.)
- **Set your own threshold** for the overheating alert, in °C or °F, right from the Power tab.
- **Calmer menu bar** — a warm battery is now a gentle amber hint; the red warning is reserved for when it's genuinely hot.

## [0.2.2] — 2026-06-17
### Added
- **Charging Comet** — a green light sweeps your screen's edge and traces the notch when you connect the charger. Toggle it in Settings.
### Changed
- Smart Alerts now queue politely instead of cutting each other off; iPhone/iPad low-battery alerts work on desktop Macs too.
- Reliability pass: a damaged data file is set aside instead of resetting your history; more work moved off the main thread; the energy list no longer shows Simulator internals.

## [0.2.1] — 2026-06-16
### Fixed
- **Much lighter on battery.** Live readings, the energy list and device scans now run only while the popover is open and stop the moment you close it; the menu bar updates on real changes instead of a constant timer. Idle CPU is ~0.

## [0.2.0] — 2026-06
### Added
- **Smart Alerts** — intelligent battery notifications that drop from the notch (unplug reminder, predictive low-battery, overheating).

[0.2.3]: https://www.mac4breakfast.app
[0.2.2]: https://www.mac4breakfast.app
[0.2.1]: https://www.mac4breakfast.app
[0.2.0]: https://www.mac4breakfast.app
