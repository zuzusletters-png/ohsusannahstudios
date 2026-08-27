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
| `index.html` | The shop — one self-contained file, no build step |
| `blog.html` | The blog, *Notes between letters*. One page, newest post at the top. Self-contained, modelled on `details.html`, no custom fonts |
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
- **A bookmark for the month** — a detail lifted from the same photograph as the
  print, dated on the back. She prints these herself on cardstock; the giclée is
  the only piece from the art printer, at $4.80 each. **Never call the bookmark
  a giclée or mention ARCHES paper in the same breath** — that wording belongs
  to the 5x7 only.
- Two postcards — **the month's quote is printed on them**; one to keep, one
  pre-stamped to pass on to a friend. The quote moved here from a separate card
  on 19 August 2026, so it should not appear twice in one envelope.
- A few surprises — deliberately unnamed. Stickers and pressed flowers go here
  rather than in the list, so nothing becomes a promise she must keep monthly.
- A Spotify playlist QR code
- Access to a private Facebook group, **The Porch at Zuzu's Letters**, created
  26 August 2026. Private, subscribers only, and named on the page as *The Porch*.
  The page does not link to it and does not say how a new subscriber gets in, because
  that has not been settled with her. Do not invent a mechanism. Account details are
  in `CLAUDE.local.md`; the group's address does not belong in this public file.

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
| **In the sign-off, "Peace and Love" takes a capital L.** | Deliberate, not a typo. Do not correct it, and do not let a tidy-up pass change it. |
| **Only genuine prints may be shown or captioned as prints.** | As of 23 August 2026 the real ones photographed are **Bob &amp; Too Big** (the draft horses and yellow wagon), **The Garden Shed** (rust-red roof, flags), **House in Walland** (soft golden light), the **creek reflection** (autumn trees in water) and **Lovely Rita's eye**. The prints have titles and the owner gave these three herself — use them exactly. **Bob and Too Big are not her horses** — corrected by her on 23 August after a session assumed they were. Her own horses are **Hairy Harry** and **Lovely Rita**. Do not assume an animal in a photograph belongs to her. The Garden Shed and House in Walland came from her by email on 23 August, both on ARCHES stock. The mountain road, donkey, grazing horse and troll pictures are **test prints on photo paper** — usable as artwork, never captioned as the 5x7 on ARCHES stock. A caption claiming otherwise went live once and had to be corrected. |

---

## Design

Approved and liked by the owner. **Improve it; do not restart it.**

- **Single self-contained HTML file.** No frameworks, no build step, no external
  requests, no CDN links. Everything inline.
- **Palette:** oat paper `#EFEDE4`, ink navy `#2C3446`, pen blue `#3E5177`,
  moss `#6E7F63`, dusty plum `#8B6478`. **There is no dark theme, deliberately.**
  Every page used to carry a `prefers-color-scheme:dark` palette, so the site
  turned dark by itself on any phone set to switch appearance at sunset. The owner
  did not want that and it was removed on 24 August 2026, together with the unused
  `[data-theme="dark"]` block that nothing ever set. Each page now declares
  `<meta name="color-scheme" content="light only">`, which also stops Chrome on
  Android force-darkening the page. **Do not reintroduce a dark palette** unless
  she asks for one.
- **Type:** Iowan Old Style / Palatino serif for reading; Optima / Candara
  humanist for small labels.
- **Body text is deliberately large.** The readership is mature women and
  comfortable reading was a stated priority. The owner confirmed the sizing is
  right. **Do not shrink it.**
- **Structure:** the page opens as a letter — the standing salutation *"Hello
  Dear Friend,"* in her own words, signed. Then the enclosure list, a full
  **sample letter** anyone can read before buying, the print section, About
  Zuzu with her photograph, and the plans.
- **The first-person voice is deliberate.** The whole page is written as Zuzu
  speaking directly to the reader. Keep it. Never add explanations about who is
  writing or how the letters are made — the owner has ruled on this.

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
3. **Everything downstream of a push lags for a few minutes.** The live site,
   `raw.githubusercontent.com` **and the `contents` API** all keep serving the
   old file. Do not conclude the push failed — on 19 August 2026 the `contents`
   API still reported the previous file size several minutes after a push that
   had definitely landed. An earlier version of this note called that API
   authoritative; it is not.

   Check the ref and the object instead, both of which are exact:

   ```
   git ls-remote origin main            # remote branch tip
   git rev-parse HEAD:index.html        # local object id for the file
   ```

   If the remote tip equals your local `HEAD`, the push landed. To confirm a
   specific file, compare the object id above with the `sha` for that path in
   `https://api.github.com/repos/zuzusletters-png/ohsusannahstudios/git/trees/main`.
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

## State of play — 27 August 2026

