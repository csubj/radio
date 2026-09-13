# tahoe_radio

A channel list for the South Lake Tahoe area, California. It focuses on
Emerald Bay and the greater Lake Tahoe Basin.

Operator: KI7LCR (Amateur Radio license).

`tahoe_radio.csv` is a CHIRP import file. It uses the same radio as the
greater Seattle list. The radio is a dual-band VHF/UHF handheld that covers
2 meters and 70 centimeters. It also receives FRS, GMRS, MURS, and NOAA
weather radio.

## How to import

1. Open CHIRP.
2. Select your radio model.
3. Select "File", then "Import from file".
4. Select `tahoe_radio.csv`.
5. Verify the memory channels, then write to your radio.

## Channel organization

The list is ordered by service group. It keeps the same structure as the
greater Seattle list.

### Simplex calling

These are the national calling frequencies. Use them to start a contact, then
move to another frequency.

| Name | Frequency (MHz) | Use |
| --- | --- | --- |
| 2M CALL | 146.520 | 2 meter FM calling |
| 70CM CALL | 446.000 | 70 centimeter FM calling |

The Tahoe Basin ARES simplex frequencies are also included:
`146.550`, `147.480`, and `147.420`.

### NOAA weather radio

The Reno, Nevada National Weather Service office covers the Lake Tahoe Basin.
These are the NOAA weather radio transmitters for the area.

| Frequency (MHz) | Station | Coverage |
| --- | --- | --- |
| 162.550 | WXK58 | Reno and Tahoe |
| 162.450 | WWG20 | Reno, Pyramid Lake, Lassen County |
| 162.475 | WWF59 | Hawthorne and Mineral County |
| 162.525 | WNG595 | Mammoth-Bishop and Mono County |

The file also keeps the general NOAA frequencies `162.400`, `162.425`, and
`162.500`.

### MURS

MURS is the Multi-Use Radio Service. It is unlicensed and limited to 2 watts.

| Name | Frequency (MHz) | Bandwidth |
| --- | --- | --- |
| MURS1 | 151.820 | 11.25 kHz |
| MURS2 | 151.880 | 11.25 kHz |
| MURS3 | 151.940 | 11.25 kHz |
| MURS4 | 154.570 | 20 kHz (blue dot) |
| MURS5 | 154.600 | 20 kHz (green dot) |

### FRS and GMRS

The FRS channels 1 to 14 are simplex. The GMRS channels 15 to 22 are simplex
and are also the downlink of GMRS repeaters. This file lists FRS channels 1 to
14 (named `FRS1` to `FRS14`), GMRS simplex channels 15 to 22 (named `GMRS1`
to `GMRS8`), and two known South Lake Tahoe GMRS repeaters.

The two GMRS repeaters are:

| Name | Output (MHz) | Offset | Tone | Note |
| --- | --- | --- | --- | --- |
| GMRS-rpt A | 462.575 | +5 MHz | 136.5 Hz | Sierra Tract. Open. |
| GMRS-rpt B | 462.600 | +5 MHz | none | Heavenly Valley. Closed. |

The Heavenly Valley repeater has no publishable tone. It is closed to general
use. Keep the output frequency to monitor it.

### Amateur 2 meter repeaters

The Tahoe Amateur Radio Association (TARA) sponsors most of the basin
repeaters. Key repeaters include:

- `146.850` (WA6EWV) at Angels Roost. It has emergency backup power.
- `146.865` (WA6EWV) at Hawkins Peak. It links to `443.700`.
- `147.240` (NR7A) at East Peak. This is the primary basin repeater.
- `146.115` (W6SUV). This is the South Tahoe Amateur Radio Club repeater.
- `146.640` (W6SAR) at Donner Peak. This covers Truckee and I-80.
- `145.150` (N6ICW). This links to the Sacramento valley repeater network.
- `145.350` (KA6GWY). It supports EchoLink. RepeaterBook lists a non-standard
  `+0.855` MHz offset. A local listing shows `-0.600` MHz. Verify against the
  club page before transmit.

