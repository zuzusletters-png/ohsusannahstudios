# Zuzu's Letters — project guide

Context for anyone (human or Claude) picking up this site. Read this before
editing `index.html`.

Public repository. Do not commit personal details, account identifiers,
credentials, or private document links here. Owner-specific context lives in
`CLAUDE.local.md`, which is deliberately not committed.

---

## What this is

- **Oh Susannah Studios** is the business. **Zuzu's Letters** is the product it
  sells. The domain belongs to the studio; the letters are the thing being sold.
- A letter arrives by post **once a month**. Not twice. An early draft said
  twice monthly and was wrong.
- Tagline: *"Pause to connect with the written word through letters delivered to
  your mailbox."*

### What arrives in each envelope

- The letter — her own stories, travels, reflections
- An original watercolour print made from one of her own photographs, on ARCHES
  100% cotton fine art paper, acid-free, archival, 5" x 7", ready to frame
- An inspirational quote on a card that doubles as a bookmark
- Two postcards — one to keep, one pre-stamped to pass on to a friend
- A few surprises
- A Spotify playlist QR code
- Access to a private Facebook group

---

## Accuracy rules — do not break these

These are corrections the owner has already made once. Getting them wrong
misrepresents her product.

| Rule | Why |
| --- | --- |
| **Never write "handwritten" or "written by hand."** | The letters are composed by hand but **computer-printed in a script font**. |
| **Prints are "made from" her photographs.** | Do **not** claim she paints each one by hand — that is unconfirmed. |
| **One letter per month.** | Not twice monthly. |
| Business is Oh Susannah Studios; product is Zuzu's Letters. | They are not interchangeable. |

---

## Design

Approved and liked by the owner. **Improve it; do not restart it.**

- **Single self-contained HTML file.** No frameworks, no build step, no external
  requests, no CDN links. Everything inline.
- **Palette:** oat paper `#EFEDE4`, ink navy `#2C3446`, pen blue `#3E5177`,
  moss `#6E7F63`, dusty plum `#8B6478`. A full dark-theme token set is defined.
- **Type:** Iowan Old Style / Palatino serif for reading; Optima / Candara
  humanist for small labels.
- **Body text is deliberately large.** The readership is mature women and
  comfortable reading was a stated priority. The owner confirmed the sizing is
  right. **Do not shrink it.**
- **Structure:** the page opens as a letter — her real salutation "Hello Dearest
  Friend," in her own words, signed. Then the enclosure list, the print section,
  About Zuzu, and the plans.

---

## Hosting and deployment

- Hosted free on **GitHub Pages**, repo `zuzusletters-png/ohsusannahstudios`,
  deployed from branch `main`, folder `/ (root)`.
- **`CNAME` must contain exactly `ohsusannahstudios.com`** — no trailing
  newline, no `https://`, no `www`.
- DNS is at Namecheap on **BasicDNS** nameservers (not the hosting nameservers).
  Apex has four A records — `185.199.108.153`, `.109.153`, `.110.153`,
  `.111.153` — and `www` is a CNAME to `zuzusletters-png.github.io.`

### Gotchas learned the hard way

1. **`index.html` must carry its own document skeleton.** If the page is drafted
   as a Claude Artifact, the Artifact runtime silently supplies
   `<!doctype>`/`<head>`/`<body>`. Served raw from Pages it needs its own —
   above all `<meta name="viewport" content="width=device-width, initial-scale=1">`,
   without which the site renders at desktop width on phones and the type is
   unreadable. This bit us once.
2. **Deploy via the GitHub web UI** (`/upload/main`). There is no `gh` CLI on the
   owner's machine, and `git push` stalls on a Windows credential dialog.
   Committing locally is still worth doing for history.
3. **The CDN lies for a few minutes.** After a commit, `raw.githubusercontent.com`
   and the live site keep serving the old file. Do not conclude the deploy
   failed. Verify against the API instead, which is never stale:
   `curl -s "https://api.github.com/repos/zuzusletters-png/ohsusannahstudios/contents/index.html?ref=main" | grep '"size"'`
   and compare with `wc -c index.html`.
4. **Changing nameservers can move email.** Before touching DNS on any domain,
   check for MX records first. See `CLAUDE.local.md`.

---

## Payments

The site is **static — there is no server, so there is nowhere for a secret key
to live.** Stripe **Payment Links** are therefore the correct approach, not a
custom checkout.

**Never put a Stripe secret key in this repository.**

Three live links are wired into `index.html`:

| Button | Product | Price |
| --- | --- | --- |
| Join the mail club | Month-to-Month | $18.99 / month, recurring |
| Give 6 months | 6-Month Bundle | $101.94 one-time ($16.99 a letter) |
| Give 12 months | 12-Month Bundle | $191.88 one-time ($15.99 a letter) |

All three collect the buyer's **name and shipping address** — these are physical
goods sent by post, and Stripe defaults to billing address only, which does not
give the owner somewhere to mail to. If you ever recreate a link, set
**"Billing and shipping addresses,"** not the default.

Shipping is currently restricted to **United States addresses only**. This was a
default chosen in the absence of an answer, on the grounds that a blocked
overseas order is recoverable and an unfulfillable one is not. Revisit it.

---

## Open items

- A photograph of a real print is the single highest-value missing asset. The
  page currently shows an empty placeholder box where it belongs, and another
  for a photo of the owner with her horses.
- Whether the studio ships outside the United States.
- The script font used on her original Google Site, which she wants carried
  over. Recommended for headings and the signature only, never body text.
- Merging the About Zuzu section with a letter she intends to supply.
