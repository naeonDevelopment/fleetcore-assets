# fleetcore-assets

Public host for **cleared** FleetCore social and marketing assets — document carousels, mechanism
diagrams, covers and short video. It exists for one reason: LinkedIn scheduling APIs reference assets by
URL and cannot upload files, so a published asset needs a fetchable address.

**This is a publication surface, not a working one.** Source lives in the FleetCore workspace; only
finished, gate-passed output lands here.

## Structure

```
carousels/<YYYY-MM-DD>_<topic-kebab>_v<semver>/
    <same-stem>.pdf              1080×1350 (4:5) or 1080×1080 (1:1)
    <same-stem>_cover.png        required — a document post needs a thumbnail
diagrams/<YYYY-MM-DD>_<topic-kebab>_v<semver>.png
video/<YYYY-MM-DD>_<topic-kebab>_v<semver>.mp4
```

Same stem, same version, extension changed. Lowercase kebab, ASCII, no spaces. The date is the **content
date**, not the upload date.

Raw URL: `https://raw.githubusercontent.com/<owner>/fleetcore-assets/main/<path>`

## What may be pushed here

Only an asset that has **already passed the promotion gate** and is cleared to appear publicly.
**Pushing is publishing.** If it is not ready for LinkedIn, it is not ready for this repository.

## What may never be pushed here

1. **Anything from the workspace `Resources/` tree.** It holds customer operational data, executed
   agreements, incorporation documents and finance records.
2. **Any real vessel name, IMO number, position, voyage, consumption figure or crew detail** — including
   inside a screenshot, a chart axis, a filename or PDF metadata.
3. **Any customer or prospect name** without a written reference consent on file.
4. **Any synthetic figure formatted to look like a real reading.** Demo content uses the sanctioned
   fixture set, whose vessel names are obviously fictitious and whose IMO numbers are invalid by
   construction — so a leaked screenshot is self-evidently synthetic.
5. **Any unmarked number or uncleared claim.** Every figure carries its proof mark; every claim traces to
   a register row.
6. **Any class society logo or mark placed adjacent to the product.** Layout adjacency is a
   certification claim whether or not a sentence makes one.

## Before you push

- [ ] The asset passed its gate and is cleared for public release
- [ ] Fonts embedded, no fallback (`pdffonts` names every family, `emb=yes`)
- [ ] Cover renders legibly at 200 px wide — **look at it**
- [ ] Alt text written and stored with the post, not here
- [ ] No real vessel, customer, crew or financial data anywhere in the file **or its metadata**
- [ ] Filename carries the content date and version

## If something wrong is pushed

**Deleting the file does not unpublish it.** Git history and raw-URL caches persist, and the repository
is public and indexable. Treat it as a disclosure, not a tidy-up: say so immediately to the owner, state
what was exposed and for how long, and follow the confidentiality escalation path. Do not investigate
quietly first — notification clocks start at discovery, not at confirmation.

## Licence

Assets are © FLEETCORE LTD, all rights reserved. Public hosting is for distribution, not a grant of
reuse.
