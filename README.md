# Eat In

*You **do** have food at home.* Eat In is a phone app for cooking at home instead of ordering delivery. It tracks your fridge, freezer and pantry, shows which of your saved recipes you can make right now, keeps a shopping list and a cookbook, logs what you eat and how it made you feel, and works out how much you save by eating in.

## What it does (course requirements)

- **Installs on your phone.** It has a web app manifest, icons and a service worker, so "Add to Home Screen" gives it its own icon and its own full-screen window.
- **Saves your data between uses.** Groceries, shopping list, meal log, water, cookbook, goals, photos and settings are stored on the device.
- **Works without an internet connection.** The service worker caches the app, so everything works offline.
- **Uses the camera and vibration.** You can add photos of meals you made. Taps give a small vibration.
- **Calculates from your inputs.** It works out how long each grocery keeps and when to shop next, what a home-cooked plate costs from your grocery prices, how much you save versus ordering in, and your Eat In streak.
- **Charts your history over time.** Meal Log analytics, a 14-day water chart, a month calendar, and a savings chart against your goal.
- **Shares your progress.** It draws a certificate, a weekly recap and milestone badges as pictures on your phone, ready for a text or an Instagram Story. Nothing is shared unless you send it.

## Publish on GitHub Pages

1. Create a new **public** repository on github.com, for example `eat-in`.
2. Click **Add file → Upload files**. Drag in every file in this folder (there are no subfolders). Then click **Commit changes**.
3. Open **Settings → Pages**. Under **Build and deployment**, set Source to **Deploy from a branch**. Pick the **main** branch and the **/ (root)** folder, then click **Save**.
4. After a minute or two, the app is live at `https://<your-username>.github.io/eat-in/`.

## Put it on your phone

Use your GitHub Pages address, not a preview link, so your phone gets the Eat In icon.

- **iPhone:** open the address in Safari. Tap **Share**, then **Add to Home Screen**.
- **Android:** open the address in Chrome. Tap the **⋮** menu, then **Install app** (or **Add to Home screen**).

If you added an older version before, delete that icon from your home screen first. Phones keep the icon they saw the first time.

## No AI inside

Eat In was built with an AI coding tool (Claude Code), but the app itself uses no AI and calls no outside service. Every result it shows comes from fixed rules: how long each kind of food keeps, where each grocery goes, what a meal costs, how far you are toward your goals. Everything is saved only on your own phone.

## Photo credits

The three sample recipe photos come from recipe websites (including Real Housemoms and HelloFresh) and are used here for a class project only.

## Updating

After changing `index.html`, raise `CACHE` in `sw.js` (for example `eat-in-v80`) so phones pick up the new version.
