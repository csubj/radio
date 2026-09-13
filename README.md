# radio

Radio channel lists and documentation.

This repo stores CHIRP radio configuration files and the research behind them.
Each region has its own directory with a channel list and a readme.

## Repo layout

- `regions/` — channel lists by region. Each region has a directory.
- `LICENSE` — MIT license.

## Regions

- [Greater Seattle](regions/greater-seattle/greater-seattle_radio.md) — greater
  Seattle and Washington State area. Includes a CHIRP import file
  `greater-seattle_radio.csv` and the source documentation
  `greater-seattle_radio.md`.
- [Tahoe](regions/tahoe/tahoe_radio.md) — South Lake Tahoe and the Lake Tahoe
  Basin, California. Includes a CHIRP import file `tahoe_radio.csv` and the
  source documentation `tahoe_radio.md`.

## File types

- `*.csv` — CHIRP import file. Import it through CHIRP, then write to your
  radio.
- `*.md` — documentation. It explains the channels and lists the sources used.

## How to import a channel list

1. Open CHIRP.
2. Select your radio model.
3. Select "File", then "Import from file".
4. Select the `*.csv` file for your region.
5. Verify the memory channels, then write to your radio.

Each region readme gives the details for that region.
