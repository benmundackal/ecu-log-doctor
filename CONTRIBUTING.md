# Contributing

Thanks for helping. You don't need to be a programmer to contribute. Logs and bug reports are the most useful thing right now.

## Sending a log

1. Open an issue and pick **Wrong result** or **New logging software**.
2. Attach the CSV. If it's large, a few minutes around the problem is enough.
3. Say which car, engine, logging software and tune (stock, VersaTuner, RomDrop, NC Flash and so on).
4. Say what the tool showed and what you think really happened.

Remove anything personal from the file first, such as a VIN, if your software logs one.

## Changing the code

The whole tool is a single file, `index.html`, with no build step and no libraries to install.

1. Fork this repository and edit `index.html`.
2. Open it in a browser to test. Use the example log, and at least one real log if you have one.
3. Open a pull request describing what you changed and why.

### Where things are in index.html

- **`Core.FIELDS`**: how column names are recognized. Add patterns here to support a new logging tool.
- **`Core.build`**: unit handling (°F/°C, lambda/AFR, 0–1 vs 0–100 %).
- **The check functions** (`knock`, `lean`, `trims`, `cruise`, `iat`, `ect`, `idle`): the automatic flags and their limits.
- **`Core.sample`**: the built-in example log.
- **The app section** after `Core`: graphs, channel picker and the relationship view.

### Ground rules

- Keep everything running in the browser. Logs must never be uploaded anywhere.
- No outside services, trackers or analytics.
- If you change a limit (for example, the lean AFR threshold), explain why in the pull request.
- Keep the wording plain. Assume the reader is new to tuning.
