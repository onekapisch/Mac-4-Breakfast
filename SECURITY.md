# Security & Privacy

Mac 4 Breakfast is built local-first. This document describes what data the app touches, what leaves your Mac (almost nothing), and how to report a security issue.

## Data flow: what's sent where

**Nothing about your battery, your usage, or your device ever leaves your Mac.** The app has no analytics SDK, no account system, and no server of its own.

| Data | Where it lives | Leaves your Mac? |
|---|---|---|
| Battery health, cycles, temperature, wattage, voltage | Read live from Apple's IOKit / IOKit.ps / SMC | **No** |
| Connected Apple devices (iPhone/iPad/AirPods/Watch) | Read over the local USB / Wi-Fi / Bluetooth APIs | **No** |
| Your settings, history & heat-event log | Local `UserDefaults` + a small on-disk file | **No** |
| Pro license key | Validated with the Lemon Squeezy licensing API **only when you activate** | Only the key, only at activation |
| Update check | Sparkle fetches a signed appcast from mac4breakfast.app | A standard HTTPS request; no personal data |

That's the complete list of network activity: **(1)** a one-time license activation, and **(2)** the Sparkle update check. You can confirm with a tool like Little Snitch, or by running the app with no network.

## Telemetry

**None.** No usage analytics, no crash-reporting SDK, no tracking or fingerprinting. We don't know which features you use, by design.

## Code signing & notarization

Every release is signed with an Apple **Developer ID** certificate, **notarized by Apple**, stapled, and distributed as a signed `.pkg` installer. Auto-updates are delivered through Sparkle and verified with an **EdDSA signature** before installation, so an update can't be tampered with in transit.

## Reporting a vulnerability

Found a security issue? Please email **support@onekapisch.com** with details and steps to reproduce. Please don't open a public issue for security problems. We'll acknowledge within a few days and keep you updated through the fix.
