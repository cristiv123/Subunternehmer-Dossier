# Subunternehmer-Dossier

A presentation of **Subunternehmer-Dossier** (in French: *Dossier sous-traitants*), a web application for the main contractor's
subcontractor file under Swiss joint liability (Art. 5 EntsG, Art. 8b EntsV): the
document state computed per firm, the whole subcontractor chain, reminders in each
firm's language, an on-site check on a phone, Excel import with a preview, and a
printable proof per site.

**→ https://cristiv123.github.io/Subunternehmer-Dossier/** — in German, French, Italian, English and
Romanian.

This repository contains the presentation page only. The application's source is
private. All data shown is invented; nothing here is legal advice.

---

## Refreshing the figures

Nine figures, in German and French — the application's interface exists in those two
languages only. The French page shows `shots/fr/`, every other language `shots/de/`
(`SHOT_LANG` in `index.html`).

They are taken by `video/screenshots.mjs` in the application's repository, against the
running demo (backend on 8090, frontend on 4300), at a 1360×850 viewport with
`deviceScaleFactor` 2, so 2720×1700:

```
node screenshots.mjs de --presentation <this repository>/shots
node screenshots.mjs fr --presentation <this repository>/shots
```

The script resets the demo data before and after, so the figures always show the same
invented firms and the check it saves for the phone figure does not stay behind.

Afterwards, **bump `SHOTS_VERSION` in `index.html`.** The images keep the same
addresses and GitHub Pages serves them with `Cache-Control: max-age=600`, so without a
new token a browser that has seen the page before goes on showing the old ones.

## Recounting the figures in §04

Counted by this method, in the application's repository, so the next count is the same
count:

```
git ls-files '*.java' '*.ts' '*.html' '*.scss' '*.sql' | xargs cat | wc -l
```

Tests are counted literally: `@Test` occurrences under `backend/src/test`, and `it(`
occurrences in `frontend/src/**/*.spec.ts`. The i18n figure is leaf keys per
translation file.
