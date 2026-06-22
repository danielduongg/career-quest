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
├── index.html              # Landing / sales page (parents + students, pricing, FAQ)
├── app/
│   └── index.html          # The gamified web app (quest board, ROI calc, mentors) — self-contained
├── curriculum/
│   ├── index.html          # Browsable curriculum hub
│   ├── facilitator-guide.md
│   ├── module-01..08-*.md  # Eight self-paced modules
│   ├── mentor-outreach-scripts.md
│   └── worksheets/         # Career Scout Sheet, ROI Worksheet, Decision Matrix
├── data/
│   └── careers.json        # The career dataset (salaries, paths, mentors) with sources
└── README.md
```

## The app at a glance

- **8 career worlds** spanning tech, healthcare, engineering, business, design, and the skilled trades.
- **Quest board** in three tracks — 🔍 Recon, 🤝 Field Work, ⚖️ Reality Check — 9 quests per career.
- **ROI calculator** that turns cost, aid, and salary into debt, monthly payments, and payback time.
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

## Selling it

The landing page ships with three suggested tiers — **Explorer (free)**, **Family ($149 one-time)**, and **Classroom (custom)** — all editable in `index.html`. The free app is the funnel; the paid plans add the full guided curriculum, workbooks, more careers, and (for schools) a counselor dashboard and live mentor sessions. CareerQuest is a starter storefront, not a payment processor — wire up your own checkout (Stripe, Gumroad, etc.) on the call-to-action buttons.

## Data & honesty

Salary figures are **illustrative U.S. national medians** from the BLS Occupational Outlook Handbook (May 2024 reference year); every career links to its BLS source so users can verify current and local numbers. Cost, debt, and graduation figures come from the College Board, the Federal Reserve, and NCES. ROI math is intentionally simplified for teaching (10-year repayment, take-home ≈ 75% of salary). **CareerQuest is an educational tool, not financial, career, or admissions advice.**

## License

[MIT](LICENSE) — free to use, fork, and adapt. Built to help students choose well.
