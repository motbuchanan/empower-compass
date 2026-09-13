# Updating Empower Compass — city officials & data

You do not need to know how to code. Everything you'd change lives in one
labeled block near the top of `index.html`. Updating is: edit the text, save,
re-upload to GitHub. That's it.

As of EM 1.2 (Sep 13, 2026), all three cities are fully filled in from each
city's official website. This guide is for keeping it current going forward.

## Two ways to update

### 1. In the app (quick, per phone — for personal notes)
Tap the pencil on any card, type, Save. This only changes the app on THAT
phone. Use it for your own talking points. To change what everyone sees, use
method 2.

### 2. In the file (the real update — changes it for everyone)
1. Open `index.html` in the repo on GitHub, click the pencil (Edit).
2. Find the block starting with `var CITIES = {` near the top.
3. Each official looks like:
   `{id:'m-w4', name:'Bill Lamb', office:'Council · Ward 4', phone:'330-421-5829', email:'', web:'...', notes:''},`
   Edit the text between the quotes.
4. Change the version line near the top (`var VERSION = 'EM 1.2 · Sep 13';`)
   — bump the number AND put today's real date.
5. Bump `CACHE` in `sw.js` to match (e.g. `empower-compass-em1.3`).
6. Commit. Live within a minute.

## Marking something as unconfirmed
If you're mid-update and a card isn't verified yet, add `verify:true,` inside
its braces. Users see a small "Being updated" tag (no alarm, no gaps). Remove
it once confirmed. A card with an empty `name:''` shows "Coming soon."

## After the November 2026 election
Update `KEY_DATES`, `ELECTION_DAY`, and `DATA_VERIFIED` near the top for the
next election, and confirm officials in `CITIES` and `SHARED_SECTIONS`.

## Reporting problems
Users can tap More → "Found a problem?" which opens a pre-filled email to
democratsempowermedina@gmail.com with the app version and device info.

## Who maintains what
- **Your team** owns the content: officials, links, scripts, dates.
- **Mot** stands behind the build: if something breaks, that's his to fix.
Questions: motbuchanan.com
