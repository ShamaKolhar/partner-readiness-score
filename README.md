# Partner Readiness Score

I built this project to understand what it actually takes to onboard a seller onto a retail marketplace, not just the concept, but the operational detail behind it.

The question I started with: if you're an analyst managing hundreds of seller item submissions, how do you decide which ones are good enough to go live, which need fixes, and which need to be escalated? This is my attempt to build that decision-making process from scratch.

---

## What I built

A scoring system that takes seller item submissions and evaluates them across 4 dimensions — completeness, accuracy, timeliness, and relevancy. Each submission gets a score out of 100. Based on that score, the system recommends one of three actions: approve, request revision, or escalate.

I used a real product dataset (Amazon Sales Dataset from Kaggle) as the base, added simulated seller submission metadata on top of it, and built everything in Excel. The results are visualized in a Tableau dashboard.

---

## How the scoring works

I broke item quality into 4 dimensions because a seller submission can fail in different ways — a product can have a great description but no image, or be submitted on time but filed under the wrong category. Treating them separately makes it easier to give specific feedback.

**Completeness (30%)** — checks if the 4 non-negotiable fields are filled: product name, category, description, and image URL. Each field is worth 25 points.

**Accuracy (25%)** — checks quality, not just presence. Is the image URL actually there? Is the description longer than 100 characters or just a placeholder?

**Timeliness (25%)** — did the seller submit within the 7-day SLA? Every day past the deadline drops the score by 10 points.

**Relevancy (20%)** — is the category path detailed enough to be useful? Is the product rating strong enough to meet platform standards?

The final score is a weighted average:
```
PRS = (Completeness × 0.30) + (Accuracy × 0.25) + (Timeliness × 0.25) + (Relevancy × 0.20)
```

---

## Action thresholds

| Score | Action |
|---|---|
| 80+ | Approve |
| 60–79 | Request Revision |
| Below 60 | Escalate to Sr. Analyst |

---

## What the data showed

Out of 100 seller submissions:
- 57 were approved
- 34 needed revision
- 9 were escalated

The Musical Instruments category had the weakest average score (42.5) — mostly due to missing images and short descriptions. Electronics performed best. If this were a real onboarding process, Musical Instruments sellers would need a targeted briefing before their next submission cycle.

---

## Files in this repo

```
├── data/partner_readiness_score.xlsx   — dataset + scoring engine
├── dashboard/PRS_Dashboard.pdf         — Tableau dashboard
├── docs/SOP.md                         — onboarding process documentation
└── docs/seller_feedback_template.md    — communication template for revision requests
```

---

## Tools
Excel, Tableau, Kaggle (Amazon Sales Dataset)

---

*Built by Shama Kolhar as a self-initiated project to understand marketplace item onboarding operations.*
