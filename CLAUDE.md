# Zuzu's Letters — project guide

**Start here, and read the whole file before editing anything.** This is the
durable record for the project. Almost everything in it was either learned the
hard way or corrected by the owner once already, so it is cheaper to read than
to rediscover.

## The five things that matter most

1. **The owner is Susannah — she goes by "Zuzu."** She is not a developer and
   has said plainly that she will not do technical steps. Do the technical work
   yourself wherever a tool allows it; when something genuinely needs her, say
   so honestly and give numbered steps that describe what she will see on
   screen, never what a thing is called.
2. **Ask her one question at a time.** She asked for this directly. A list of
   questions stalls her; a single question gets answered well.
3. **This repository is public.** Never commit personal details, account
   identifiers, credentials, customer data, or private document links.
4. **Three product facts are not negotiable:** the letters are never
   "handwritten," the prints are "made from" her photographs, and a letter
   arrives once a month. The full set is in *Accuracy rules* below.
5. **The site is live and taking real money.** `index.html` is the shop. A
   careless commit closes it.

## If you are running in the cloud

A cloud session can see this repository and nothing else. It **cannot**:

- read the working copy on the owner’s own computer, where
  `CLAUDE.local.md` sits beside these files holding account details and open
  questions;
- reach her Stripe, Namecheap, GitHub or Google accounts, or drive her browser;
- see the private working folder kept outside this repo — mailing list,
  production schedule.

So a cloud session can edit files, write copy, fix markup and prepare changes.
Anything that touches her accounts has to wait for a session on her own machine,
or be handed to her as on-screen steps. Say which of the two it is rather than
implying the work is done.

## Where things live

| Path | What it is |
| --- | --- |
| `index.html` | The entire website — one self-contained file, no build step |
| `images/` | Photographs used by the page |
| `CNAME` | The custom domain, exactly `ohsusannahstudios.com` |
| `CLAUDE.md` | This file: the durable, public-safe project record |
| `CLAUDE.local.md` | Owner context, accounts, open questions — gitignored, local only, never pushed |
| `HANDOFF-PROMPT.md` | Superseded and gitignored. Historical only; its product wording contradicts this file |
| A private folder outside the repo | Internal documents — mailing list, production schedule. Named in `CLAUDE.local.md`. Never belongs here |

**Keep this file true.** When something here turns out to be wrong or goes
stale, correct it in the same commit as the work. The *State of play* section at
the bottom goes stale fastest.

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
- An original **giclée print** made from one of her own photographs, 5" x 7",
  ready to frame, on **ARCHES® Aquarelle Rag Paper**, 0.61 mm thick, acid-free
  and pH-neutral. Call it a giclée
  print, never a "watercolour" — the owner asked for this explicitly. For the
  paper itself, use the required wording in the accuracy table below. The two
  are consistent: Aquarelle Rag is the product name; the required sentence
  describes how it is made.
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
| **Describe the paper in exactly these words:** *"printed on 100% cotton fiber paper produced from the ARCHES® traditional molds that create beautiful texture."* | The owner supplied this phrasing verbatim and asked for it exactly. Treat it as required brand wording — do not paraphrase, shorten, or "improve" it. Keep the ® symbol. Earlier copy said "ARCHES 100% cotton fine art paper," which was wrong. |
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
2. **`git push` works** now that the owner has signed in to GitHub through the
   Windows credential dialog — it no longer stalls. There is still no `gh` CLI
   on her machine. The GitHub web UI (`/upload/main`) remains a fallback.
   Note that commits made through the web UI create a history unrelated to any
   local one; if both have been used, `git rebase` will try to replay every
   commit and conflict. Reset to `origin/main` and reapply the file instead.
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

Four live links are wired into `index.html`, in two cards:

| Card | Button | Product | Price |
| --- | --- | --- | --- |
| One at a time | Keep them coming | Month-to-Month | $18.99 / month, recurring |
| One at a time | Try a single letter | Zuzu's Letter | $18.99 one-time |
| All at once | Six months | 6-Month Bundle | $97.99 one-time ($16.33 a letter) |
| All at once | Twelve months | 12-Month Bundle | $179.99 one-time ($15.00 a letter) |

The cards split on **whether it renews**, not on who it is for. An earlier
version split "for yourself" versus "a gift" and that was wrong — any of the
four works as a gift, and the old labels turned gift-buyers away. A line under
both cards now says so explicitly.

**Stripe prices cannot be edited.** To change an amount you create a new price,
build a new payment link on it, and deactivate the old link. The bundles were
repriced this way on 18 August 2026; the superseded $101.94 and $191.88 links
are deactivated, not deleted.

### Statement descriptors — the gotcha that bit us

All four read **`Zuzus Letters`** on card statements. No apostrophe: Stripe
rejects `< > \ ' " *` and caps descriptors at 22 characters.

Setting `statement_descriptor` on the **Product** only works for
**subscriptions and invoices**. One-time payments ignore it completely — a live
test purchase came through reading `O.S. STUDIOS`, the account default, despite
the product being set correctly. For one-time payments the value must go on the
**payment link** as `payment_intent_data.statement_descriptor`.

So: the monthly is covered by the product setting; the single letter and both
bundles are covered on their payment links. If you ever rebuild a one-time link,
set it again — it does not inherit.

Do **not** fix this by changing the account-level descriptor. The account also
sells mugs and totes, and those buyers should not see "Zuzus Letters."

All four collect the buyer's **name and shipping address** — these are physical
goods sent by post, and Stripe defaults to billing address only, which does not
give the owner somewhere to mail to. If you ever recreate a link, set
**"Billing and shipping addresses,"** not the default.

Shipping is currently restricted to **United States addresses only**. This was a
default chosen in the absence of an answer, on the grounds that a blocked
overseas order is recoverable and an unfulfillable one is not. Revisit it.

---

## State of play — 19 August 2026

**Working.** The site is live at `https://ohsusannahstudios.com`; HTTPS is
issued and plain `http://` redirects to it. All four payment links are live. A
real purchase went through with the shipping address captured correctly, and was
refunded in full.

**Outstanding**

1. **The monthly subscription has never been tested end to end.** It is built
   differently from the three one-time links, and it bills again next month.
2. **The Namecheap shared hosting is still being paid for** and is no longer
   needed now that HTTPS is confirmed. Settle the domain-email question in
   `CLAUDE.local.md` first — her mail was historically tied to that hosting.
3. **A photograph of the owner with her horses** is still an empty placeholder
   box in the *About Zuzu* section. The print photograph is done.

**Unanswered — ask at most one per turn, and only when it blocks the next step**

- The script font from her old Google Site, which she wants carried over.
  Recommended for headings and the signature only, never body text.
- Whether she paints the watercolours herself. Until she confirms, the prints
  are "made from" her photographs.
- Whether the studio ships outside the United States. Currently US-only.
- Merging the *About Zuzu* section with a letter she intends to supply.
- Whether the single letter should be promoted as a "try one first" option.
