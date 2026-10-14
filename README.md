# Weather nowcast — bar widget for Omarchy

Rain for the next two hours, at radar resolution, in the Omarchy 4 bar.
Mirrors the `mmb.rainnowcast` plugin generated from
[Hizoul/rusty-bui](https://github.com/Hizoul/rusty-bui) (see there for
sources, tests and the full weather window).

## Install

The widget runs the `rustybui` binary (fetching, caching and rate limiting
live there). Install it first — build it:

```bash
git clone https://github.com/Hizoul/rusty-bui.git && cd rusty-bui && ./install.sh --no-plugins
```

…or grab a prebuilt tarball from
[Releases](https://github.com/Hizoul/rusty-bui/releases) and unpack it into
`~/.local/bin`. Then:

```bash
omarchy plugin add https://github.com/Hizoul/omarchy-weather-nowcast.git --enable
```

Set your location: `rustybui set-location "Leiden" --lat 52.16 --lon 4.49 --country NL --timezone Europe/Amsterdam`.

Remove it with `omarchy plugin remove mmb.rainnowcast` and delete the binary
at `~/.local/bin/rustybui` (plus the caches under `~/.cache/rustybui`, if you
want them gone too).

## Attribution

Nowcast from KNMI radar (NL, CC BY 4.0), DWD/Bright Sky radar (DE,
CC BY 4.0), Open-Meteo minutely-15 fallback. GPL-3.0-or-later.
