# slb-supplies

Website for **SLB Supplies Ltd** ([slb-supplies.co.uk](https://slb-supplies.co.uk)): animal feed and supplies, Wiggs Farm, Ellistown, Coalville.
It is plain HTML with one stylesheet and no JavaScript, hosted on Netlify.

```
site/          the website: Netlify publishes this folder (set in netlify.toml)
  index.html   home page; every other page is <page>/index.html
  styles.css   all styling
  images/      photos (WebP, no location or camera metadata)
  fonts/       Righteous + Josefin Sans (SIL Open Font Licence)
  _redirects   old GoDaddy page addresses -> new ones
```

## Editing

Edit the HTML or CSS in `site/`, then commit and push to `main`. Netlify redeploys automatically.
To preview locally, run `python3 -m http.server 8000 --directory site` and open http://localhost:8000.
Opening the files directly won't work, because links start at the site root (`/styles.css`).

## Netlify setup (one-off)

1. **Add new site → Import an existing project** → this repo. There's no build command; the publish folder comes from `netlify.toml`.
2. **Contact form:** Site configuration → Forms → *Enable form detection*, then trigger a redeploy. Add the email that should receive enquiries under *Form notifications*.
3. **Domain:** add `slb-supplies.co.uk`, then set these records in the Fasthosts DNS:
   - `@`: an A record pointing to `75.2.60.5`
   - `www`: a CNAME pointing to `<site-name>.netlify.app`

   HTTPS is issued automatically once the records resolve.

## Notes

- `info@slbsuppliesltd.co.uk` (shown on the site) is a GoDaddy mailbox on the old domain. Keep the old domain's email running, or change the address in the HTML.
- The contact form uses Netlify Forms, with a honeypot field for spam.

## Photo credits

The shop's own photos and graphics belong to SLB Supplies Ltd. The old site's Getty and GoDaddy stock photos were licensed for GoDaddy's site builder only, so they were replaced with photos from Pexels. The [Pexels licence](https://www.pexels.com/license/) allows free commercial use with no attribution required:

| Used for | Photo |
|---|---|
| Home page banner and link previews | [Two horses at a stable shed](https://www.pexels.com/photo/two-brown-horses-in-the-stable-7883179/) |
| Livestock: alpaca | [Two alpacas on grass](https://www.pexels.com/photo/alpacas-standing-on-a-grass-field-11093544/) |
| Livestock: cattle | [Cow and calf](https://www.pexels.com/photo/cow-and-calf-1838564/) |
| Livestock: general feed | [Cows on the pasture](https://www.pexels.com/photo/view-of-cows-on-the-pasture-26382432/) |
| Livestock: goat | [Two goats](https://www.pexels.com/photo/close-up-photograph-of-two-goats-7057492/) |
| Livestock: lamb/sheep | [Lamb beside a sheep](https://www.pexels.com/photo/white-lamb-beside-black-sheep-10636271/) |
| Livestock: pig | [Piglets](https://www.pexels.com/photo/close-up-shot-of-piglets-on-the-mud-4751423/) |
| Livestock: poultry | [Brown hen](https://www.pexels.com/photo/close-up-photo-of-brown-hen-101830/) |
| Livestock: rabbit | [Rabbit in grass](https://www.pexels.com/photo/a-rabbit-on-the-grass-13014564/) |
| Pet food: cats | [Black cat](https://www.pexels.com/photo/black-cat-28119304/) |
| Pet food: small pets | [Hamster](https://www.pexels.com/photo/close-up-photo-of-cute-hamster-4520484/) |
