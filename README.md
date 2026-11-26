# Eat In

*You **do** have food at home.* Eat In is a phone app for cooking at home instead of ordering delivery. It tracks your fridge and pantry, suggests meals from what you already have, keeps a cookbook of saved recipes, and logs what you eat, how it made you feel, and how much water you drank.

## What it does (course requirements)

- **Installs on your phone.** It has a web app manifest, icons and a service worker, so "Add to Home Screen" gives it its own icon and its own full-screen window.
- **Saves your data between uses.** Groceries, trips, food log, water, cookbook, photos and settings are stored on the device.
- **Works without an internet connection.** The service worker caches the app, so everything works offline.
- **Uses the camera and vibration.** You can add photos of meals you made. Taps give a small vibration.
- **Calculates from your inputs.** It works out the next grocery run from how long your food keeps. It splits a dish into meal-prep containers by size. It tracks water against a goal you set.
- **Charts your history over time.** Food log analytics show calories per day, which foods agree with you, and meals by time of day. There is also a 14-day water chart and a month calendar.

## Publish on GitHub Pages

1. Create a new **public** repository on github.com, for example `eat-in`.
2. Click **Add file → Upload files**. Drag in everything in this folder, including the `icons` and `vendor` folders. Then click **Commit changes**.
3. Open **Settings → Pages**. Under **Build and deployment**, set Source to **Deploy from a branch**. Pick the **main** branch and the **/ (root)** folder, then click **Save**.
4. After a minute or two, the app is live at `https://<your-username>.github.io/eat-in/`.

## Put it on your phone

- **iPhone:** open the address in Safari. Tap **Share**, then **Add to Home Screen**.
- **Android:** open the address in Chrome. Tap the **⋮** menu, then **Install app** (or **Add to Home screen**).

## No AI inside

Eat In was built with an AI coding tool (Claude Code), but the app itself uses no AI and calls no outside service. Every result it shows comes from fixed rules: how long each kind of food keeps, when the next grocery run falls due, how many containers a batch fills, how much water is left to reach your goal. Everything is saved only on your own phone.

## Updating

After changing `index.html`, raise `CACHE` in `sw.js` (for example `eat-in-v29`) so phones pick up the new version.
