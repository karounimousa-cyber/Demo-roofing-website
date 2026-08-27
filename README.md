# Wright Brothers Roofing — Redesign Concept

Single-page site. No build step, no dependencies. Drop `index.html` into a repo and
deploy on Vercel with the **Other** preset.

## Before this goes live

Search the file for `class="ph"` — every one of those `◆` markers is a placeholder
that needs a real answer from the owner.

| Item | Where | Needs |
|---|---|---|
| Phone number | nav, hero card, footer | Real number — currently `(713) 000-0000` |
| Business hours | hero card, footer | Confirm |
| Years in business | — | Add a stat if they want one |
| Licensed / insured / bonded | trust strip | **Confirm before publishing.** Do not claim this unverified. |
| "Free" anything | — | REMOVED. Was invented, not stated by the business. Re-add only if the owner confirms. |
| Same-day callback | quote section | Invented — confirm or cut |
| Emergency tarping / after-hours | hero card, storm band | Invented — confirm or cut |
| Photos sent to you, claim docs, written estimate | quote checklist | Invented — confirm or cut |
| Three-step process | process section | Proposed workflow, not theirs — confirm |
| Review quotes | reviews section | Replace the three `SAMPLE` cards with real Google reviews |
| Job photos | "Recent work" | Six real photos, 4:3, ideally 1600px wide |

**Only these are verified** from published sources and safe as-is: business name,
address (5803 Gulf Fwy, Houston, TX 77023), the service list, the roof-type list,
and the 4.9 / 120-review aggregate.

**Everything else is proposed copy** — wording written for this mockup to show what
the page could say. It is not what the business claims. Treat the whole body text as
a draft for the owner to approve, edit, or reject line by line.

## Remove the concept banner

Delete the block between `<!-- ===== CONCEPT NOTICE` and `<!-- ===== /CONCEPT NOTICE ===== -->`
plus the `.concept` CSS rules. Also remove every `<span class="ph">◆</span>` once the
real content is in.

## Wire up the form

The form currently shows a preview message on submit. Options, cheapest first:

- **Formspree / Basin** — change `<form>` to `action="https://formspree.io/f/XXXX" method="POST"`
  and delete the submit handler in the script block. Free tier covers a small roofer.
- **Vercel serverless function** — `/api/quote.js` posting to email or a CRM.

Make sure submissions also fire a text message. Roofing leads go cold in hours.

## Re-skinning

Colour and type variables sit at the top of the `<style>` block in `:root`.
`--copper` is the accent; `--slate` is the dark ground.
