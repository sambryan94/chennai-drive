# Chennai Drive

A lightweight browser driving game around Velachery and Guindy, Chennai.

## Latest build

This repository contains the tested September 14 build from source commit `0257a2f19c3c93e42395e9369dfb6f070029252d`. The root contains the ready-to-host static game (18 files, 1,080,027 bytes). The editable project, tests and documentation are in `source/`.

- Real OpenStreetMap road geometry and 24 named interior streets.
- Solid map boundary, sidewalk traffic signals, 50 m streetlight stations and lit shop/building windows.
- Temporary SUV, automatic transmission, eight-second rechargeable turbo, traffic, pedestrians and day/night mode.
- Chase and bonnet cameras, compact mobile controls, simple speed/gear/RPM instruments and grouped sound controls.

## Host on Vercel

Import this repository into your existing Vercel project. Choose **Other** as the framework, keep the root directory at the repository root, leave Build Command and Install Command empty, and use `.` as the Output Directory if requested. The game is already compiled.

Alternatively, from this repository's root:

```sh
npx vercel@59.16.0 login
npx vercel@59.16.0 link --yes --scope sam-2717 --project chennai-afternoon-drive
npx vercel@59.16.0 deploy --prod --yes
```

Uploading to GitHub does not itself publish a live website. GitHub Pages can serve these root static files if enabled in repository settings.

## Run locally

With Python installed, run `python -m http.server 8080` here and open http://localhost:8080. Serve through HTTP; opening index.html as a file URL will not work correctly.

## Controls

WASD/arrows: drive; Shift: turbo; Space: handbrake; C: camera; R: recover; Escape: pause. Touch pedals and steering are available. Sound channels are grouped under Sound.

## Source and evidence

See [source README](source/README.md), [architecture](source/ARCHITECTURE.md), [vehicle tuning](source/VEHICLE_TUNING.md), [test report](source/TEST_REPORT.md) and [map sources](source/MAP_DATA.md). The original development scaffold is retained under source; its environment-specific wrapper is not needed to host this compiled game.

81 automated checks passed, with browser driving verification. Physical HP Envy performance has not been measured. Scenery and elevations are simplified; this is not surveyed navigation or a photorealistic city. The SUV is a clearly temporary substitute.

## Attribution

Map data © OpenStreetMap contributors, available under ODbL. Keep the in-game attribution visible. Downloadable road and POI exports are in `data/`. Third-party library notices are in `licenses/`. No API keys or downloaded commercial map tiles are required. See source/MAP_DATA.md for licensing and update details.

![Night driving](source/evidence/osm-night.jpg)
![Mobile controls](source/evidence/osm-mobile.jpg)
