# SSC CGL Prep Portal

A complete, offline SSC CGL preparation web app — **no API key, no backend, no internet needed after first load**. Just open `index.html` and start studying.

## How to run

```bash
# Just open the file — that's it
open index.html          # macOS
start index.html         # Windows
xdg-open index.html      # Linux
```

No `npm install`. No build step. No API key. Safe to push to a public GitHub repo.

---

## How to add more questions

All questions live in **`questions.js`**. Just follow the pattern:

```js
const QUESTION_BANK = {
  qa: [   // Quantitative Aptitude
    {
      source: "R.S. Aggarwal Ch.10",
      year: "SSC CGL 2023",
      topic: "Percentage",
      difficulty: "easy",          // easy | medium | hard
      question: "What is 15% of 480?",
      options: ["A) 62", "B) 72", "C) 82", "D) 92"],
      correct: 1,                  // 0-indexed (B = index 1)
      explanation: "15% of 480 = (15/100)×480 = 72",
      trick: "10% = 48, 5% = 24. Add = 72."
    },
    // ... more questions
  ],
  ri: [ /* Reasoning */ ],
  en: [ /* English   */ ],
  ga: [ /* GK        */ ]
};
```

**Section keys:** `qa` = Quant, `ri` = Reasoning, `en` = English, `ga` = GK

---

## Source books used

| Section | Source |
|---|---|
| Quantitative Aptitude | R.S. Aggarwal — Quantitative Aptitude · Rakesh Yadav — 7300+ Maths |
| Reasoning | M.K. Pandey — Analytical Reasoning |
| English | SP Bakshi — Objective General English · SSC CGL PYQ |
| General Awareness | Lucent's General Knowledge · Testbook / Adda247 Current Affairs |
| Mock Tests | Testbook · Adda247 · Career Power PYQ series |

---

## Features

- **Study mode** — solution + Rakesh Yadav / M.K. Pandey shortcut trick after each answer
- **Exam mode** — countdown timer (72 sec/question) + live −0.5 negative marking
- **Full Tier 1 mock** — 100 Qs, 4 sections, 15 min sectional time locks (2026 pattern)
- **Source tags** — every question shows book name and chapter
- **XP system** — earn XP per correct answer, level up from Beginner → Master
- **Bookmarks** — save tricky questions, review later with tricks
- **Analytics** — section-wise accuracy bars, score trend, day streak
- **Tools tab** — Vocab builder (SP Bakshi), Formula sheet (R.S. Aggarwal), Speed tricks (Rakesh Yadav), Current affairs (Testbook/Adda247)
- **Topic filter** — drill into a specific topic (e.g. only Percentage within Quant)
- **Dark mode** — automatic via `prefers-color-scheme`
- **Mobile responsive** — works on phones too

---

## Push to GitHub

```bash
git init
git add .
git commit -m "SSC CGL prep portal — offline, no API key"
git branch -M main
git remote add origin https://github.com/sourav1206/ssc-cgl-portal.git
git push -u origin main
```

Enable **GitHub Pages** (Settings → Pages → main → root) to host it free at:
`https://sourav1206.github.io/ssc-cgl-portal`

---

## Exam pattern reference (SSC CGL 2026)

| Tier | Duration | Questions | Marks | Negative marking |
|---|---|---|---|---|
| Tier 1 | 60 min | 100 (25 × 4 sections) | 200 | −0.5 per wrong |
| Tier 2 | Sectional | Multiple papers | 400+ | −1 per wrong |

**Tier 1 exam:** Aug–Sep 2026 · **Tier 2 exam:** Dec 2026

---

Good luck with SSC CGL 2026!
