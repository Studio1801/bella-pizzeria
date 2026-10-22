# Bella Pizzeria site (Studio 1801 mockup)

Static site. No build step. In Replit, use the HTML/CSS/JS template, upload everything in this folder, and run.

## Files
- `index.html` : the whole site. CSS at the top, menu data and cart logic in the script at the bottom.
- `404.html`, `terms.html`, `privacy.html` : supporting pages (terms and privacy are placeholders).
- `dashboard.html` : the owner dashboard. Orders shows Right now (waiting orders with a live countdown and one check button) and This week (seven day cards with orders, sales and a busy bar; tap one to zoom into that day's list). New order types in phone orders. Money and Menu sit in the top bar, which matches the website header. Sample data only, not connected.
- `favicon.svg`
- `images/` : Bella's dish photos plus a storefront crop from Google Maps (low resolution).

## What this build fixes from the Slice site
1. **Brand and identity.** No Slice branding. Hand-lettered red hero, doodles that say "Brazilian style!", a live circled "Open now", and a note pointing new customers to the chicken with catupiry.
2. **Finding food fast.** One ordering section: search box (matches English words too, so "sausage" finds calabresa and "steak" finds picanha), four starter dishes (a swipe row on phones), then sticky category tabs.
3. **A menu people understand.** Pronunciation and a plain-English line on every Brazilian dish, plus a glossary.
4. **Ordering that fixes real gaps.** Flavor picker for 6 esfihas (the old flow never asked), one-tap reorder for returning customers, ready time as a clock time, Guarana and sweet pizza add-on in the cart, call-in link at checkout. The cart and checkout never leave Bella's page.
5. **Small moments that make people stay.** Tap the speaker next to any Brazilian word to hear it said in Portuguese (uses the phone's built-in voice). "Can't decide? Let the pizza pick" spins the doodle and jumps to a random Brazilian pizza. The Order button bounces when something is added. A sticky note on the map says "We're right here!"

## Before showing the owner (search the code for `SWAP:`)
- Photos: hero and the four starter dishes use Bella's own photos in `images/`. Most other menu thumbnails still load from Slice's image server; replace them as you collect better shots.
- About text: placeholder, rewrite with the owner's real story.
- Weekly hours, delivery fee (`SETTINGS.deliveryFee`), tax rate (`SETTINGS.taxRate`, 7% = MA 6.25% + 0.75% local).
- Items without photos simply show no thumbnail. Add `img` to any item in `MENU` once you have a photo.
- `SETTINGS.onlineDiscount` (10%): matches the "10% off online orders" Slice runs today. Confirm Bella wants to keep it.
- `SETTINGS.promoCodes`: empty. Add codes like `{"PIZZANIGHT": 0.15}` for their special offers.
- `SETTINGS.tips`: driver tip choices on delivery orders.
- Sweet pizza fruit choices (Strawberry, Banana) are a guess. Slice only says "optional fruit".
- "Pay when I pick up": Slice lists card payments only. Confirm Bella takes cash before launch.

## Parity with the Slice site (checked Oct 2026)
Everything on bellapizzeriama.com is here: all 91 dishes and prices, hours, address, phone, pickup 20 to 30 and delivery 20 to 35 minutes, 10% off online, curbside pickup, schedule-ahead ordering, Visa/Mastercard/Amex, fries or yuca on the plates, optional fruit on sweet pizzas, get directions, terms, privacy, do not sell my data and accessibility. Slice's app download links are left out on purpose.

## Next steps in Replit
- Real payments: mount Square or Stripe card fields where the `SWAP` comment sits in the checkout form.
- Send orders somewhere: right now "Place order" only shows a confirmation. Hook it to the owner's POS, a webhook, or SMS.
- Host a `404.html` route (Replit and Vercel both pick it up automatically for static sites).
