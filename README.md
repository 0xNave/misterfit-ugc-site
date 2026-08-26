# Misterfit UGC Accelerator — funnel site

Static two-page funnel for the $2,000 UGC Accelerator, built on the qualification
playbook researched from the biggest info sellers (short application before the
calendar, transparent pricing, action-based guarantee, waitlist routing for
not-ready leads).

## Pages

- `index.html` — landing page: guarantee-led hero, VSL slot, mechanism,
  12-week curriculum, who-it's-for / who-it's-not, dark guarantee band,
  transparent pricing ($2,000 or 3 × $700), FAQ, earnings disclaimer.
- `apply.html` — 7-question multi-step application:
  1. Contact (name, email, phone, optional handle)
  2. Current content stage
  3. Prior course/coaching investment
  4. Hours per week available
  5. #1 obstacle (open text — call ammo)
  6. Investment readiness at the real price (**branch point**: "Not right now" → waitlist)
  7. Show-up commitment ("No" → waitlist)

  Qualified applicants land on a booking screen (Calendly embed, prefilled
  name/email). Everyone else lands on a friendly waitlist screen with an
  optional low-ticket downsell button.

## Before launch — fill in `config.js`

| Key | What it does |
|---|---|
| `CALENDLY_URL` | Booking link shown to qualified applicants. Empty → "we'll reach out within 24h" message. |
| `FORM_ENDPOINT` | Optional JSON endpoint (Formspree/Basin/webhook) that receives every application, including waitlisted ones. Empty → no capture. |
| `DOWNSELL_URL` | Where "not right now" leads can go (low-ticket product / community). Empty → message only. |

Also:

- Replace the VSL placeholder in `index.html` with your video embed.
- Add a testimonials section **only when you have real student results**
  (see the HTML comment in `index.html`) — never fabricated ones.

## Deploy

Hosted on GitHub Pages from the `main` branch root. Any push to `main`
redeploys. To run locally, just open `index.html` in a browser.
