# CMO Swings

Website for CMO Swings: apparel, in-person hitting lessons, and online swing reviews.

## Go live

1. **Upload:** put `index.html` and the image files in the root of a GitHub repo (for example `cmoswings`).
2. **Turn on GitHub Pages:** repo Settings → Pages → Source: "Deploy from a branch" → branch `main`, folder `/ (root)` → Save.
3. **Order emails:** orders are emailed to `ORDER_EMAIL` through FormSubmit. The first order sends an "Activate" email from FormSubmit; click it once. To use Formspree instead, paste your form ID into `FORMSPREE_ID`.
4. **Domain:** in GitHub Settings → Pages → Custom domain, enter `cmoswings.com`. Then in GoDaddy → DNS for cmoswings.com add:
   - four `A` records for `@` pointing to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - a `CNAME` record for `www` pointing to `<your-github-username>.github.io`
   Then tick "Enforce HTTPS" in GitHub Pages once it becomes available.

## Edit later

Near the top of the script in `index.html`:
- `PRODUCTS`: apparel names, prices, sizes, photos
- `TYPES`: lesson types and prices
- `HOURS`: weekly lesson hours (0 = Sunday)
- `SHIP` / `FREE_SHIP`: shipping cost and free-shipping threshold
- `CAL_USERNAME`: your Cal.com username; in-person lessons book on your Cal.com calendar
- `VENMO`: Venmo username; checkout and the lesson "Pay on Venmo" buttons send payments here
- `ORDER_EMAIL` / `FORMSPREE_ID`: where order emails go (FormSubmit by default; set a Formspree ID to use that instead)
- The "Questions" section (FAQ) is plain HTML near the bottom of the page
