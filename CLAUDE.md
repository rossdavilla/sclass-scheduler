# Semester Grid (`sclass-scheduler`)

A teaching tool for building weekly class-schedule tables to paste into Google Docs. Live at
<https://rossdavilla.github.io/sclass-scheduler/>.

`README.md` covers what it does from the user's side. The notes here are for changing it.

## Layout

The whole app is the single `index.html` — HTML, CSS and JS inline, no build step, no
dependencies, everything client-side.

## The two things that are easy to break

- **"Copy table" has to survive a paste into Google Docs.** The copied markup is an 8-inch HTML
  table written for Docs' clipboard parser, and the `.doc` / `.html` downloads lean on the same
  markup. Docs drops most CSS, so the table carries inline attributes rather than classes.
  Changing the table markup means re-testing an actual paste into a Google Doc, not just the
  on-screen render.
- **Direct sync is an optional Google Apps Script Web App.** Ross pastes his own `…/exec` URL
  into the Direct sync box once and it is remembered in `localStorage`; the app then reads and
  writes whole schedules through it. Save/load by copy-pasted code must keep working without
  that URL — the sync is a convenience, never a requirement, and the URL is Ross's and belongs
  only in his browser, never in the repo.

## Publishing

GitHub Pages serves `main` from the repository root, so a push to `main` is the deploy. Already
listed in `data/sites.json` in the
[`rossdavilla.github.io`](https://github.com/rossdavilla/rossdavilla.github.io) repo under the
`tools` tag.
