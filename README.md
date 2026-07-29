# Jack Lake Fitness

Static site for Jack Lake Fitness — personal training in Grays, Essex. Plain HTML/CSS/JS, no build step, deployed via GitHub Pages.

## Preview locally

Open `index.html` directly in a browser, or serve it:

```
python3 -m http.server 8000
```

then visit `http://localhost:8000`.

## Push to GitHub

Done — [github.com/reeceosullivan/jacklakefitness](https://github.com/reeceosullivan/jacklakefitness) (public, required for free GitHub Pages on a private-repo-restricted plan).

## Enable GitHub Pages

Done — serving from `master` / root, custom domain registered via the API.

## Connect jlfitness.o-sullivan.uk

The repo includes a `CNAME` file containing `jlfitness.o-sullivan.uk`, and GitHub Pages already has this registered as the custom domain for this repo.

At the o-sullivan.uk registrar's DNS settings, add:

- One **CNAME** record: host `jlfitness`, pointing to `reeceosullivan.github.io`

Once that resolves, tick **Enforce HTTPS** in **Settings → Pages** (can take a few hours after DNS propagates).

If Jack later buys jacklakefitness.com and wants to point it here instead, swap the contents of the `CNAME` file to `jacklakefitness.com` (or `www.jacklakefitness.com`), re-register the custom domain via the Pages API/settings, and update the DNS record at his registrar instead.

## Things to get from Jack

- **Real bio** — About section currently has generic filler copy ("Jack is a qualified personal trainer based in Grays, Essex, focused on...") — replace with his own words, story, and specialties.
- **Real training photos** — the 3-tile Gallery grid is still placeholders.
- **Prices** — currently all "TBC" on the Services cards.
- **Testimonials** — section says "coming soon"; add real client quotes once he has some (with their consent) — don't fabricate these, fake reviews are a genuine legal/trust issue for a real business.
- **A few FAQ answers** — equipment, session length, and cancellation policy currently redirect to "get in touch" rather than guessing at his actual policies.
- **Facebook** — no icon yet since he doesn't have a page. Once he sets one up, duplicate the Instagram/TikTok anchor block in the Contact section's `.social-links` div.

## Small setup tasks (on you, not Jack)

- **Contact form** — wired to Formspree but needs a real endpoint: sign up free at [formspree.io](https://formspree.io), create a form, and replace `YOUR_FORM_ID` in the form's `action` attribute in `index.html`.
- **TikTok feed embed** — "Latest on TikTok" section has a placeholder div. Jack needs to create a free widget at [snapwidget.com](https://snapwidget.com) or [elfsight.com](https://elfsight.com), connecting his own `@jacklakefitness` account (has to be him, needs his login). Once he sends the generated embed code, paste it in place of the placeholder div in the `#tiktok` section of `index.html`.
- **Google Business Profile** — separate from this site but worth setting up (free) for local search/maps visibility.
