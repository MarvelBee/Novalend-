# AI Usage Documentation

**Tools used:** 
*   **Claude (Sonnet):** Used conversationally for extracting and re-verifying the funnel/default-rate math from the brief, and drafting the initial root-cause analysis[cite: 15].
*   **Google Gemini & Python:** Used to refine the PRD technical scope, pivot the Go/No-Go strategy, generate the horizontal funnel visualization, and output the final `.docx` artifacts.

## Representative Prompts

**1. Diagnosing the Funnel (Claude):**
> *"Read the attached FirstBank NovaLend brief. Before writing anything, tell me where the real problem sits in the funnel and default-rate data, onboarding friction vs. underwriting/credit risk vs. something else, and justify it with the numbers, not narrative."*[cite: 15]
→ **Result:** The AI successfully diagnosed that the 66.1% offer-decline rate plus the 14%-vs-6% default gap point to underwriting/pricing calibration as the primary driver[cite: 15].

**2. Identifying the Repayment Bottleneck (Claude):**
> *"I have an issue with the bottlenecks being stated and the on-screen tiered-pricing feature, which I believe does not fully tend to the bottlenecks mentioned, especially the aspect of repayment."*[cite: 15]
→ **Result:** The PRD's first pass named three candidate bottlenecks (price, amount, and repayment tenor) but the AI generated a feature that only structurally addressed two (price and amount)[cite: 15].

**3. Refining the PRD & Go/No-Go (Gemini):** 
> *"Act as a product owner. We have a 66.1% drop-off at the offer stage and a 14% default rate. Draft a PRD for a new offer screen that fixes this... Let's proceed to the one-page Go/No-Go Recommendation."*
→ **Result:** The AI drafted a comprehensive PRD and Go/No-Go strategy, but missed several critical business constraints that required immediate human correction (detailed below).

## Where the AI missed a real constraint or misread the data, and how it was caught

**1. The PRD's feature claimed to fix a bottleneck it hadn't actually built a fix for.**
Section 4 of the PRD named three candidate causes of the 66.1% offer-decline rate: an unattractive flat price, a flat loan amount, and a fixed repayment schedule that may not fit cash flow[cite: 15]. The first draft of the feature built tiered pricing and tiered loan amounts, but left the repayment term fixed and identical for everyone[cite: 15]. 
*The Fix:* I caught this by checking the feature's actual scope against the three bottlenecks it claimed to address[cite: 15]. I forced the AI to include a "Repayment schedule selector" (Tenor Toggle) in the Comprehensive PRD so all candidate bottlenecks are addressed by the shipped feature[cite: 15].

**2. Missing the Regulatory Transparency Constraint (Hidden Fees).**
In a PRD draft, the AI suggested hiding the loan fees behind a "See full details" toggle to keep the UI clean. I flagged this as a severe regulatory risk, as financial regulators strictly penalize hidden fees. 
*The Fix:* I directed the AI to rewrite the PRD to mandate 100% upfront fee transparency on a single screen by default.

**3. Introducing UX Friction (The NovaWallet Trap).**
To solve the 14% default rate, the AI confidently recommended a "Mandatory NovaWallet Auto-Debit." I caught a major product flaw here: forcing users to pre-fund a specific native wallet just to pay a loan introduces massive friction and would likely worsen our 66.1% abandonment rate. 
*The Fix:* I corrected the AI's logic and pivoted the strategy to a **Specific Account Direct Debit Mandate (Card Tokenization)**. This gives Risk their guaranteed recovery without forcing the user to manually move funds.
