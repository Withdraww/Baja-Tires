# Baja Tires & Detailing — site

Plain static site. No build step, no dependencies, no framework.

## Deploying to Vercel

`index.html` MUST sit at the top level of the repo. If it is nested inside a
folder, Vercel serves nothing at `/` and you get 404: NOT_FOUND.

Vercel → Project → Settings → Build and Deployment:

  Framework Preset ....... Other
  Build Command .......... (empty / override OFF)
  Output Directory ....... (empty)
  Install Command ........ (empty / override OFF)
  Root Directory ......... ./

Then Deployments → latest → Redeploy.

## Updating photos

Replace the file in images/ keeping the same filename. Sizes are already
correct; nothing else to change.

  hero-lotus.jpg ........ hero background
  wheel-rack.jpg ........ tires column
  detail-before.jpg ..... detailing, left
  detail-after.jpg ...... detailing, right
  shopfront-truck.jpg ... wide band above Visit
  challenger.jpg ........ square beside the services list

## Updating hours

Two places, both in index.html: the `<table class="hours">` in the Visit
section, and the hours lines in the footer.

## Notes

- Google reviews are hardcoded, not live. They will go stale.
- Map is an OpenStreetMap embed, no API key needed.
- Fonts are self-hosted Poppins and Geist Mono, both SIL Open Font License.
