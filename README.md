# World Time Zones

An interactive globe showing the world's time zones, the day–night terminator, and the current
local time anywhere on Earth.

**Live:** https://laurencefwhite.github.io/world-time-zones/

## What it does

- **A rotating globe** with all 444 IANA time zones drawn as real boundaries, not rectangles — 418
  on land, plus the 26 nautical zones that cover the oceans — so the awkward ones (Kiribati, the
  Chatham Islands, the western tip of China) are where they actually are.
- **Local time and UTC** side by side, with the date, updating continuously.
- **Sunlight shading**, stepped at each twilight threshold — the sun 0°, 6°, 12° and 18° below the
  horizon, which is to say sunset, then civil, nautical and astronomical twilight. Cities are marked
  as being in daylight or darkness.
- **The local time in every zone**, set large above that zone's UTC offset and its code — so you can
  read the world's clocks at a glance rather than doing the arithmetic.
- **A time scrubber.** Drag or press play to run the clock forward and watch the terminator sweep
  across the globe.
- **Current weather** on cities — temperature, apparent temperature, humidity and wind, in Celsius
  or Fahrenheit.
- **A slow spin**, on by default. **Click the globe to stop it, and click again to start it** — a
  drag still spins it by hand, and clicking a city still flies to that city.
- **On a touch screen**, where there is no hovering, one tap does the looking and a second does the
  going. A tap on the globe reads whatever is under it and holds the globe still: a city gives its
  clock and its weather, open country or open water gives the zone. Tapping a selected city again,
  or its card's *Fly to* button, flies there; a tap anywhere else puts it down and lets the globe
  turn again. Only a tap off the globe altogether starts and stops the turning, which is what a
  click does with a pointer. The card sits above your finger rather than under it, the target around
  a city is wider, and the panels fold into the corners with only one open at a time, so a tap on
  the globe clears the way.
- **A Reset view pill.** When the layers panel is folded away, Reset view comes out and sits beside
  the folded pill, so the one control worth having to hand is always there.
- **Layers you can switch on and off:** time zones, countries, sun and shadow, city markers, city
  names, zone offsets, zone codes, local times, the graticule, daylight saving, weather,
  Fahrenheit, and the spin. City names imply the markers, so switching names on brings the markers
  with them.
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