The national 2 meter calling frequency `146.520` is in the simplex section.

### Amateur 70 centimeter repeaters

Key 70 centimeter repeaters include:

- `442.825` (W6SUV) at Heavenly Valley. It covers the Tahoe Basin.
- `443.700` (WA6EWV). It has a full-time link with `146.865`.
- `442.300` (K5BLS) at East Peak. It supports System Fusion and analog.
- `440.700` (W6SAR) at Donner Summit. It covers I-80 and part of the basin.
- `441.750` (K1BMW) in Truckee.

The national 70 centimeter calling frequency `446.000` is in the simplex
section.

### Digital repeaters

The `442.475` repeater (WA6EWV) at East Peak is a DMR repeater. It uses color
code 3. An analog-only handheld does not decode DMR traffic. Keep it to
monitor activity, or to use if your radio has DMR.

### Alpine County simplex

The file keeps the Alpine County primary simplex frequency `147.420`. This is
useful in the area west of Lake Tahoe.

## Known limits

Repeaters change over time. Some go off-air, some change tone, and some move
frequency. Verify a repeater against its club page or RepeaterBook before you
rely on it in an emergency.

Some repeaters have a split tone. This means the transmit tone differs from the
receive tone. RepeaterBook marks these with the letter "s". This file sets a
single tone for both directions. Confirm the split tone before transmit.

The `145.350` (KA6GWY) repeater has a non-standard offset that is not the
common `0.600` MHz. It needs `+0.855` MHz. Do not assume the standard offset
for this one.

Several repeaters around Lake Tahoe use digital modes (DMR, System Fusion, or
WIRES-X). An analog-only handheld hears the analog side of a Fusion repeater,
but not a dedicated DMR repeater.

## Sources

- Tahoe Amateur Radio Association, "TARA Repeater and Sponsored Systems - 2026",
  http://tahoeamateurradio.com/tara_rpt.htm
- National Weather Service, Reno, "NOAA Weather Radio",
  https://www.weather.gov/rev/Radio
- RepeaterBook, "South Lake Tahoe, California Amateur Radio Repeaters",
  https://www.repeaterbook.com/repeaters/location_search.php?loc=South+Lake+Tahoe&state_id=06&type=city
- RepeaterBook, "Truckee, California Amateur Radio Repeaters",
  https://www.repeaterbook.com/repeaters/location_search.php?loc=Truckee&state_id=06&type=city
- RepeaterBook, "GMRS Repeater ID 2321 (Sierra Tract)",
  https://www.repeaterbook.com/gmrs/details.php?ID=2321&state_id=06
- RepeaterBook, "GMRS Repeater ID 2185 (Heavenly Valley)",
  https://www.repeaterbook.com/gmrs/details.php?ID=2185&state_id=06
- RepeaterBook, "Tahoe Amateur Radio Association",
  https://www.repeaterbook.com/repeaters/details.php?ID=2021&state_id=06
- RadioReference Wiki, "FRS/GMRS combined channel chart",
  https://wiki.radioreference.com/index.php/FRS/GMRS_combined_channel_chart
- FCC, "Multi-Use Radio Service (MURS)",
  https://www.fcc.gov/wireless/bureau-divisions/mobility-division/multi-use-radio-service-murs
- FCC, "General Mobile Radio Service (GMRS)",
  https://www.fcc.gov/wireless/bureau-divisions/general-mobile-radio-service-gmrs
- Tahoe Basin ARES Frequency Plan,
  http://sacvalleyares.org/contents/ARES%20Documents/Band%20Plans/2nd%20T-B%20Freq.%20plan%20Nov%202023.pdf
- Alpine County Frequency Plan,
  http://www.sacvalleyares.org/contents/ARES%20Documents/Band%20Plans/Alpine%20DCART-Freq-Plan.pdf
- SNARS, "Analog Repeaters",
  https://snars.org/repeaters/analog/
