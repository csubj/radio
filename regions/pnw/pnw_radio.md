# pnw_radio

A channel list for the greater Washington State area.

Operator: KI7LCR (Amateur Radio license).

`pnw_radio.csv` is a CHIRP import file. It replaces the content of
`downloaded_radio.csv`. The original file has duplicates and placeholder tones.
This file has clean channels, correct tones, and correct offsets.

## How to import

1. Open CHIRP.
2. Select your radio model.
3. Select "File", then "Import from file".
4. Select `pnw_radio.csv`.
5. Verify the memory channels, then write to your radio.

Use the CSV with the same radio as `downloaded_radio.csv`. It is a dual-band
VHF/UHF handheld that covers 2 meters and 70 centimeters. It also receives
FRS, GMRS, MURS, and NOAA weather radio.

## What changed

The original file has these problems.

- Some FRS and GMRS rows repeat the same placeholder tone. The tone does not
  match the actual service.
- Some channels appear twice. For example `462.5625` and `162.400`.
- Some rows have non-standard offsets. For example `444.925` with a `0.948`
  offset, and `166.300` with a `1.875` offset.
- Some channels have no name.

This file fixes those problems and adds coverage.

## Channel organization

The list is ordered by service group.

### Simplex calling

These are the national calling frequencies. Use them to start a contact, then
move to another frequency.

| Name | Frequency (MHz) | Use |
| --- | --- | --- |
| 2M CALL | 146.520 | 2 meter FM calling |
| 70CM CALL | 446.000 | 70 centimeter FM calling |

ARES simplex channels for King County are also included. They are
`146.440`, `144.430`, and `144.370`.

### NOAA weather radio (WX1 to WX7)

These are the seven NOAA weather radio frequencies. They cover western
Washington through four NWS offices. The Seattle, Portland, Spokane, and
Pendleton offices broadcast on these frequencies.

| Frequency (MHz) | Note |
| --- | --- |
| 162.400 | |
| 162.425 | |
| 162.450 | |
| 162.475 | |
| 162.500 | |
| 162.525 | |
| 162.550 | |

Specific western Washington stations include Seattle on `162.550`, Puget Sound
marine on `162.425`, and Olympia on `162.475`.

### MURS

MURS is the Multi-Use Radio Service. It is unlicensed and limited to 2 watts.
Three channels use narrowband. Two channels use wideband.

| Name | Frequency (MHz) | Bandwidth |
| --- | --- | --- |
| MURS1 | 151.820 | 11.25 kHz |
| MURS2 | 151.880 | 11.25 kHz |
| MURS3 | 151.940 | 11.25 kHz |
| MURS4 | 154.570 | 20 kHz (blue dot) |
| MURS5 | 154.600 | 20 kHz (green dot) |

### Personal channel

The `BACKEND` channel uses `154.600` MHz with a 67.0 Hz tone-squelch (TSQL).
It shares the MURS5 frequency. The tone separates your traffic from other
users on that frequency.

### FRS and GMRS

FRS and GMRS share the 462 MHz and 467 MHz bands. FRS channels 1 to 14 are
simplex. GMRS channels 15 to 22 are simplex and are also the downlink of GMRS
repeaters.

This file lists FRS channels 1 to 14 (named `FRS1` to `FRS14`), GMRS simplex
channels 15 to 22 (named `GMRS1` to `GMRS8`), and four known Seattle-area GMRS
repeaters.

The four GMRS repeaters are:

| Name | Output (MHz) | Offset | Tone |
| --- | --- | --- | --- |
| GMRS-rpt 1 | 462.550 | +5 MHz | 103.5 Hz |
| GMRS-rpt 2 | 462.575 | +5 MHz | 103.5 Hz |
| GMRS-rpt 4 | 462.625 | +5 MHz | 100.0 Hz |
| GMRS-rpt 6 | 462.675 | +5 MHz | 141.3 Hz |

Three of these are the Shoreline and Hillside Repeater Group (SHRG). The
`462.675` repeater is the North Seattle 675. It supports Seattle ACS and the
Seattle Emergency Community Hubs.

### Amateur 2 meter repeaters

This file includes major repeaters in Seattle, Tacoma, Everett, and the wider
Puget Sound area. Each repeater has the correct CTCSS tone and offset.

Key repeaters include:

