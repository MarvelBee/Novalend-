# NovaLend Product Owner Decision Kit

**Candidate:** Marvelous Bolaji
**Role:** Product Owner / Product Manager (NovaLend)

Submission for the FirstBank Digital Factory NovaLend Product Owner take-home task. Scenario: incoming Product Owner for NovaLend with a 6-week hard CBN reporting deadline and a 30-day beta showing a 14% default rate against a 6% target[cite: 16].

**Start here if you only read one thing:** `NovaLend-Go-No-Go-Final.docx`, the executive recommendation, followed by `NovaLend-Data-Driven-Final.docx` for the reasoning it's built on[cite: 16].

## Deliverables Index

| # | File | What it is |
|---|---|---|
| 1 | `NovaLend-Go-No-Go-Final.docx` | **Go/no-go recommendation:** The executive call to launch with severe restrictions (Strict Risk Cutoff + Card Tokenization). Explicitly addresses the 14% vs. 6% default gap. <br><br>|
| 2 | `NovaLend-Data-Driven-Final.docx` | **Data-driven decision:** Mathematically proves the bottleneck is an underwriting/adverse selection crisis, not just onboarding friction. <br><br>* A **Funnel Visualization Chart** highlighting the 66.1% drop-off. <br>*A/B testing* A **"Painted Door" Experiment Design** to validate user demand for flexible loans before committing engineering time. |
| 3 | `NovaLend-PRD-Final-V2.docx` | **PRD:** Full PRD for the NovaLend Offer Screen. Details a dynamic, risk-tiered offer with specific account tokenization to secure repayments. Includes 6 user stories and clear acceptance criteria. |
| 4 | `NovaLend-Prioritized-Backlog-V2.docx` | **Prioritized backlog:** 10 candidate features scored using the RICE framework. Features requiring >4 weeks of effort were strictly excluded to protect the 6-week CBN deadline. |
| 5 | `NovaLend-Stakeholder(team)docx` | **Stakeholder/Team Communication:** Three distinct communications tailored for the Executive Sponsor, Compliance & Risk, and Engineering. Each addresses the exact same trade-off but with highly calibrated emphasis and detail. |
| 6 | `AI_USAGE.md` | **AI usage requirement:** Tools and prompts used, and specific cases where the AI's first-pass output missed a real constraint or misread the data, and how each was caught. |

## Key Assumptions Made

- **Pre-screened Population:** "Invited" is treated as a plausibly pre-screened population for the purposes of the root-cause analysis[cite: 16].
- **Continuous Risk Scoring:** The existing alternative-credit score is assumed to be a continuous/ordinal value that can be cut into risk tiers without a model retrain[cite: 16].
- **Recovery vs. Friction:** I assumed that forcing users to pre-fund the native NovaWallet would spike abandonment. Therefore, the product relies on direct debit card tokenization to balance guaranteed recovery with user trust. 
- **The Deadline:** "6 weeks" is treated as the deadline for a launch-ready, Risk-approved framework, not for a full 100% reopening of the user base[cite: 16].
