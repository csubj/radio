# radio

Radio channel lists and documentation.

This repo stores CHIRP radio configuration files and the research behind them.
Each region has its own directory with a channel list and a readme.

## Repo layout

- `regions/` — channel lists by region. Each region has a directory.
- `LICENSE` — MIT license.

## Regions

- [Pacific Northwest (pnw)](regions/pnw/pnw_radio.md) — greater Washington State
  area. Includes a CHIRP import file `pnw_radio.csv` and the source
  documentation `pnw_radio.md`.

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
