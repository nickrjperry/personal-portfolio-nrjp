# Portfolio site

One HTML file, one images folder, no build step, no dependencies.

## Files

```
index.html      the whole site: markup, styles, animations
images/         01-problem.png, 01-solution.png, 01-outcome.png (Dragon Copilot)
                nick.jpg (portrait in the contact section)
README.md       this file
```

Open `index.html` in a browser to preview locally. That is the whole workflow.

## Deploy

**Cloudflare Pages or Netlify, via GitHub (recommended)**

1. Create a repo on GitHub and upload `index.html` and the `images` folder.
2. In Cloudflare Pages or Netlify, connect the repo.
3. Framework preset: none. Build command: leave empty. Output directory: `/`.
4. Deploy. You get a free subdomain immediately, and a custom domain is a DNS record away.

Ongoing edits: change the text in GitHub's web editor and commit. Live in about thirty seconds.

**Netlify Drop, if you never want to touch git**

Drag this folder onto app.netlify.com/drop. Re-drag the folder to update. No version history, no browser editing.

## Editing

Everything worth changing is near the top of `index.html`, in the comment block:

1. Surname. Search `Nick` in the nav mark, hero and footer wordmark.
2. Email and LinkedIn. Search `TODO-CONTACT`.
3. Case 01 outcome numbers are invented. Search `DUMMY`.
4. About section numbers. Search `data-count`.
5. Images for cases 02 to 05. Drop files into `images/` named `02-problem.jpg`,
   `02-solution.jpg`, `02-outcome.jpg` and so on up to `05-outcome.jpg`.
   Around 1800x760, or anything near 21:9. Missing files show a labelled
   placeholder rather than breaking. Add `class="fit"` to a slide if it is a
   screenshot you do not want cropped.
6. Case 06 is redacted on purpose. Bar widths are inline styles.
7. Portrait crop lives in the `.portrait img` rule, `object-position`.

## How it behaves

- Cases collapse and expand. The first three are open by default.
- Each case has a three-image strip that pans with scroll, one image per stage.
- The Problem to Solution to Outcome rail draws as you scroll through a case.
- Light and dark follow the visitor's system setting.
- Everything respects `prefers-reduced-motion`.

## The one citation

The Growzen adherence figure is the published ECOS result, median 93.7% over the
first year, n=1190 across 24 countries. Source is linked in the outcome panel.
