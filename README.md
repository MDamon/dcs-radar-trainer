# DCS Radar Trainer

An in-browser trainer for the air-to-air radar in the DCS F/A-18C Hornet and F-16C Viper.

**Try it: https://mdamon.github.io/dcs-radar-trainer/**

Three views are driven by the same simulated sky:

- **Radar page**: a replica of the Hornet's radar attack page or the Viper's FCR page, with working bezel buttons, cursor, designation and lock.
- **HUD**: target box, range, closure, and the close-in acquisition patterns.
- **Reality**: a top-down map and a side profile showing the true aircraft, the scan volume and the live beam.

Click the map to drop contacts (MiG-29, Tu-95, Mi-24, cruise missile, F-16C, KC-135), drag them around, and change their heading, speed and altitude. A table explains, for every contact, why the radar does or does not see it: below the scan, outside the azimuth, too small at that range, or in the Doppler notch.

Seven short lessons plus a sandbox cover reading the scope, antenna elevation, scan volume, designating and locking, track while scan, the notch, and the close-in modes. Switch aircraft with the tabs at the top (`#hornet` or `#f16` in the URL).

## What is simplified

This is a teaching model, not a copy of either radar. Detection is all-or-nothing, the notch is a fixed ±90 kt gate, bar spacing and scan speed are approximate, and the jet only flies level. Button positions, scan widths, cockpit control locations and DCS binding names were written from memory and have not been checked against the game, so verify them against the manuals and your bindings screen. Missiles, datalink, jamming and air-to-ground modes are not modelled.

## Running it

It is one static file. Open `index.html` in a browser, or serve the folder:

```
python3 -m http.server
```

Inspired by the BMS F-16 radar trainer shown in https://www.youtube.com/watch?v=nBQ0NL620Qs. Not affiliated with Eagle Dynamics.
