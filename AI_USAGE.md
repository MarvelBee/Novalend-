# AI Usage Documentation

**Tools used:** 
*   **Claude (Sonnet):** Used conversationally for extracting and re-verifying the funnel/default-rate math from the brief, and drafting the initial root-cause analysis.
*   **Google Gemini & Python:** Used to refine the PRD technical scope, pivot the Go/No-Go strategy, generate the horizontal funnel visualization, and format the final Word deliverables.

## Representative Prompts

**1. Diagnosing the Funnel (Claude):**
> *"Read the attached FirstBank NovaLend brief. Before writing anything, tell me where the real problem sits in the funnel and default-rate data, onboarding friction vs. underwriting/credit risk vs. something else, and justify it with the numbers, not narrative."*
→ **Result:** The AI successfully diagnosed that the 66.1% offer-decline rate plus the 14%-vs-6% default gap point to underwriting/pricing calibration as the primary driver.

**2. Refining the PRD & Go/No-Go (Gemini):** 
> *"Act as a product owner. We have a 66.1% drop-off at the offer stage and a 14% default rate. Draft a PRD for a new offer screen that fixes this... Let's proceed to the one-page Go/No-Go Recommendation."*
→ **Result:** The AI drafted a comprehensive PRD and Go/No-Go strategy, but missed several critical business constraints and UX logic flows that required immediate human correction (detailed below).

## Where the AI missed a real constraint or misread the data, and how it was caught

**1. The PRD's feature originally missed a core structural bottleneck.**
Section 2 of the PRD identified three candidate causes of the 66.1% offer-decline rate: an unattractive flat price, a flat loan amount, and a fixed repayment schedule. The first draft of the feature built tiered pricing and tiered loan amounts, but left the repayment term fixed. 
*The Fix:* I caught this omission and forced the AI to include a "Tenor Toggle" component so that all three candidate bottlenecks are addressed by the final feature.

**2. Missing the Regulatory Transparency Constraint (Hidden Fees).**
In an early draft, the AI suggested hiding the loan fees behind a "See full details" toggle to keep the UI clean. I flagged this as a severe regulatory risk, as financial regulators strictly penalize hidden fees. 
*The Fix:* I directed the AI to rewrite the PRD to mandate 100% upfront fee transparency on a single screen by default.

**3. Misaligning the Solution with the Data (The Friction Trap).**
To solve the 14% default rate, the AI initially recommended forcing users to add a card or bank account directly on the offer screen via direct debit tokenization. I caught a critical product flaw here: forcing upfront payment tokenization introduces heavy front-end friction that would actively worsen our primary 66.1% abandonment crisis. 
*The Fix:* I corrected the logic, completely removed front-end payment friction from the 6-week MVP scope, and decoupled the solutions. I directed the AI to rely on a **Strict Backend Risk Cutoff** to handle defaults, leaving the front-end entirely focused on **Bounded Flexibility (Dynamic Sliders & Tenor Toggles)** to win back safe users, backed by a **Decline-Reason Feedback UI** to capture exit data.
