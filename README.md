<p align="center">
  <img src="docs/icon.png" width="128" height="128" alt="nDashMo app icon">
</p>

<h1 align="center">nDashMo</h1>

<p align="center"><b>Neue Dashboard with Emotion</b><br>
A car home screen for Android tablets and car head units.</p>

<p align="center">
  <img src="docs/screenshots/home-matte.jpg" width="49%" alt="nDashMo home screen, Matte theme">
  <img src="docs/screenshots/home-glass.jpg" width="49%" alt="nDashMo home screen, Glass theme">
</p>

nDashMo puts the map, music, clock, weather and your speed in one dashboard, and replaces your device's home screen.
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
- **Car power** (for a device that charges from the car): when the car is switched off, the music pauses and the
  screen sleeps; when it starts, the screen wakes to the home screen and the music carries on.
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

You need an Android tablet or car head unit with **Android 8 or newer** (see
[Will it work on my device?](#will-it-work-on-my-device)). No computer needed.

1. On the device, open this repo's [Releases](https://github.com/faizaldjoo/nDashmo-app/releases) in a browser and
   download the APK of the latest release (`nDashMo-<version>.apk`).
2. Open the downloaded file. Android asks to allow installing apps from your browser (or file manager): allow it,
   then tap **Install**. If Play Protect warns about an unknown developer, choose **More details > Install anyway**.
3. **Android 13 and newer:** Settings > Apps > nDashMo, then the ⋮ menu (top right) > **Allow restricted settings**.
   Without this, Accessibility and Notification access stay greyed out for an app installed from an APK.
4. Open nDashMo and allow **Location** (speed, map and weather).
5. Press **Home** and choose **nDashMo**, then **Always**. If nothing asks, set it under Settings > Apps > Default
   apps > Home app (the names differ a little between devices).
6. Open **Controls** (tap the battery pill at the top of the sidebar) > **Details**. The About page lists what is
   still off and opens the right setting for each:
   - **Notification access**: the song, the music controls and the turn card.
   - **Accessibility**: sleep when unplugged, wake when plugged in, split screen, recent apps and the edge strip.
   - The brightness bar asks once for **Modify system settings**.

### Will it work on my device?

nDashMo is built and tested on a Samsung Galaxy Tab A7 Lite (Android 14). It should also run on other Android
tablets and on Android car head units, with these limits:

- **Needs** Android 8 or newer on an ARM processor (nearly all tablets and head units; not the rare x86 head units).
- **Screen:** landscape, about 1024 x 600 or larger (common head units are 1024 x 600 or 1280 x 720; 8 to 10 inch
  tablets are fine). It always runs in landscape; very small screens (800 x 480) will feel cramped.
- **Split screen:** on Samsung (One UI) nDashMo opens it through One UI's own menu. On other devices it uses
  Android's own split screen, which most Android 7 to 11 tablets and head units allow; some devices and newer Android
  versions don't let apps start it, and nDashMo says so.
- **Bluetooth button:** Samsung's Bluetooth pop-up on Samsung, Android's Bluetooth settings on other devices.
- **Head units without a battery** are always "charging": the screen does not sleep when the car is switched off (the
  car powers the unit down itself), and the battery shows 100%.
- **Without Google services** (some head units), the place name may not show; the map, weather and speed still work.
- **Some head units do not let you change the Home app.** nDashMo then runs as a normal app you open from the app list.

Tried it on another device? Tell us how it went in an [issue](https://github.com/faizaldjoo/nDashmo-app/issues).

### Updating

Install the new APK over the old one: everything you set stays. On some devices an update switches nDashMo's
**Accessibility** off again; Controls shows a warning until you turn it back on (Settings > Accessibility >
Installed apps > nDashMo).

### Good to know

- The map, weather and speed limits need an internet connection (mobile data is fine).
- It never switches Bluetooth, Wi-Fi or mobile data by itself: those buttons open Android's own panels.

## Remove bloatware and ads (optional)

Android devices (tablets, car head units, phones) often come with apps you never use, and some show ads. nDashMo
does not remove apps itself (Android doesn't let a normal app do that), but you can do it in a few minutes from a
computer, letting an AI agent such as [Claude Code](https://claude.com/claude-code) do the typing. The tablet nDashMo
was developed on was cleaned up this way.

**What you need:** a computer (Mac, Windows or Linux) with Android's
[platform-tools](https://developer.android.com/tools/releases/platform-tools) (`adb`), on the same Wi-Fi as the device
(or a USB cable).

1. **On the device:** Settings > About phone / About tablet (on Samsung: About > Software information) > tap
   **Build number** 7 times.
   Then Settings > Developer options > **Wireless debugging** on > **Pair device with pairing code** (Android 11 and
   newer; on older devices or head units, turn on **USB debugging** and connect a cable instead).
2. **On the computer:** `adb pair <ip>:<port>` with the code the device shows, then `adb connect <ip>:<port>` (the
   address on the Wireless debugging screen). With a cable, skip this. `adb devices` should list the device.
3. **Start the AI agent** in a terminal and paste this:

   ```text
   My Android device is connected over adb (check with `adb devices`). First find out what it is
   (adb shell getprop ro.product.manufacturer, ro.product.model and ro.build.version.release) and tell me.
   Help me remove bloatware and ads safely:
   1. List the installed packages (adb shell pm list packages) and sort them into: ads and tracking,
      the maker's extras I probably don't need, and system apps I must keep. Use what you know about
      this maker and model.
   2. Show me the list and wait for my OK before removing anything. Never remove anything needed to start
      the device, the system UI, the launcher or home app I use, Settings, the keyboard, Wi-Fi, Bluetooth,
      phone / SIM / mobile data, Google Play services, the Play Store, or apps I tell you I use.
   3. Remove only what I approve, one by one, with `adb shell pm uninstall --user 0 <package>` (it can be
      undone), and save the list to removed-packages.txt.
   4. Write restore.sh, which puts every one of them back with `adb shell cmd package install-existing <package>`.
   ```

**Ads everywhere:** on the device, set **Private DNS** to an ad-blocking DNS. Samsung: Settings > Connections > More
connection settings > Private DNS; other devices: Settings > Network & internet > Private DNS. Choose "Private DNS
provider hostname" and enter `dns.adguard-dns.com`. It blocks most ads in apps and browsers, with no extra app and no
battery cost. To undo it, set Private DNS back to Automatic.

**To undo the clean-up:** run `restore.sh`, or put any single app back with
`adb shell cmd package install-existing <package>`. A factory reset also brings every app back.

**At your own risk.** Removing the wrong system app can break a feature (on some head units, the whole device), so
read the list before you approve it, and keep `removed-packages.txt` and `restore.sh`. Car head units often use their
own system apps for the radio, reversing camera, steering wheel buttons or CarPlay / Android Auto: tell the agent
which of those you use. When you are done, turn Wireless debugging (or USB debugging) off again.

## Report a problem

Open an [issue](https://github.com/faizaldjoo/nDashmo-app/issues): what happened, what you expected, your device's
make and model and its Android version, and a screenshot if you can. Controls > Details > **Drive log** shows what
nDashMo did and when (power in and out, the screensaver, split screen); a photo of it helps with anything to do with
the car.

New versions appear under [Releases](https://github.com/faizaldjoo/nDashmo-app/releases). Install the new APK over
the old one: your settings stay.

## Credits

Map data © OpenStreetMap contributors, OpenMapTiles, OpenFreeMap; MapLibre Native. Weather Open-Meteo, weather icons
Weatherglass. Icons Phosphor. Speed limits Overpass API. Screensaver face bbot by bwnd (MIT).
