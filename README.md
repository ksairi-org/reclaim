# Reclaim — validation landing page

A single-page, hard-paywall landing page used to test **willingness to pay** for
Reclaim (a focus / attention app with an AI attention coach) *before* building it.

Working name "Reclaim" is a placeholder.

## Live
Hosted on GitHub Pages → https://ksairi-org.github.io/reclaim

## What to configure before running traffic
See the comment block at the top of `index.html`:
1. **Email capture** — replace `YOUR_FORMSPREE_ID` with a form id from [Formspree](https://formspree.io).
2. **Analytics** — uncomment the Plausible snippet (or add GA4) to measure the funnel.
3. **Price** — tweak the price in the CTAs / pricing card to test price sensitivity.

## The metric that matters
`pay_intent` clicks (the pricing "Start free trial" button) ÷ visitors.
**>5–8% = strong willingness to pay.** Secondary: email signups ÷ visitors.
