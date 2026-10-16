# ECU Log Doctor

A free, browser-based datalog explorer for car tuning. Load a CSV log and see every channel as its own graph on one shared timeline, compare any two channels to see how they relate, and get automatic flags for things like knock, lean mixture, fuel trims, heat soak and idle.

**Live site:** https://loganalyzer-nc.netlify.app

Built and tested on an NC Miata (2.5 swap, VersaTuner), but it reads any CSV log with column headers.

## Privacy

Your log never leaves your computer. Everything runs in your browser. Nothing is uploaded, stored or tracked.

## What it does

- **Synced channel graphs.** Every column in your CSV gets its own strip chart. Hover to read all values at the same moment. Drag to zoom.
- **Channel picker.** Choose which columns to show, with quick groups for Fuel, Ignition, Temps and Driving.
- **Relationships.** Plot any channel against another, colored by a third, and see which channels move most closely together.
- **Automatic flags.** Knock, lean at full throttle, fuel trims, rich cruise, intake heat soak, coolant temperature and idle quality. Each flag jumps the graphs to the moment it found.

The flags are automatic and can be wrong. Always confirm in the graphs before changing a tune.

## How to help

The fastest way to improve this is real logs from real cars.

- **Something looks wrong?** [Open an issue](https://github.com/benmundackal/ecu-log-doctor/issues/new/choose) and pick "Wrong result". Attach the CSV (or a short piece of it) and say what the tool showed versus what really happened.
- **Your logging software isn't recognized?** Open an issue with the column names from your CSV header row.
- **Want a feature?** Open an issue and pick "Feature idea".
- **Want to change the code?** See [CONTRIBUTING.md](CONTRIBUTING.md).

## Tested with

| Software | Status |
| --- | --- |
| VersaTuner | Tested |
| RomDrop / EcuFlash | Help wanted, please send a log |
| NC Flash | Help wanted, please send a log |
| Other (Tactrix, OBD apps) | Help wanted |

## License

MIT. Free to use, copy and modify. See [LICENSE](LICENSE).

This tool gives suggestions from data, not a tune. You are responsible for any changes you make to your car.
