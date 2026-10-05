# Airzone (IAQ) for Home Assistant

Custom integration that overrides the built-in `airzone` integration (same domain) and adds
the Airzone IAQ sensor (CO2, PM2.5, PM10, TVOC, pressure, air quality score).

It is based on the Home Assistant core `airzone` integration (2026.9.4) and depends on a
fork of [aioairzone](https://github.com/fabiencheret/aioairzone) that adds `/api/v1/iaq` support.

## Install with HACS

1. HACS → ⋮ → Custom repositories → add this repository, type **Integration**.
2. Install **Airzone (IAQ)** and restart Home Assistant.
3. Your existing Airzone config entry keeps working; IAQ entities appear under a new
   "IAQ Sensor" device.

The container needs `git` and internet access to install the library from GitHub.

## Notes

- Units are assumed (ppm, µg/m³, ppb, hPa); the Airzone API docs don't specify them.
- Home Assistant logs a warning that this overrides the core integration. That is expected.
- Licensed under Apache 2.0, like Home Assistant core.
