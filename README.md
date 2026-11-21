# websites-stationsafari

The website for Station Safari, served at https://stationsafari.com by GitHub Pages.

## What is here

- `index.html`: landing page
- `gameplay/index.html`: how the app works, with screenshots and themes
- `terms/index.html`: the terms of service
- `privacy/index.html`: privacy policy, linked from the Google Play listing at https://stationsafari.com/privacy/
- `style.css`: shared styles (light and dark). Colours come from the logo: navy `#273654` (the app's `Colours.primary`), red `#731d17`, gold `#c08b54`
- `images/`: the logo (`logo.png`, `favicon.png`, `apple-touch-icon.png`), the four background themes (`theme-*.webp`) and app screenshots (`shot-*.webp`), all WebP at 420 to 480px wide
- `CNAME`: the custom domain for Pages
- `.nojekyll`: tells Pages to serve the files as they are

Plain static files with no build step. To preview locally, run `python3 -m http.server` in this folder and open http://localhost:8000.

## Publishing

- **GitHub Pages:** Settings, then Pages, then deploy from branch `main`, folder `/ (root)`. Custom domain `stationsafari.com`, with "Enforce HTTPS" ticked once the certificate is issued.
- **DNS (GoDaddy):** delete the default parked records first. Then add the four GitHub Pages `A` records for `@` (the current addresses are in [GitHub's custom domain docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)) and a `CNAME` for `www` pointing to `exileddevs.github.io`.
- **Domain verification:** verify the domain in the organisation's Pages settings (a TXT record) so no one else can claim it.
- Pages publishes whatever is on `main`, so check a change before pushing it.

## Rules to keep

- **Keep `/privacy/` where it is.** The Google Play listing links to it.
- **Update the policy when the app changes.** If the app starts collecting anything, adds an SDK or asks for a new permission, change the privacy policy and the Play Data safety answers together.
- **No tracking on the site.** No analytics, cookies, fonts from other sites or ads. The policy says the site has none.
- **No third-party logos.** Transport operators' logos and brands (including National Rail's) belong in the app where their terms allow, not here.
- **No en or em dashes.** Write a dash as a spaced hyphen ("Bank - Lewisham"), as in the app.

## Settings

Issues are off and pull requests can only be opened by collaborators. A ruleset on the default branch blocks deletion and force pushes. Contact: dave@exileddevs.com.

## Licence

All rights reserved. Copyright 2026 Exiled Developers.
