# Syd's Day — Setup Guide

A private schedule + goals app that lives on Syd's iPhone home screen like a real app.
Everything she does in it (checking off tasks, editing the schedule, tracking streaks)
is saved only on her own phone — there's no server, no login, no internet required
after the first visit.

---

## Part 1 — Put it online with GitHub Pages (free)

1. Go to [github.com](https://github.com) and create a free account if you don't have one.
2. Click the **+** in the top right → **New repository**.
   - Name it something like `syds-day`
   - Set it to **Public** (Pages needs this on the free plan)
   - Click **Create repository**
3. On the new repo page, click **uploading an existing file**.
4. Drag in all 6 files from this folder:
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `icon-192.png`
   - `icon-512.png`
   - `avatar.png`
5. Scroll down, click **Commit changes**.
6. Go to the repo's **Settings** tab → **Pages** (left sidebar).
7. Under "Build and deployment," set **Source** to `Deploy from a branch`, branch = `main`, folder = `/ (root)`. Click **Save**.
8. Wait about a minute, then refresh — GitHub will show a link like:
   `https://yourusername.github.io/syds-day/`

That link is the app. Anyone who opens it on their phone can use it — but since everything
saves locally, it's really just Syd's copy on her device.

---

## Part 2 — Add it to Syd's iPhone home screen

Send her the link (text, email, whatever), then have her:

1. Open the link in **Safari** (must be Safari, not Chrome, for this to work on iPhone)
2. Tap the **Share** button (square with an arrow, bottom of screen)
3. Scroll down and tap **Add to Home Screen**
4. Tap **Add**

Now there's an app icon on her home screen called **Syd's Day**. Opening it feels like a
normal app — full screen, no browser bar, works with airplane mode on after the first load.

---

## Part 3 — What she can customize herself, no coding needed

Inside the app, under the **Settings** tab:

- **Add / rename / recolor categories** — tap the color circle to change it, tap the name to rename
- **Export backup** — downloads a small file with everything saved, good to do occasionally
- **Import backup** — restores from that file (useful if she gets a new phone)

On the **Schedule** tab:

- Tap any block to edit its time, title, category, or delete it
- Tap **+ Add block** to add something new to that day
- Tap **Copy a day** to duplicate one day's plan into another (handy since weekdays often repeat)

On the **Goals** tab:

- Add anything she wants to build a streak on (not tied to a specific time)
- Tap **Mark done** each day to keep the streak going

---

## A note on the pre-loaded schedule

I loaded in what I could clearly read from her PDF — Monday is filled in as a full example,
and Sunday has Church + Relax. The PDF's table had merged cells that didn't translate cleanly
to text, so Tuesday–Saturday are currently empty. The fastest way to fill them in:

1. Open Monday (or Sunday), tap **Copy a day** from another day, then just edit the couple of
   blocks that are different for that day.

Should take her a few minutes per day once she's looking at her own sheet.

---

## Making changes later (for you)

Everything is in plain HTML/CSS/JS in `index.html` — no build step, no dependencies to install.
To change something: edit the file, re-upload it to the same GitHub repo (or edit directly in
GitHub's web editor — click the pencil icon on the file), and it updates live within a minute.
