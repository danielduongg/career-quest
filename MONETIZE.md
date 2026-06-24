# Turn CareerQuest into a business 💸

Everything is already built. This guide gets you taking payments in about **15 minutes** — no coding, no backend, no monthly hosting bill.

## The funnel (already wired up for you)

1. **Free** — the app + a free *"Don't Waste 4 Years"* checklist + an email sign-up. This builds your audience.
2. **Family — $49 one-time** — the printable bundle people buy: workbook, roadmaps booklet, certificate, parent guide.
3. **Classroom — custom** — schools email you.

## What you'll need

- A free **[Gumroad](https://gumroad.com)** account *(recommended)* — it hosts the checkout, **delivers your files automatically**, and handles sales tax. (Stripe alternative is below.)
- The 3 paid PDFs delivered to you: **CareerQuest-Complete-Workbook.pdf**, **CareerQuest-Career-Roadmaps.pdf**, **CareerQuest-Certificate.pdf**.
- ~15 minutes.

---

## Step 1 — Create your product on Gumroad

1. Sign up at gumroad.com → **New product** → **Digital product**.
2. Name it *"CareerQuest — The Complete Family Bundle"*. Set the price to **$49**.
3. **Upload the 3 paid PDFs** (you can add the free checklist as a bonus too).
4. In the product settings, set the **"after purchase" / redirect URL** to your thank-you page:
   `https://danielduongg.github.io/career-quest/success.html`
5. Publish, then **copy the product's share URL** (it looks like `https://yourname.gumroad.com/l/careerquest`).

## Step 2 — Paste your link into the site (the only edit you need)

1. Open `index.html` on GitHub: go to the file → click the **pencil (Edit)** icon.
2. Scroll to the bottom and find the **CAREERQUEST STORE CONFIG** block:

   ```js
   window.CAREERQUEST_CONFIG = {
     familyCheckoutUrl: "",            // ← paste your Gumroad link here
     familyPrice:       "$49",         // ← change the displayed price if you want
     classroomContact:  "mailto:hello@example.com?subject=...",  // ← your email
     emailFormEndpoint: ""             // ← (optional) your Formspree link
   };
   ```

3. Paste your Gumroad URL between the quotes for **`familyCheckoutUrl`**, and set **`classroomContact`** to your real email address.
4. Click **Commit changes**.

That's it. Your **"Get instant access"** button is now a live checkout, and GitHub Pages redeploys in about a minute. **You're selling.** 🎉

> Until you paste a link, the buy button gently sends visitors to your free email list instead — so the page is never "broken," it just isn't charging yet.

---

## Step 3 (optional, 5 min) — Collect emails

The free checklist already downloads directly, but you can also build a mailing list:

1. Create a free form at **[formspree.io](https://formspree.io)** and copy its endpoint (`https://formspree.io/f/xxxxxxx`).
2. Paste it into **`emailFormEndpoint`** in the same config block. Commit.

Now the email box on the page collects subscribers, and you can email them the checklist plus future offers.

## Changing the price

The price that's actually **charged** is set in Gumroad. Update **`familyPrice`** in the config so the page display matches.

## Prefer Stripe?

1. In Stripe, create a **Payment Link** for a $49 product and set its **after-payment redirect** to your `success.html`.
2. Paste that payment-link URL into **`familyCheckoutUrl`**.

Note: Stripe doesn't auto-deliver files. Either email the PDFs after purchase, or stick with Gumroad — it's simpler for digital products.

---

## ⚠️ Keep the paid files private

The 3 paid PDFs are **deliberately not in your public GitHub repo** (anyone could grab them for free). The repo's `.gitignore` already blocks them. Sell them only through your store. The **free checklist** is the one PDF meant to be public — it's the hook.

## Pricing ideas

- Launch at **$49**. Later, test **$39** for volume or **$79** as a premium anchor.
- Add a **Classroom** upsell for schools (handled by email — low effort, high value).
- Offer a higher tier that bundles a live 30-minute planning session.

A good gut check before raising the price: does the buyer walk away with a clear, defensible **Plan A / B / C**? If yes, it's worth more than a single hour with a college counselor.
