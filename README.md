# For You ❤️ — a digital love story

A single-page romantic website, built for one person to open.

## How to personalize it

Open `index.html` in any text editor and find the `CONFIG` object near the
top of the `<script>` section (right after the `<body>` tag). Everything
you need to change lives there:

- `HIS_NAME`, `YOUR_NAME`, `BIRTHDAY_DATE`
- `BACKGROUND_MUSIC` — path to your music file (see below)
- `LOVE_LETTER` — your own words, replaces the placeholder
- `TIMELINE` — six moments in your story (date, title, description, optional photo)
- `MEMORIES` — the gallery, 10 placeholders ready to fill
- `THINGS_I_LOVE` — the ten flip cards
- `OUR_WORLD` — favorite song, movie, place, food, inside joke, etc.
- `BUCKET_LIST` — add or remove lines freely, it's a plain list
- `SECRET_MESSAGE` — shown when the hidden heart (bottom-left corner) is tapped 5 times

## Adding real photos

1. Create a `photos` folder next to `index.html` (already included, empty).
2. Drop your images in — JPG or PNG, ideally under ~500KB each so the page stays fast.
3. In `CONFIG.MEMORIES`, add `src: "photos/yourfile.jpg"` to any entry.
   Example:
   ```js
   { src: "photos/us-at-the-beach.jpg", caption: "One of my favorite days ❤️", ar: 1.1 }
   ```
   `ar` is the photo's aspect ratio (width ÷ height) — it keeps the gallery
   grid tidy even before the image loads. A square photo is `1`, a portrait
   phone photo is roughly `0.75`.
4. Timeline photos work the same way — just add `photo: "photos/yourfile.jpg"`
   to any item in `CONFIG.TIMELINE`.

## Adding music

1. Put an MP3 in the included `music` folder (e.g. `music/our-song.mp3`).
2. Set `BACKGROUND_MUSIC: "music/our-song.mp3"` in the config.
3. Music will not play until he taps "Open Your Surprise" — this is a
   browser rule, not a bug, and it also means the surprise gets a proper
   musical entrance. The note icon top-right toggles play/pause anytime.

## Trying it out

Just double-click `index.html` — it opens in any browser, no installation
needed. For music and photos to load correctly, keep the `music` and
`photos` folders in the same place as `index.html`.

## Sending it to him

Easiest options:
- Zip the whole folder (`index.html` + `music` + `photos`) and send it directly.
- Or host it for free in a couple of minutes on Netlify Drop
  (netlify.com/drop) or GitHub Pages — drag the folder in, get a shareable link.

## The hidden surprise

There's a small, faint heart (♡) in the bottom-left corner of the page.
Tap it five times to unlock a secret message — edit it in
`CONFIG.SECRET_MESSAGE`.
