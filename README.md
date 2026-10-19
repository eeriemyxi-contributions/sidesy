# Sidesy: Your Comments Sidebar For YouTube

A browser extension for Chrome and Firefox. Comments move to a sidebar so you can read them without scrolling past the video.

![sidesy](images/name-card.png)

## Installation

1. [Chrome Web Store](https://chromewebstore.google.com/detail/sidesy-your-comments-side/fjonckloandknnijadolfebflfgjchne)
2. [Firefox Add-ons (AMO)](https://addons.mozilla.org/en-US/firefox/addon/sidesy/)
3. [Local Installation](#local-installation)

## Features

- Comments load in a sidebar to the side of the video, so you never lose your place.
- Follows your YouTube dark/light mode setting.
- Toggle button built into the comments section to switch between sidebar and default views.
- Full-height mode: press **Z** or use the header button to stretch the sidebar to the full window height.
- Fold mode: press **X** or use the header button to collapse the sidebar to a slim bar. Press again to expand.
- Press **Alt + Shift + S** anywhere on the page to toggle the sidebar.

## Showcase

![screenshot 1](images/1.png)
![screenshot 2](images/2.png)
![screenshot 3](images/3.png)

## Local Installation

### Chrome, Brave, Edge

1. Clone the repo.
2. Go to `chrome://extensions/`.
3. Turn on **Developer Mode** (top right).
4. Click **Load Unpacked** and select the repo folder.

### Firefox

**Option A: `web-ext run` — active while the command runs**

Reloads the extension automatically on file changes. Stops when you kill the process or close Firefox.

1. Clone the repo.
2. Run `npm install -g web-ext` if you do not have it.
3. Run `web-ext run` from inside the repo folder.

**Option B: Load Temporary Add-on — active until Firefox closes**

No extra tools needed. Firefox removes the extension on every close; you must reload it manually each session.

1. Clone the repo.
2. Go to `about:debugging#/runtime/this-firefox`.
3. Click **Load Temporary Add-on** and select any file in the repo folder (e.g. `manifest.json`).

**Option C: Install from zip — permanent**

The extension survives restarts, the same as a store-installed one. Firefox blocks unsigned extensions on most channels, so you need to turn off signature enforcement first.

> [!WARNING]
> `xpinstall.signatures.required` only works on **Firefox Developer Edition**, **Firefox Nightly**, and **Firefox ESR**. On Firefox Release and Beta the preference is hardcoded to `true` and changing it has no effect.

1. Clone the repo.
2. Run `web-ext build`. The zip lands in `web-ext-artifacts/`.
3. In Firefox, go to `about:config`, find `xpinstall.signatures.required`, and set it to `false`.
4. Go to `about:addons`, click the gear icon, and select **Install Add-on From File**.
5. Pick the zip from `web-ext-artifacts/`.
