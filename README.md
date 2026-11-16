# Daybook

**A calm, paper-like notebook for your week.** Plan your timetable, protect what matters, and let the day tick itself off.



Daybook is a single-page app with no account, no server, and no build step. It opens like a notebook: a week spread, a page for each day, and a margin for what matters most. Everything you write stays in your browser.

## Why it feels good

- **A real timetable** — a quiet weekly grid from early morning to late night. Click an empty slot to add something, or drag an entry to move it.
- **★ Priorities that stand out** — pin the tasks that matter. They get a warm glow, a star on every view, and their own “Priority today” section in the margin.
- **Gentle reminders** — 10 minutes before a pinned task, Daybook nudges you with an in-app card (and a browser notification when you allow it). No noise for everything else.
- **A page per day** — a focused list with times, categories, notes, and a completion circle you can actually click.
- **Daily check-offs** — every date has its own progress. Monday’s lecture can be done this week and waiting again next week.
- **Notes that save themselves** — a lined note box for every date, saved as you type.
- **A living background** — layered paper, warm light, soft drifting orbs, and a little grain. Not a plain white page.
- **Light & dark** — warm daylight paper, and a lamp-lit evening version.
- **Yours to keep** — export/import as JSON. Data lives in `localStorage`; there is no tracking and no backend.


  
## Install it as an app

Daybook is a PWA, so it can live in your dock, taskbar, or home screen and work offline.

| Where | How |
| --- | --- |
| **Chrome / Edge (desktop)** | Open the [live app](https://arushvarma.github.io/daybook/), then click the install icon in the address bar — or the download button in Daybook’s toolbar. |
| **iPhone / iPad** | Open the live app in Safari → **Share** → **Add to Home Screen**. |
| **Android** | Open the live app in Chrome → **⋮** → **Install app** (or “Add to Home screen”). |

The live site needs a one-time GitHub Pages deploy (see [Publishing](#publishing-this-repo)). Until then, the app still runs perfectly by opening `index.html`.

## Download and run it yourself

**Option 1 — download the ZIP**

1. Click **Code → Download ZIP** on GitHub and unzip it.
2. Open `index.html` in any modern browser.
3. Optional: serve the folder locally so offline caching and installation work:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

**Option 2 — clone**

```bash
git clone https://github.com/arushvarma/daybook.git
cd daybook
open index.html
```

No npm, no bundler, no dependencies.

## Shortcuts

| Key | Action |
| --- | --- |
| `N` | New entry |
| `T` | Jump to today |
| `W` / `D` | Week / Day view |
| `←` / `→` | Previous / next week or day |
| `Esc` | Close the editor |

## How your data works

- The timetable is a **weekly template**: editing “Deep work” on Monday changes every Monday. Check-offs and notes belong to the actual date.
- State is stored in `localStorage` under `daybook.v1`.
- A sample student week is seeded on first run so the notebook isn’t empty. Clear it with the trash button when you’re ready for your own.
- Export a JSON backup before switching browsers or clearing site data.
- Reminders are on by default. The bell in the toolbar turns them off/on; browser notifications are requested only when you enable them.
- Reminders are checked while Daybook is open. It does not schedule push notifications while the app is closed.

## Project structure

```text
.
├── index.html                  # the whole app — markup, styles, and logic
├── manifest.webmanifest        # name, icons, colours for installation
├── sw.js                       # offline cache
├── icons/                      # app icons (SVG source + PNG exports)
├── docs/                       # screenshots used by this README
├── .github/workflows/pages.yml # deploy to GitHub Pages on every push
└── LICENSE
```

## AI-assisted development

Daybook was created with help from AI tools, which contributed to parts of the design and code. The project is being developed as a portfolio piece, and its author is responsible for reviewing, understanding, and maintaining the work they present.

## Publishing this repo

These are the one-time steps to put Daybook online:

1. Create an empty **public** repository named `daybook` on GitHub (no README, no `.gitignore`).
2. In the new repository, open **Settings → Pages** and set **Source** to **GitHub Actions**.
3. From this folder, push the project:

```bash
git branch -M main
git remote add origin https://github.com/arushvarma/daybook.git
git push -u origin main
```

The first commit is already made. If you started from a downloaded copy instead, run `git init` and commit once before adding the remote.

4. Open the **Actions** tab and wait for “Deploy Daybook to GitHub Pages” to finish. The app will be at `https://arushvarma.github.io/daybook/`.

If the first deploy fails because Pages is not enabled yet, enable it as in step 2 and re-run the workflow from the **Actions** tab.

If your GitHub username is different, replace `arushvarma` in the links above and in `README.md`.

## License

[MIT](LICENSE) — use it, fork it, make it yours.
