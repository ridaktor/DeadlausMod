# Deadlaus Mod (QIDI Q1 Pro)

[![Release](https://img.shields.io/github/v/release/ridaktor/DeadlausMod)](https://github.com/ridaktor/DeadlausMod/releases)
[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey)](LICENSE)
[![Printables](https://img.shields.io/badge/Printables-model-orange)](https://www.printables.com/model/1561573-deadlaus-mod-qidi-q1-pro)

Toolhead-focused upgrade for the **QIDI Q1 Pro** aimed at reliable **high-temp, enclosed engineering materials** printing.

## Highlights
- Klicky detachable probe for accurate Z and flexible build surfaces
- Volcano nozzle system (supports CHT inserts) for higher flow and stronger parts
- Upgraded hotend cooling fan to 3010
- Upgraded part cooling duct
- Added rear-cover fan to prevent toolhead overheating in a hot chamber
- Designed for enclosed “engineering materials” workflow
- Detachable front cover via pogo-pin connection for the part cooling fan
- Rear electronics exhaust fan relocated to the back wall to pull hot air away from the electronics bay and improve temperature stability in an enclosed setup
- **Deterministic XY motion tuning (StealthChop disabled)** for more repeatable high-speed moves and cleaner motion behavior

## Pros
- Proven hot-chamber readiness: stable printing at **80°C chamber** (tested), likely higher depending on your setup
- Works on basically any build surface (including glass) thanks to Klicky probing and consistent Z referencing
- Stronger parts / higher throughput using Volcano nozzles + CHT inserts (more flow headroom, better layer bonding at speed)
- Toolhead stays cooler in an enclosed printer: rear-cover fan reduces heat soak and helps protect electronics
- More repeatable first layer after maintenance: detachable probe reduces “drift” from fixed sensors
- **More repeatable motion at high accel:** XY drivers run in a consistent regime (no StealthChop), improving step consistency/torque behavior for aggressive CoreXY profiles (at the cost of extra motor noise)

## Cons
- Harder extruder access: servicing the extruder or clearing clogs takes longer due to the toolhead layout and added parts
- Slightly reduced printable area near the Klicky dock zone (rear notch). Keep models out of that region to avoid collisions
- **More noise (by design):** X/Y drivers are in a deterministic motion mode (StealthChop disabled) for higher positional repeatability at high accel; extra fans add airflow noise.  
  *You can trade some of this back by lowering accel/jerk, reducing fan speeds, or enabling StealthChop below a speed threshold.*
- Reduced maximum Z height: using a ~5 mm glass build plate and longer Volcano nozzle setups can slightly reduce available Z travel (plan for a few mm less print height)
- No automatic nozzle-wipe/cleaning: you must use a manual wipe/brush or a purge line in your start G-code
- Part cooling asymmetry: even though the duct is designed for balanced flow, one side may cool slightly better due to a larger outlet area on that side

## Repo layout
- `config/` — Klipper config (printer.cfg)
- `docs/` — BOM, wiring, tuning notes + images
- `models/` — STL/STP models (**Git LFS**)
- `CHANGELOG.md` — release notes history

## Downloads
See **GitHub Releases** for ready-to-download ZIP assets (models + docs/config).

## Disclaimer / use at your own risk
This is not a beginner upgrade. You must be comfortable with disassembly, wiring, tuning, and Klipper configuration. Everything is provided as-is. You accept full responsibility for any damage, malfunction, injury, or loss.
- Fully reversible: can be reverted to stock (no permanent mods)

## Links
- Releases: https://github.com/ridaktor/DeadlausMod/releases
- Printables (draft): https://www.printables.com/model/1561573-deadlaus-mod-qidi-q1-pro
- Boosty: (add link)
- Patreon: (add link)
