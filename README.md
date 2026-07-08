# Reclaim — validation landing page

A single-page, hard-paywall landing page used to test **willingness to pay** for
Reclaim (a focus / attention app with an AI attention coach) *before* building it.

Working name "Reclaim" is a placeholder.

## Live
GitHub Pages (Actions workflow) → https://reclaim.sytes.net · https://anicca-labs.github.io/reclaim

## Tracking (built in — no config needed)
The full funnel is captured to **Supabase** (`reflect-stg` → `public.reclaim_events`),
inserted client-side with the publishable key (RLS allows INSERT only, so the page
can write but not read — data is readable only via the service role):
- `page_view` — on load (the denominator)
- `pay_intent` — clicking the pricing "Start free trial" button (the key signal)
- `lead` — email submit (waitlist), stored with the email

Optional: A/B the price in the CTAs / pricing card to test price sensitivity.

## The metric that matters
`pay_intent` events ÷ `page_view` events. **>5–8% = strong willingness to pay.**
Secondary: `lead` (emails) ÷ `page_view`.
