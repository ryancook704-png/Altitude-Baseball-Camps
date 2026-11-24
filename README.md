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
- Real photos of the camps are the next addition. Planned spots: one wide photo under the For Coaches headline, small photos on the home cards. Use `<figure class="photo"><img src="images/your-photo.jpg" alt="..."></figure>` (classes `wide` and `tall` change the shape) and write real alt text.

## Pages
- `index.html` home, `our-camps.html` the three camps, `for-coaches.html` the Coach Partner offer, `contact.html` the inquiry form, `404.html` the not-found page (GitHub Pages serves it automatically).
- `for-coaches.html` carries its own styles in a `<style>` block scoped to `.fc`: a six-month "We handle / You handle" timeline, a plain-terms ledger, and the disclaimer. Its copy follows the locked contract (3 years, 33% of gross, no minimum payment, minimum camp hours and in-region exclusivity during the term, shortfall fee, renew at 25% or buy). Change the page and the contract together.
- `.sr` (in `style.css`) hides text visually but keeps it for screen readers; used for section headings that would look redundant and for the "We:" / "You:" labels in the timeline.
- Do not name a page-scoped CSS class `.camp`; `style.css` already uses it for the Our Camps list.

## Contact form
- `contact.html` posts to Formspree once `YOUR_FORM_ID` is replaced with a real form ID. Until then a small script opens the visitor's email app with the message filled in, so no inquiry is lost. Once the ID is set the script steps aside and the note under the button disappears on its own.

## To confirm
- The email and phone in the footer and on the contact page are Boulder Baseball Camps' details. Replace them with Altitude's own if different (search for `boulderbaseballcamps.com` and `435-901-9468`).
- The stats (3 locations, 2,000+ athletes, since 2017) and the camp claims on Our Camps (85 to 250+ campers, 70% return, sold out in one week) are copied from the old site or supplied by Cook. Confirm they are current before relying on them in coach outreach.
- The South Denver logo reads "EST. 2024" but the Our Camps copy says it launched in mid-summer 2026. One of them needs to change.
- Travel Camps were removed from the site for now. The old `/travel-camps` Squarespace URL lands on the 404 page; add a redirect to `/for-coaches` if you want one.