- `146.960` (WW7PSR) on Capitol Hill, Seattle. This is the main Puget Sound
  Repeater Group 2 meter repeater. It uses a `-0.600` MHz offset and a 103.5 Hz
  tone.
- `146.820` (K7LED) on East Tiger Mountain. This is a Mike and Key club
  repeater.
- `147.080` (W7WWI). This is a King County ARES primary repeater.
- `147.000` (W7DX). This is a King County ARES backup repeater.

The national 2 meter calling frequency `146.520` is in the simplex section.

### Amateur 70 centimeter repeaters

This file includes the major 70 centimeter repeaters in Seattle, Tacoma, and
Everett. Each uses a `+5.0` MHz offset.

Key repeaters include:

- `444.375` (AJ7JA) on Capitol Hill, Seattle.
- `444.700` (WW7SEA) on Queen Anne, Seattle.
- `444.425` (WW7SEA) at the KOMO tower, Seattle.
- `444.000` (K7SPG) in Seattle.
- `441.800` (W7AW) in West Seattle.

The national 70 centimeter calling frequency `446.000` is in the simplex
section.

### Digital and linked repeaters

Some repeaters use D-STAR, DMR, System Fusion, AllStar, or IRLP. The comment
field notes these when known. A radio without a digital mode still hears the
analog traffic on FM-linked or Fusion repeaters.

The `WR7DS` repeater on `442.725` uses DTCS. It uses code 172 with normal
polarity. A radio that supports DTCS receives it correctly.

### Licensing note

Amateur repeaters on 2 meters and 70 centimeters require an Amateur Radio
license. You hold KI7LCR.

GMRS repeaters and simplex channels require a separate GMRS license from the
FCC. Do not transmit on GMRS channels unless your GMRS license covers them.

FRS, MURS, and NOAA weather radio are receive-only on most radios. NOAA is
receive-only. Transmitting on FRS or MURS from a ham handheld may exceed the
service power limit.

## Known limits

Repeaters change over time. Some go off-air, some change tone, and some move
frequency. Verify a repeater against its club page or RepeaterBook before you
rely on it in an emergency.

The `443.300` frequency appears twice. One is `W7PLU` in Tacoma with a 103.5 Hz
tone. The other is `K7KG` with a 156.7 Hz tone. They are separate repeaters
that share an output frequency. Keep both to hear both.

Western Washington repeaters are moving to narrowband FM. The mode stays `FM`
in this file. Follow your radio manual when the local repeater operator
announces a change.

## Sources

- Puget Sound Repeater Group, "Bands, Frequencies and Tones",
  https://web.psrg.org/repeater-system/
- RepeaterBook, "SEATTLE, Washington Amateur Radio Repeaters",
  https://www.repeaterbook.com/repeaters/location_search.php?loc=SEATTLE&state_id=53&type=city
- RepeaterBook, "TACOMA, Washington Amateur Radio Repeaters",
  https://www.repeaterbook.com/repeaters/location_search.php?loc=TACOMA&state_id=53&type=city
- RepeaterBook, "EVERETT, Washington Amateur Radio Repeaters",
  https://www.repeaterbook.com/repeaters/location_search.php?loc=EVERETT&state_id=53&type=city
- RepeaterBook, "Washington State Repeaters",
  https://www.repeaterbook.com/repeaters/index2.php?country_code=US&state_id=53
- Mike and Key ARC, "Repeaters",
  https://www.mikeandkey.org/repeaters.php
- RadioReference Wiki, "FRS/GMRS combined channel chart",
  https://wiki.radioreference.com/index.php/FRS/GMRS_combined_channel_chart
- FCC, "Multi-Use Radio Service (MURS)",
  https://www.fcc.gov/wireless/bureau-divisions/mobility-division/multi-use-radio-service-murs
- FCC, "General Mobile Radio Service (GMRS)",
  https://www.fcc.gov/wireless/bureau-divisions/general-mobile-radio-service-gmrs
- NOAA / National Weather Service, "NWR Stations (Washington)",
  https://www.weather.gov/nwr/stations?State=WA
- PSRG Wiki, "GMRS and FRS Radio in Western Washington",
  https://wiki.psrg.org/wiki/GMRS_and_FRS_Radio_in_Western_Washington
- ARES / RACES of King County, "Resources and Frequencies",
  https://www.kingcoares.org/
- Puget Sound Repeater Group, "Net Schedule",
  https://web.psrg.org/net_schedule/

Original file: `downloaded_radio.csv`.
