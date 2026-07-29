# Jack Lake Fitness

Static site for Jack Lake Fitness — personal training in Grays, Essex. Plain HTML/CSS/JS, no build step, deployed via GitHub Pages.

## Preview locally

Open `index.html` directly in a browser, or serve it:

```
python3 -m http.server 8000
```

then visit `http://localhost:8000`.

## Push to GitHub

Not yet done — create a repo (e.g. `jacklakefitness`) and push this directory.

## Enable GitHub Pages

Under repo → **Settings → Pages**, set source to the default branch / root.

## Connect jlfitness.o-sullivan.uk

The repo already includes a `CNAME` file containing `jlfitness.o-sullivan.uk`.

At the o-sullivan.uk registrar's DNS settings, add:

- One **CNAME** record: host `jlfitness`, pointing to `reeceosullivan.github.io`

Once that resolves, tick **Enforce HTTPS** in **Settings → Pages** (can take a few hours after DNS propagates).

If Jack later buys jacklakefitness.com and wants to point it here instead, swap the contents of the `CNAME` file to `jacklakefitness.com` (or `www.jacklakefitness.com`) and update the DNS record at his registrar instead.

## Things to customise before showing Jack

- **Email** — set to `info@jacklakefitness.com`; swap if he'd rather use something else.
- **Facebook** — no icon on the site yet since he doesn't have a page. Once he sets one up, duplicate the Instagram/TikTok anchor block in the Contact section's `.social-links` div and point it at the new page.
- **About section** — replace the bio placeholder and photo placeholder with Jack's real bio and photo.
- **Gallery** — replace the six placeholder boxes with real training photos in `images/`.
- **Testimonials** — currently says "coming soon"; add real client quotes once he has some (with their consent).
- **Prices** — currently all "TBC"; fill in once he decides.
- **FAQ answers** — a few are pre-filled (qualifications, insurance, online coaching); the rest (cancellation policy, session length, equipment) need his actual answers.
- **Contact form** — wired to Formspree but needs a real endpoint: sign up free at [formspree.io](https://formspree.io), create a form, and replace `YOUR_FORM_ID` in the form's `action` attribute in `index.html`.
- **TikTok feed embed** — there's a "Latest on TikTok" section with a placeholder div for this. Jack needs to create a free widget at [snapwidget.com](https://snapwidget.com) or [elfsight.com](https://elfsight.com), connecting his own `@jacklakefitness` TikTok account (this step has to be done by him — it needs his login). Once he sends you the generated embed code, paste it in place of the placeholder div in the `#tiktok` section of `index.html`.
- **Google Business Profile** — separate from this site but worth setting up (free) for local search/maps visibility.
- Favicon — none set yet; could crop the existing logo into one.
