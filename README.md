<div align="center">

# 🧭 CareerQuest

### Try the major *before* you spend four years and $100k on it.

A gamified course that helps high schoolers — and their parents — test-drive real careers,
meet the people who live in that world, and run the honest cost-vs-salary math
**before** committing to a path.

[**▶ Play the app**](app/) · [**📘 Curriculum**](curriculum/) · [**🏠 Landing page**](index.html)

</div>

---

## Why this exists

The decision of what to study after high school is one of the largest financial commitments a person ever makes — yet most people make it on a guess.

- About **one-third of bachelor's students change their major** at least once. ([NCES](https://nces.ed.gov/pubs2018/2018434/index.asp))
- Only about **64% finish a bachelor's within six years**. ([NCES](https://nces.ed.gov/fastfacts/display.asp?id=40))
- Private-college tuition averages **~$45,000/year**, and Americans owe **$1.84 trillion** in student debt. ([College Board](https://research.collegeboard.org/trends/college-pricing/highlights), [Federal Reserve](https://www.federalreserve.gov/releases/g19/current/))

CareerQuest's goal: **don't waste four years.** Choose a path on purpose — degree, trade, or apprenticeship — backed by real experience and real numbers.

## Is there already a platform that does this?

Pieces of it exist — CareerQuest stitches them into one guided, gamified journey and adds the money math:

| Need | Best existing tools | What CareerQuest adds |
|---|---|---|
| Test-drive the actual work | [Forage](https://www.theforage.com/) (free company job simulations) | Routes students to the right simulation per career, as a quest |
| Talk to real professionals | [CareerVillage](https://www.careervillage.org/), [LinkedIn](https://www.linkedin.com/), [VirtualJobShadow](https://www.virtualjobshadow.com/) | Built-in directory **plus** copy-paste outreach scripts |
| Cost & salary reality | [BLS OOH](https://www.bls.gov/ooh/), [Georgetown CEW](https://cew.georgetown.edu/), College Scorecard | An interactive **ROI calculator** that ties cost to debt to salary |
| Keep teens engaged | (mostly worksheets) | A **quest board** with XP, levels, and badges |

The app's mentor directory links out to those real platforms, so CareerQuest complements them rather than replacing them.

## What's in this repo

```
career-quest/
├── index.html              # Landing / sales page — pricing, value stack, checkout, email capture
├── success.html            # Post-purchase thank-you page (your checkout redirects here)
├── MONETIZE.md             # Step-by-step: turn on payments + an email list in minutes
├── CareerQuest-Free-Checklist.pdf   # Free lead magnet (the only PDF in this public repo)
├── app/
│   └── index.html          # The gamified web app (quest board, ROI calc, roadmaps, mentors)
├── curriculum/
│   ├── index.html          # Browsable curriculum hub
│   ├── facilitator-guide.md
│   ├── module-01..08-*.md  # Eight self-paced modules
│   ├── mentor-outreach-scripts.md
│   └── worksheets/         # Career Scout Sheet, ROI Worksheet, Decision Matrix
├── data/
│   └── careers.json        # Career dataset (salaries, paths, mentors, roadmaps) with sources
└── README.md
#
# The PAID product (Complete Workbook, Roadmaps booklet, Certificate PDFs) is delivered
# to you separately and is deliberately NOT in this public repo — those are what you sell.
```

## The app at a glance

- **32 career worlds** with built-in search and category filters, spanning tech, healthcare, engineering, business, design, public service, and the skilled trades.
- **Quest board** in three tracks — 🔍 Recon, 🤝 Field Work, ⚖️ Reality Check — 9 quests per career.
- **ROI calculator** that turns cost, aid, and salary into debt, monthly payments, and payback time.
- **Step-by-step roadmap** for every career — five clear stages from high school to landing the job.
- **Simulated mentors** (day-in-the-life) **plus** a directory to meet *real* professionals.
- **XP, levels, and 6 badges**; progress saves locally in the browser.
- **Zero dependencies, zero build step, zero tracking.** One HTML file.

## Run it locally

It's static — just open the files, or serve the folder:

```bash
# Python
python3 -m http.server 8000
# then visit http://localhost:8000

# or Node
npx serve .
```

## Deploy free on GitHub Pages

1. Push this repo to GitHub (see below).
2. Repo **Settings → Pages → Build and deployment → Source: Deploy from a branch**.
3. Choose branch `main` and folder `/ (root)`, then **Save**.
4. Your site goes live at `https://<your-username>.github.io/career-quest/` within a minute or two.

The landing page is the root `index.html`; the app lives at `/app/`; the curriculum at `/curriculum/`.

## Make money with it

This is a complete, ready-to-sell funnel — no backend required:

- **Free** — the gamified app, a downloadable [decision checklist](CareerQuest-Free-Checklist.pdf) (lead magnet), and an email-capture form.
- **Family — $49 one-time** — the printable bundle people buy: the 22-page Complete Workbook, the 32-Career Roadmaps booklet, a completion certificate, and the parent guide (delivered as PDFs).
- **Classroom — custom** — a contact link for schools and districts.

Going live takes about 15 minutes: create a product on **Gumroad** (or a Stripe Payment Link), upload the paid PDFs, and paste your link into the one **config block at the bottom of `index.html`**. The buy button, price, classroom contact, and email list are all wired to that block. Full instructions — plus the post-purchase thank-you page (`success.html`) — are in **[MONETIZE.md](MONETIZE.md)**.

> The paid PDFs are intentionally kept out of this public repo so they aren't free. Your store hosts and delivers them; only the free checklist is public.

## Data & honesty

Salary figures are **illustrative U.S. national medians** from the BLS Occupational Outlook Handbook (May 2024 reference year); every career links to its BLS source so users can verify current and local numbers. Cost, debt, and graduation figures come from the College Board, the Federal Reserve, and NCES. ROI math is intentionally simplified for teaching (10-year repayment, take-home ≈ 75% of salary). **CareerQuest is an educational tool, not financial, career, or admissions advice.**

## License

[MIT](LICENSE) — free to use, fork, and adapt. Built to help students choose well.