**A new section, *The stories*, was added on 27 August 2026.** It sits between the
excerpt quote and the print band, as `<section class="band" id="stories">`, and its
job is to make the *content* of the letters interesting rather than to describe the
product again. The owner supplied the raw material as a list of things she has done,
and asked for something composed from it.

It is **four paragraphs of her own prose, deliberately not a bulleted list of
credits.** Her voice profile records that she never uses bullets in prose, and a
résumé would have sold her rather than the letters. The paragraphs group the material
into stages, horses, and backstage, and the fourth turns it toward the envelope: *"A
rainy walk home with my dog Otter is every bit as likely to turn up in your mailbox as
a Lipizzaner stallion."* That last paragraph is the one doing the selling; keep it if
the section is ever edited.

Voice rules were applied throughout: **no em dashes, `&hellip;` where a dash would go,
full forms rather than contractions, and her exclamation points left in.** The section
is `.stories`, 40rem, matching the excerpt above it. It is **not** in the masthead nav
— neither is the sample letter, and the nav already wraps to two rows on a phone.

**"The stage," never "a stage" (27 August 2026).** She corrected this twice and asked
that it be learned as a general rule rather than patched in one line: people who
perform say *the* stage. Back to the stage, time spent off the stage, a life on the
stage. "A stage" is right only for one physical platform among several. The same holds
for the rest of the vocabulary she uses from inside the business — *the wings*, *the
talent* — so **when she corrects a term from her own trade, apply it everywhere, not
only where she pointed.**

**Three judgement calls in that copy were put to her on 27 August 2026, and she
settled all three:**

- **Queen Guinevere and King Arthur&rsquo;s Tournament are two different things.** A
  first draft merged them, assuming Guinevere was a role in that show. It is not.
  They are now two separate sentences, and **the Guinevere line carries no venue**
  because she has not said where it was. Do not attach one.
- **The Little Mermaid line reads "at Walt Disney World when it was Disney-MGM
  Studios,"** which is her own wording, chosen after the anachronism was pointed out
  to her (the park was not called Hollywood Studios when the original show opened).
  Leave it as she wrote it.
- Her phrasing doubled back on itself: *"one of the largest ... that was once one of
  the largest programs in the country."* A draft cut it to a single claim and she
  approved that, then **put the past tense back herself** on 27 August: *"Years later
  I built, what was once, one of the largest equine assisted activities and therapies
  programs for veterans and first responders in the country."* **The "what was once"
  is deliberate and it is a matter of accuracy** — she has confirmed the program is no
  longer that large. Do not tidy it away as redundancy, and leave her commas around it;
  they are the rhythm of the sentence spoken aloud.

**The lede under the heading is hers, word for word (27 August 2026):** *"People ask
what I could possibly find to write about every month. Well, you see, that has never
been a problem&hellip;"* **It ends on the ellipsis, with nothing after it.** That is
not an unfinished sentence; it is the trailing beat her voice profile describes, and
it is doing the work the cut phrase used to do. Do not close it with a full stop or
finish the thought for her.

Two steers from how she got there, both useful when drafting for her. She reached for
the **plainer, more ordinary word** over the more writerly one, changing "my trouble"
to "a problem". And she **trimmed a phrase she had written herself** a few minutes
earlier ("I can talk about anything!"), so do not treat her own wording as fixed once
she has said it once. She edits herself hard, and usually by removing.

**She gave notes across roughly a dozen small edits before approving it**, and the copy
on the page is the result. **Every sentence in that section has now been through her
hands** &mdash; treat it the way *About Zuzu* is treated and do not tighten, shorten or
"improve" it.

**The blog was added on 25 August 2026.** `blog.html` — *Notes between letters* —
is a single page with the newest post at the top, reached from the masthead nav
("The Blog") and from the footer. It is modelled on `details.html`: the same
tokens and type, self-contained, and deliberately **without** the two base64
fonts that make `index.html` 166 KB. To add a post, copy the
`<article class="post">` block and paste it directly under the HTML comment that
says so; the newest post goes first. The first post is *Hard days do not have to
be harder*, her own writing.

**Her writing voice is now captured in a `my-writing-style` skill.** Built from
her own letters and personal essays. The findings that matter when drafting
anything in her voice: **she does not use em-dashes** — see the ellipsis rule
below for what does that work; she **rarely uses contractions** ("I am", "it is",
"do not"), which is what makes her prose sound like a letter; and her
**exclamation points are deliberate** and should not be trimmed. She has also
settled on **"Hello Dear Friend,"** as the standing salutation, replacing the
"Dearest Friend," of her earlier letters. Note this applies to *her* prose — the
site's own furniture copy, written for her, still uses `&mdash;` throughout.

