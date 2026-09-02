# World Time Zones

An interactive globe showing the world's time zones, the day–night terminator, and the current
local time anywhere on Earth.

**Live:** https://laurencefwhite.github.io/world-time-zones/

## What it does

- **A rotating globe** with the 392 IANA time zones drawn as real boundaries, not rectangles —
  so the awkward ones (Kiribati, the Chatham Islands, the western tip of China) are where they
  actually are.
- **Local time and UTC** side by side, with the date, updating continuously.
- **Sunlight shading**, stepped at each twilight threshold — the sun 0°, 6°, 12° and 18° below the
  horizon, which is to say sunset, then civil, nautical and astronomical twilight. Cities are marked
  as being in daylight or darkness.
- **A time scrubber.** Drag or press play to run the clock forward and watch the terminator sweep
  across the globe.
- **Current weather** on cities — temperature, apparent temperature, humidity and wind.
- **Layers you can switch on and off:** cities, country outlines, country codes, zone boundaries,
  DST status, the graticule, labels, night shading, weather, and a slow spin.
- **Offset from UTC** shown in the legend.

## Running it

Open `index.html` in a browser. That is the whole procedure.

It is a single self-contained file — no build step, no server, no dependencies to install. The zone
boundaries are embedded in the page, which is why it is about a megabyte.

Two things do come from the network, and both fail quietly rather than breaking the page:

- **Fonts** (Inter and Spectral) from Google Fonts.
- **Weather** from the Open-Meteo API. Offline, or behind a strict content-security policy, the
  weather simply does not appear and everything else works.

## Data and credits

| | |
|---|---|
| Time zone boundaries | [timezone-boundary-builder](https://github.com/evansiroky/timezone-boundary-builder) 2026c |
| Clocks and offsets | IANA time zone database |
| Country outlines | Natural Earth |
| Weather | [Open-Meteo](https://open-meteo.com) |

The boundary data is derived from OpenStreetMap and carries the
[Open Database Licence](https://opendatacommons.org/licenses/odbl/), which requires attribution —
hence the credits shown on the page itself as well as here. Natural Earth is public domain, and the
IANA database is in the public domain.
