# Get Yo Plate — Ordering Demo

A preview of the text + web ordering system built for **Get Yo Plate**, a Southern food catering business in Spokane, WA. This replaces the current Instagram DM + Venmo/CashApp workflow with a structured order form, automated text updates, and a live dashboard for the owner.

This repo hosts the **customer-facing demo**, live for testers to try before the real backend goes live.

**[Live site →](https://ben-blair-net.github.io/getyoplate)**

---

## What's here

| File | Purpose |
|---|---|
| `index.html` | Landing page — FAQ for testers. Explains what the demo is, how to place a test order, dietary alerts, and the feedback survey. Links to the demo. |
| `customer-demo.html` | The interactive demo itself — order form → receipt → simulated text thread → feedback survey. |

Both are self-contained, single-file HTML — no build step, no dependencies beyond Google Fonts.

---

## The demo flow

1. **Order form** — pick plates, add notes, submit
2. **Receipt** — confirms the order, prompts to check texts
3. **Simulated SMS thread** — payment instructions, reply "PAID," a short wait, then confirmation and an opt-in for next week's drop list
4. **Feedback survey** — three quick questions at the end; submitting opens a pre-filled Google Form in a new tab

No real orders are placed and no real payment is taken — everything after "Place order" is simulated so testers can react to the real flow without touching money.

---

## Running locally

```bash
git clone https://github.com/ben-blair-net/getyoplate.git
cd getyoplate
# open index.html directly, or serve it:
npx serve .
```

---

## Customizing the current drop

Edit the `DROP` config object near the top of the `<script>` in `customer-demo.html`:

```js
var DROP = {
  item: "Smothered Pork Chops",
  desc: "...",
  price: 20,
  dietary: "Contains pork & dairy. Gravy is flour-based — not gluten-free.",
  deadlineLabel: "Sat, Jul 25",
  dropDayLabel: "Sunday, Jul 26",
  sold: 38, cap: 50
};
```

Update this weekly to match the real drop — item, price, dietary info, dates, and how many plates have sold.

---

## Feedback

Feedback from the survey at the end of the demo goes to [this Google Form](https://docs.google.com/forms/d/e/1FAIpQLSfqObmn3HwkUQMR-ExwOC60Dfxg6qxJwK5eGutXjxL4-fxQlw/viewform), pre-filled with the tester's in-app answers. Responses land in the linked [Google Sheet / form dashboard](https://docs.google.com/forms/d/1TsWGvXkkKoOYhuFvqDzUJjzZHSNND5TBnkXCp0rMgRo/edit) for Avant to review.

---

## What's next

This demo is the front end for a larger system currently in progress:

- Flask + Postgres (Supabase) + Twilio backend for real order handling and SMS
- Owner dashboard for order management, payment confirmation, and revenue tracking
- Deployment to Render, with a GitHub Actions heartbeat to keep the free-tier database awake between weekly drops
- Stripe integration planned for real payment processing

---

## Tech stack

- Vanilla HTML/CSS/JS — no framework, no build step
- Google Fonts (Anton, Inter)
- Hosted on GitHub Pages

---

## License

MIT — free to use, fork, and modify.
