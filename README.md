# Altitude Baseball site

Static site for altitudebaseballcamps.com, hosted free on GitHub Pages. Plain HTML and CSS, no build step.

## Publishing (when you're ready)
1. Create a GitHub repo, push this folder, then Settings > Pages > Deploy from branch `main` / root.
2. DNS at your registrar: `www` CNAME -> `<your-github-username>.github.io`; apex `@` A records -> 185.199.108.153, .109.153, .110.153, .111.153. Turn on "Enforce HTTPS" in Pages once it verifies. Leave any MX and TXT records (email) alone.
3. Contact form: make a free form at formspree.io and replace `YOUR_FORM_ID` in `contact.html`.
4. Cancel Squarespace only after the new site is live. If the domain is registered through Squarespace, transfer it out first.

## Brand (Brand Kit 2.0)
- Colors are CSS variables at the top of `assets/style.css`: Summit Navy #14263D, Infield Clay #B94A22, Chalk #F7F2E9, Granite #5D6877, Fog #E2DCCF, Ink #1B2430, Ember #E88A62 (accent on navy only).
- Type: Oswald (headlines and labels, uppercase) and Inter (body), self-hosted in `assets/fonts/` under the SIL Open Font License (license files included). The site makes no Google Fonts requests.
- Logos, favicons, and the share image are in `images/brand/`. The full logo set (one-color versions, app icons, SVG sources) is in the separate brand kit.
- `images/brand/og-image.png` (1200 x 630) is the link-preview image. After you change it, Facebook, LinkedIn, and similar services can take a while to refresh their cached preview.

## Photos
- The site currently has no photographs. The old AI-generated photos were removed on purpose; heroes and cards use the brand's rays and ridge-line graphics (`assets/ridge.svg`).
- When real photos are ready, use `<figure class="photo"><img src="images/your-photo.jpg" alt="..."></figure>` (classes `wide` and `tall` change the shape). See the Photo shot list for what to shoot.

## Notes
- Canonical tags and `sitemap.xml` use `/our-camps`, `/for-coaches`, and `/contact`, matching the old Squarespace URLs. GitHub Pages serves `our-camps.html` at `/our-camps`.
- `robots.txt` and `sitemap.xml` are included.

## To confirm
- The email and phone in the footer and on the contact page are Boulder Baseball Camps' details. Replace them with Altitude's own if different (search for `boulderbaseballcamps.com` and `435-901-9468`).
- The earnings estimator shows total camper revenue. The original showed take-home and per-hour; add that formula in `for-coaches.html`.
- The stats (3 locations, 2,000+ athletes, since 2017) are copied from the old site. Confirm they're current.

- Travel Camps were removed from the site for now (page removed, nav and contact option dropped). The old `/travel-camps` Squarespace URL will 404; add a redirect to `/for-coaches` if you want one.