**The ellipsis is her dash. Use `&hellip;`, never a hyphen and never an em dash
(26 August 2026).** She asked directly whether she uses `...` where a dash would go,
and her own writing bears her out: three ellipses do that job — `wins the
race&hellip;just like snail mail`, `turn on some music&hellip; Enjoy this moment`,
and `I will never do it&hellip;What is the saying` — against a single hyphen-as-dash,
`ready- ready to talk`, in the blog post. **She asked for that hyphen to be changed
and for `...` to be the rule from now on**, and it was, the same day. Note the
spacing habit: **no space before it**, and usually none after either. This applies to
her prose only; the em dashes in the site's furniture copy were left alone and are a
separate question she has not been asked. **The `my-writing-style` skill still
records the hyphen as the habit and does not know about this preference** — it could
not be re-saved from the session where she said it, so fold this in if a future
session has the tool.

**Name the product, do not talk around it (25 August 2026).** A draft social
caption read "these are the sorts of stories I am putting in the post now" and
she corrected it to "**these are the sorts of stories I am sending in Zuzu's
Letters.**" In captions and anywhere she is speaking about what she sends, use
the name. The coy phrasing was a writing tic, not her preference. This belongs
in the `my-writing-style` skill, but that skill could not be re-saved from the
session where the correction happened, so it is recorded here instead — fold it
in if a future session has the tool for it.



**Working.** The site is live at `https://ohsusannahstudios.com`; HTTPS is
issued and plain `http://` redirects to it. All four payment links are live. A
real purchase went through with the shipping address captured correctly, and was
refunded in full.

**The masthead nav stopped running off the side of a phone, 25 August 2026.**
`.masthead nav` was a flex row with no `flex-wrap`, so the five links could not
wrap and pushed about 5px past the right edge at 375px, letting the whole page
slide sideways. It now wraps (`flex-wrap:wrap;gap:.7rem 1.6rem`) and the links
carry `white-space:nowrap` so a label never breaks in the middle of its own
name. Checked at 320, 360, 375 and 414px: `scrollWidth` equals `clientWidth` at
all four, and the nav settles into two tidy rows (three at 320px). Predates the
wash work; it was only noticed while checking that.

**The painting now sits behind every page, on every screen, 25 August 2026.**
It used to be on the front page only, and only on screens wider than 64rem, so
phones never saw it at all. She asked for it everywhere. Two changes:

- `index.html` — the `@media (min-width:64rem)` gate around the wash was
  removed. The paper strengths that lie over it are unchanged (82% for ordinary
  sections, 64% for the sample letter and the plans, 97% behind the prints, 88%
  for the footer), so **the computer view looks exactly as she approved it**;
  what is new is that a phone now sees the same thing. The masthead and the
  opening letter are still uncovered, so the painting is at full strength there.
- `blog.html`, `details.html`, `404.html` — the wash was added to all three.
  These pages have no sections, just one centred `.wrap`, so the wrap itself
  now carries the paper at 88% (90% on `404.html`) with a soft shadow. It reads
  as a sheet of paper laid on the painting: on a computer the painting shows at
  full strength either side of the column, and on a phone the sheet fills the
  width and the painting tints it. `404.html` uses **`/images/wash.jpg`, an
  absolute path, on purpose** — that page is served for any address that does
  not exist, including deep ones like `/a/b/c`, where a relative path would look
  for the image in a folder that is not there.

Note while you are in that CSS: the `.band` rule inside the old media query was
dead. `.band{background:var(--paper-deep);}` sits later in the file at the same
specificity and has always won, so bands have always been solid. That is what
she has seen and approved, so it was left alone; the dead rule was dropped.

**The quote credit and the background wash, 24 August 2026.** The excerpt now
reads *From letter #1 · September 2026* — her wording, replacing a specific date
that would have gone stale.

