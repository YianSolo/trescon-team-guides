# Trescon LinkedIn Employment Guide — web version

A single-page HTML version of the Trescon team guide for re-linking LinkedIn profiles to our reinstated company page.

## Files

```
.
├── index.html               Self-contained guide (HTML + inline CSS)
├── fonts/
│   ├── OptimaLTPro-Roman.otf  Display / headline typeface
│   └── Montserrat-Regular.ttf Body / UI typeface
├── images/
│   ├── trescon_logo.svg     Master brand mark (cover, nav, footer)
│   ├── trescon_logo.png     PNG fallback (also used inside mockup SVGs)
│   ├── *_me_menu.svg        Animated mockups — gentle pulse on the
│   ├── *_experience_*.svg     dashed callout rings draws the eye to
│   ├── *_company_*.svg        each click target. Animations are SMIL,
│   ├── *_profile_*.svg        embedded in the SVG, and play automatically
│   └── *_pencil.svg           when the page is opened in a browser.
└── README.md
```

No build step — `index.html` references images via relative paths and uses only inline CSS. Open it locally in any browser to preview.

## Brand styling

The page implements the **Trescon Modern** visual design system v1.0:

- Fraunces (display) + Inter (body) loaded from Google Fonts
- Sage-green palette on `--paper` (#FAFAF6) backgrounds — never pure white
- Inset rounded dark hero (`--ink` #161718 with green radial-gradient mesh)
- One italicised phrase per display headline in `--green-dark`
- Eyebrow + green hairline opening every section
- Three-dot accent dividers between sections instead of `<hr>`
- Soft shadows and rounded corners on all cards (`--r-lg` / `--r-xl`)

Master design system lives at `Trescon Marketing/Trescon-Visual-Design-System.md`. If you re-skin or extend this page, follow that document.

## Deploying via GitHub Pages

1. Create a new public repo (suggested name: `trescon-team-guides`).
2. Push the contents of this folder to the repo's default branch.
3. In the repo's **Settings → Pages**:
   - Source: **Deploy from a branch**
   - Branch: `main` / root
4. After ~30 seconds, the guide is live at:

   ```
   https://<github-username>.github.io/trescon-team-guides/
   ```

5. (Optional) Add a custom domain like `guides.trescon.com.au` under **Settings → Pages → Custom domain**, then add a `CNAME` DNS record pointing at `<github-username>.github.io`.

## Updating the guide

1. Edit `index.html` (or replace mockups in `/images`).
2. Commit and push — GitHub Pages redeploys automatically within a minute.

## Notes

- The page is fully responsive and works on phones, tablets and desktop browsers.
- The mockup images are stylised illustrations, not real LinkedIn screenshots.
- The Trescon T-mark is the master SVG (`/images/trescon_logo.svg`). A 512×512 PNG fallback (`trescon_logo.png`) is also embedded inside each mockup SVG via base64 for the LinkedIn company-logo slot.
