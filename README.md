<p align="center">
  <img src="icons/icon128.png" alt="Defog — Glassdoor unblock extension logo" width="96" height="96">
</p>
<h1 align="center">Defog — Glassdoor Unblock Chrome Extension</h1>
<p align="center">A free Chrome extension that removes Glassdoor's blur overlay, paywall and login prompts — read company reviews and salaries without signing up.</p>

## What it does

Glassdoor blurs review content, drops sign-in-to-unlock buttons over reviews, truncates long text behind a "continue reading" link, and layers cookie/login banners on top of everything until you create an account. Defog is a lightweight Chrome extension that strips all of that out as the page loads, so the content is readable straight away — no Glassdoor account required.

Specifically, it:

- Removes the blur overlay, the "sign in to unlock" button and the review "expand" button
- Un-truncates collapsed review text and the employer hero image
- Removes the login/cookie-consent banners and the "continue reading" prompt
- Re-enables scrolling on pages Glassdoor locks in place behind those banners
- Keeps working as you scroll/paginate, by watching the page for new content

The toolbar popup gives you a master on/off switch **per site** (so you can pause it on a specific Glassdoor domain without affecting the others) and a live counter of how many elements it has hidden on the current page.

![Before and after Defog is applied to a Glassdoor company review page](before-after.jpg)

## Supported sites

Defog works on the localized Glassdoor site for each of these countries: US, Italy, UK, Canada, Australia, Ireland, Germany, France, Netherlands, Switzerland, Austria, Belgium, Spain, India, Hong Kong, Singapore, New Zealand, Mexico and Brazil.

## Why isn't this on the Chrome Web Store?

Because it strips out Glassdoor's paywall and sign-up prompts, this extension almost certainly runs afoul of the Chrome Web Store's policies (and probably Glassdoor's Terms of Service too). Rather than risk a takedown — or worse — it's distributed here as source only, and you load it yourself. Use it at your own discretion.

## Installing it in Chrome or a Chromium-based browser

Since it's not on the Web Store, you install it as an "unpacked" extension. This works the same way in Chrome, Edge, Brave, Opera, Vivaldi, Arc and any other Chromium-based browser — just swap in that browser's equivalent of `chrome://extensions`.

1. Download this repository (`Code → Download ZIP` on GitHub, then unzip it — or `git clone` it if you have Git).
2. Open `chrome://extensions` (or your browser's equivalent, e.g. `edge://extensions`, `brave://extensions`).
3. Turn on **Developer mode** (top-right toggle).
4. Click **Load unpacked** and select the folder you just downloaded (the one containing `manifest.json`).
5. The Defog icon appears in your toolbar. Pin it for easy access via the puzzle-piece icon next to the address bar.

### Keeping it up to date

Unpacked extensions don't auto-update. To get the latest version, pull the latest changes (or re-download the ZIP) and click the refresh icon for Defog on `chrome://extensions`.

## FAQ

**Is this safe to use?**
Yes — Defog only hides/unhides DOM elements on pages you already have open. It doesn't send any data anywhere; see the source in this repo.

**Do I need a Glassdoor account?**
No. Defog removes the sign-in wall so you can read reviews and salary data without creating an account.

## Found a bug?

[Open an issue](https://github.com/lprevidente/defog-glassdoor-unblock/issues) — the popup also has a "Report it" link that goes to the same place.

## License

Code is MIT-licensed — see [LICENSE](LICENSE). The bundled fonts (Space Grotesk, Instrument Sans, IBM Plex Mono) are separately licensed under the SIL Open Font License 1.1; their license texts live alongside them in `fonts/`.
