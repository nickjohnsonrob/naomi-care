# Naomi Care Log

A simple, single-page web app for tracking a sick kid's fever and medication schedule. Built for grandpa — big buttons, clear status, big tappable emoji for mood, automatic reminders, one-tap export to share with Mom/Dad.

## What it does

- **Log temperature** and **log motrin dose** with one tap each
- **Mood emoji** captured with every reading (5 levels: playful → out of it)
- **Color-coded status** — green / amber / red based on the latest temp
- **Smart reminders** — "recheck temp in 1 hour after a dose", "next dose due around X", "over the 6-hour mark" (only fires if she's still feverish)
- **Warning list** with AAP-aligned red-flag symptoms and one-tap phone links
- **Export** to share the day's log with Mom/Dad
- **PIN gate** so random people with the link can't see anything
- **Works offline** — everything stored in the phone's browser, no server, no account

## How to use

Open the page in any phone browser. The PIN is `1972` (change it in `index.html` if you want). Bookmark the page on grandpa's phone. Tap a button, log, done.

## Data and privacy

- **All data lives in the phone's browser storage (localStorage).** Nothing is uploaded anywhere.
- Clearing browser history wipes the log. Use the **export** button at the end of the day to save a copy.
- The page is hosted on GitHub Pages but does not transmit data to GitHub or anywhere else.

## Editing

- **PIN** — change `const PIN = "1972";` near the top of the `<script>` in `index.html`
- **Phone numbers** — change `PHONE_DAD`, `PHONE_MOM`, `PHONE_DAD_TEL`, `PHONE_MOM_TEL` constants
- **Dose amount / interval** — `DOSE_INTERVAL_HOURS` constant (default 6)

## Sources

Warning thresholds and dosing guidance drawn from the American Academy of Pediatrics (healthychildren.org) and CDC pediatric guidance.
