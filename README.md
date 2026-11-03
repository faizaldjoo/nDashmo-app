<p align="center">
  <img src="docs/icon.png" width="128" height="128" alt="nDashMo app icon">
</p>

<h1 align="center">nDashMo</h1>

<p align="center"><b>Neue Dashboard with Emotion</b><br>
A car home screen for an Android tablet as your car head unit.</p>

<p align="center">
  <img src="docs/screenshots/home-matte.jpg" width="49%" alt="nDashMo home screen, Matte theme">
  <img src="docs/screenshots/home-glass.jpg" width="49%" alt="nDashMo home screen, Glass theme">
</p>

nDashMo puts the map, music, clock, weather and your speed in one dashboard, and replaces the tablet's home screen.
It has two looks: **Matte** (flat and dark, with a light version by day) and **Glass** (see-through panels over a photo
wallpaper). Built and tested on a Samsung Galaxy Tab A7 Lite (Android 14, One UI 6.1). Made by
[@faizald.jo](https://www.threads.com/@faizald.jo).

## What it does

- **Map**: a tilted driving view that turns with the car, the street you are on, and the speed limit when
  OpenStreetMap knows it. With Google Maps navigating, the next turn and the arrival time show on the map. Tap the map
  to open Waze or Google Maps.
- **Today**: a flip clock, the weather where you are, and the place name.
- **Car**: GPS speed, a compass, a speed bar, and the trip (distance, driving time, average). The trip starts again
  each time the car is switched off.
- **Music**: whatever is playing (YouTube Music, Spotify, radio apps), shown as a cassette, with the controls.
  Long titles scroll.
- **Volume and brightness** bars, and a thin strip on the screen edge to change them over other apps.
- **Sidebar**: battery and connection, split screen with two apps, your pinned and recent apps, All apps.
- **Car power**: unplug the charger (car off) and the music pauses and the screen sleeps; plug in (car on) and it
  wakes to the home screen and the music carries on.
- **Screensaver**: a friendly face (bbot) with the clock and the song, after 5 minutes without a touch while
  charging. Play with it: hold, rub, double tap.
- **Gestures**: swipe left for All apps, right for the screensaver; two fingers up or down for volume, right for
  recent apps, left for the last split screen.

<p align="center">
  <img src="docs/screenshots/all-apps.jpg" width="32%" alt="All apps">
  <img src="docs/screenshots/controls.jpg" width="32%" alt="Controls">
  <img src="docs/screenshots/wallpaper.jpg" width="32%" alt="Wallpaper picker (Glass)">
</p>
<p align="center">
  <img src="docs/screenshots/screensaver.jpg" width="49%" alt="Screensaver">
</p>

## Install the APK

You need an Android tablet (or car head unit) with **Android 8 or newer**. No computer needed.

1. On the tablet, download `nDashMo-1.0.apk` from this repo's
   [Releases](https://github.com/faizaldjoo/nDashmo-app/releases).
2. Open it. Android asks to allow installing apps from your browser (or Files): allow it, then tap **Install**.
   If Play Protect warns about an unknown developer, choose **More details > Install anyway**.
3. **Android 13 and newer:** Settings > Apps > nDashMo > ⋮ (top right) > **Allow restricted settings**. Without this,
   Accessibility and Notification access stay greyed out for an app installed from an APK.
4. Open nDashMo and allow **Location** (speed, map and weather).
5. Press **Home** and choose **nDashMo**, then **Always** (or Settings > Apps > Default apps > Home app).
6. Open **Controls** (tap the battery pill at the top of the sidebar) > **Details**. The About page lists what is
   still off and opens the right setting for each:
   - **Notification access**: the song, the music controls and the turn card.
   - **Accessibility**: sleep when unplugged, wake when plugged in, split screen, recent apps and the edge strip.
   - The brightness bar asks once for **Modify system settings**.

### Updating

Install the new APK over the old one: everything you set stays. On some tablets an update switches nDashMo's
**Accessibility** off again; Controls shows a warning until you turn it back on (Settings > Accessibility >
Installed apps > nDashMo).

### Good to know

- The map, weather and speed limits need an internet connection (mobile data is fine).
- Split screen and the Bluetooth pop-up work on Samsung tablets (One UI); the rest works on any Android tablet.
- nDashMo is designed for a landscape screen around 8 to 10 inches.
- It never switches Bluetooth, Wi-Fi or mobile data by itself: those buttons open Android's own panels.

## Report a problem

Open an [issue](https://github.com/faizaldjoo/nDashmo-app/issues): what happened, what you expected, your tablet
(or head unit) model and Android version, and a screenshot if you can. Controls > Details > **Drive log** shows what
nDashMo did and when (power in and out, the screensaver, split screen); a photo of it helps with anything to do with
the car.

New versions appear under [Releases](https://github.com/faizaldjoo/nDashmo-app/releases). Install the new APK over
the old one: your settings stay.

## License

© 2026 [@faizald.jo](https://www.threads.com/@faizald.jo). All rights reserved. You may download, install and use the
nDashMo app from this repo's Releases. You may not copy, modify, rebuild, publish or redistribute the code, the design
or the app, in whole or in part, without written permission. See [LICENSE](LICENSE). The third-party parts listed
under Credits keep their own licenses.

## Credits

Map data © OpenStreetMap contributors, OpenMapTiles, OpenFreeMap; MapLibre Native. Weather Open-Meteo, weather icons
Weatherglass. Icons Phosphor. Speed limits Overpass API. Screensaver face bbot by bwnd (MIT).
