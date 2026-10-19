# Sidesy: Your Comments Sidebar For YouTube

A browser extension for Chrome and Firefox that brings the comments section to the sidebar, so you can dive into the comments without scrolling past the video.

![sidesy](images/name-card.png)

## Installation

1. [Chrome Web Store](https://chromewebstore.google.com/detail/sidesy-your-comments-side/fjonckloandknnijadolfebflfgjchne)
2. [Firefox Add-ons (AMO)](https://addons.mozilla.org/en-US/firefox/addon/sidesy/)
3. [Local Installation](#local-installation)

## Features

1. Built for convenience with an eye for aesthetics. Unlike other similar options in the market, the sidebar comments don't feel out of place. They look nice and work well.
2. Dark & light modes depending on your YouTube settings.
3. Easy toggle integrated right into the comments section to easily switch between default and sidebar views.
4. Full-height sidebar — switch comments to full height from the header button or press **Z**.
5. Fold comments into a slim bar — press **X** or use the header button to collapse and expand.
6. Keyboard shortcut **Alt + Shift + S** to toggle the sidebar from anywhere on the page.

## Showcase

![showcase-image-1](images/1.png)
![showcase-image-2](images/2.png)
![showcase-image-3](images/3.png)

## Local Installation

### Chrome / Chromium-based browsers (Chrome, Brave, Edge)

1. Clone the repo
2. Navigate to `chrome://extensions/`
3. Turn on **Developer Mode** at the top right
4. Click **Load Unpacked** and select the repo folder

### Firefox

**Option A — `web-ext run` (live reload, lasts while the command is running)**

Best for active development. The extension is active only while `web-ext run` is running and is removed when the process exits or Firefox closes.

1. Clone the repo
2. Install web-ext if you haven't: `npm install -g web-ext`
3. Run `web-ext run` from inside the repo folder
4. Firefox will open with the extension loaded and live-reload on any file change

**Option B — Load Temporary Add-on (no tooling needed, lasts until Firefox closes)**

Quickest way to test without any extra tools. The extension is removed every time Firefox closes and must be reloaded manually.

1. Clone the repo
2. Navigate to `about:debugging#/runtime/this-firefox`
3. Click **Load Temporary Add-on** and select any file inside the repo folder (e.g. `manifest.json`)

**Option C — Install from `.zip` via `web-ext build` (permanent, requires a flag)**

Installs the extension permanently — it survives Firefox restarts just like a store-installed extension. However, Firefox enforces extension signing on most channels, so you need to disable that check first.

> **Supported Firefox editions only:** `xpinstall.signatures.required` can be set to `false` on **Firefox Developer Edition**, **Firefox Nightly**, and **Firefox ESR**. It has no effect on **Firefox Release** or **Firefox Beta** — the preference is hardcoded there and cannot be overridden.

1. Clone the repo
2. Build the zip: `web-ext build` (output goes to `web-ext-artifacts/`)
3. In Firefox, open `about:config`, search for `xpinstall.signatures.required`, and set it to `false`
4. Go to `about:addons`, click the **⚙ gear icon**, and select **Install Add-on From File...**
5. Select the `.zip` file from `web-ext-artifacts/`
6. The extension is now installed permanently and persists across restarts
