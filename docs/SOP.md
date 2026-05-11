# Item Onboarding Standard Operating Procedure
**Process:** Partner Readiness Score — Seller Item Submission Review  
**Owner:** Item Onboarding Analyst  
**Last Updated:** January 2024  

---

## 1. Purpose

This document outlines the process for reviewing, scoring, and actioning seller item submissions on the marketplace platform. The goal is to ensure every item that goes live meets the platform's content standards for completeness, accuracy, timeliness, and relevancy.

---

## 2. Submission Requirements Checklist

Before scoring, confirm the seller has submitted all required fields:

| Field | Requirement | Required? |
|---|---|---|
| Product Name | Clear, descriptive title | Yes |
| Category | Nested path (e.g. Electronics\|Mobiles\|Smartphones) | Yes |
| Product Description | Minimum 100 characters | Yes |
| Image URL | Valid, working image link | Yes |
| Price | Actual and discounted price | Yes |
| Rating | Product rating out of 5 | Yes |

If any required field is missing, the submission is automatically flagged for revision before scoring begins.

---

## 3. Scoring Process

Each submission is scored across 4 dimensions using the Partner Readiness Score (PRS) framework.

**Step 1** — Open the partner_readiness_score.xlsx scoring tracker.

**Step 2** — Enter the seller's submission data into the data sheet.

**Step 3** — The following scores calculate automatically:

- **Completeness Score** — checks if all 4 key fields are filled (25 points each)
- **Accuracy Score** — checks image URL presence (50 pts) and description length >100 chars (50 pts)
- **Timeliness Score** — 100 points if submitted within 7-day SLA; -10 points per day late
- **Relevancy Score** — category path detail (70 pts) + rating ≥ 4 (30 pts)

**Step 4** — The composite PRS calculates automatically:
```
PRS = (Completeness × 0.30) + (Accuracy × 0.25) + (Timeliness × 0.25) + (Relevancy × 0.20)
```

---

## 4. Action Thresholds

Based on the PRS, the system recommends one of three actions:

| PRS Score | Action | Next Step |
|---|---|---|
| 80 and above | Approve | Item moves to listing review queue |
| 60 – 79 | Request Revision | Send seller the feedback template with specific issues |
| Below 60 | Escalate | Flag to Sr. Item Data Process Analyst within 24 hours |

---

## 5. Escalation Path

If a seller scores below 60:
1. Flag the submission in the tracker with status "Escalate"
2. Document the top 3 issues causing the low score
3. Notify the Sr. Item Data Process Analyst via email within 24 hours
4. Do not send the standard feedback template — the Sr. Analyst will handle communication
5. Log the escalation date and follow up if no response within 48 hours

---

## 6. SLA Timelines

| Milestone | Deadline |
|---|---|
| Seller submits items | Day 0 |
| Analyst completes scoring | Within 2 business days |
| Revision request sent to seller | Within 3 business days |
| Seller resubmits revised items | Within 7 days of feedback |
| Final approval or escalation | Within 10 business days of original submission |

---

## 7. Common Failure Reasons by Category

Based on analysis of 100 submissions:

- **Musical Instruments** — most common issues: missing image URLs, descriptions too short
- **Computers & Accessories** — most common issue: vague category paths
- **Home & Kitchen** — most common issue: late submissions past SLA

Use this to proactively brief sellers in these categories before their submission deadline.

---

## 8. Revision and Resubmission

When a seller is asked to revise:
1. Send the seller feedback template (see `seller_feedback_template.md`)
2. Clearly state the 1–2 specific fields that need fixing
3. Give a firm resubmission deadline (7 days from feedback date)
4. Re-score the resubmission using the same framework
5. If the resubmission still scores below 60, escalate immediately

---

*This SOP is a living document and should be updated whenever scoring thresholds, SLA timelines, or submission requirements change.*