On the wash: the fixed painting is always at full strength; what varies is how
much paper each section lays over it. She asked first for the closing block (the
O.S. Studios mark, Otter's photograph, the footer) to match the uncovered top of
the page, saw it live and **did not like it** — the small faint footer lines sat
on the fence and leaves. That was reverted the same day. What she wanted instead
was **more of the painting showing behind the plans**, so `#subscribe` dropped
from 82% paper to 64%, the same as the sample letter. It is safe there because
the plan cards and the timing panel carry their own solid backing; only the
ground behind them thins. **Do not strip the paper off the footer again.**

**About Zuzu was rewritten from the third paragraph on, 25 August 2026.** She
supplied the replacement wording herself and it is now three paragraphs where
there were two. The "It is loss that sent me..." paragraph gained the herd
lines and a purple heart emoji (written as `&#128156;`, chosen to match the dusty
plum in the palette; the file is otherwise
ASCII with named entities). A new paragraph after it tells the real origin
story — three years of the idea, fear and excuses, spinal fusion surgery two
months ago, and the decision to use the recovery time. The closing paragraph
now reads "connection, positivity, love and kindness." **This is her own text,
sent verbatim — do not tighten, shorten or "improve" it.** Only the punctuation
was normalised to match the rest of the file (curly apostrophes, an ellipsis, an
em dash for the hyphen after "ring true"). Supersedes the note below.

**A line came out of About Zuzu, 24 August 2026 (partly superseded).** "When
people ask if I miss performing, I can honestly say no." was removed at her
request. The love-and-kindness paragraph it left standing has since been
replaced by her own rewrite above.

**Search wording added, 24 August 2026.** She asked for **snail mail**, **letter
club** and **letter subscription service** to appear on the site for search. They
now sit in the page title, the description search engines show, and one line in
her own voice under *One envelope holding rather a lot*: "Some people call it
snail mail. Some call it a letter club, or a letter subscription service. I call
it writing to a friend." `details.html` carries the service phrase in its
description too. **This does not reopen the masthead line she removed** — the
objection there was defining the product against someone else's, not the words
themselves. Keep all three phrasings positive.

**Dark mode was removed everywhere on 24 August 2026.** The owner reported the
site turning dark at night on her phone but never on her computer — her phone
switches appearance at sunset and her computer is set to stay light. The cause was
the site's own dark palette, not the phone force-darkening it. All three pages now
show the light design to every visitor, always. See *Design* above.

**The desk photograph was replaced again on 24 August 2026.** The owner supplied
a cottage scene of her own choosing — table, teacup, daisies, stove — and asked
for it as-is. It supersedes everything described in the paragraph below. Note it
is a generated scene, not a photograph of her actual enclosures, so **do not
caption it as a photograph of what arrives**; the present caption, "A sneak peek of what
might arrive in your letter," is deliberately loose. Her genuine photographs of the
real enclosures are kept in the working folder named in `CLAUDE.local.md` and can
be swapped back in at any time.

**The desk photograph held the owner's real letter (23 August 2026, superseded).**
The picture at the top of *What arrives* was a generated scene whose letter and
print were invented; its fake letter had a warped fold, a blurred print and a
smear of leftover blur beside it, and each repair only went so far. She
photographed the real thing — her letter, the envelope, the quote card, the
postcard, the O.S. Studios sticker — on black cloth, and those items were cut
out and placed on the same cottage desk, lit and shadowed to match the room.
The Garden Shed print was warped into the photograph in place of the archway
print she had to hand, because the real Garden Shed is 8x12 and too big to sit
in the arrangement. **Nothing invented remains in that photograph except the
room itself.** Her originals and every intermediate step are in the working
folder named in `CLAUDE.local.md`.

**The print section shows three prints (23 August 2026).** The creek reflection
was taken off the page at the owner's request and replaced by two new
photographs of prints on ARCHES stock — The Garden Shed and House in Walland. Each print is now titled on the page.
All three on the page are now landscape, which settles the old mismatch between
a landscape and a portrait stacked together. The creek reflection image file is
still in `images/` but nothing references it.

**The playlist entry now explains the Spotify account (23 August 2026).** A
reader without an account tried the QR code and hit a login wall, so *A playlist*
in **And beyond the envelope** now says the free account is enough, that the
code leads to Spotify's sign-up page when you don't have one, and that scanning
again afterwards opens the playlist. The behaviour is as the owner's tester
reported it, not something verified here. The printed cards that carry the code
say the same thing; they are produced outside this repository.

The contact address in the footer, `hello@ohsusannahstudios.com`, is confirmed
to reach the owner — she tested it. Leave it as it is.

**Outstanding**

1. **The monthly subscription has never been tested end to end.** It is built
   differently from the three one-time links, and it bills again next month.
   This is the only untested part of the shop.
2. **The zuzusletters.com forwarding is unfinished** — she owns the name and it
   renews itself, but it still leads nowhere. Deferred by her on 19 August.

**Unanswered — ask at most one per turn, and only when it blocks the next step**

- The script font from her old Google Site, which she wants carried over.
  Recommended for headings and the signature only, never body text.
- Whether she paints the watercolours herself. Until she confirms, the prints
  are "made from" her photographs.
- Whether the studio ships outside the United States. Currently US-only.
- Merging the *About Zuzu* section with a letter she intends to supply.
- Whether the single letter should be promoted as a "try one first" option.

**"The last full time Queen Guinevere," corrected 27 August 2026.** The first version
read *"the last Queen Guinevere&hellip;the very last one."* She came back and said there
is a chance she was the last **full time** one but not the very last ever, and asked for
the qualifier so the line is certainly true. **"The very last one" is gone and must not
come back.** She weighed "one of the last" as a safer alternative and rejected it: the
hook depends on the word *last*, and "full time" turns out to strengthen the line rather
than hedge it, because a payroll word next to *Queen Guinevere* is both funnier and more
convincing than the bare claim. **This is the second time in one day she has chosen the
true sentence over the tidier one** — see the "true is better" note in `CLAUDE.local.md`.
