# NovaLend Product Owner Decision Kit | FirstBank Digital Factory Assessment

**Candidate:** Marvelous Bolaji  
**Target Role:** Product Manager / Product Owner (IT-CIO Organization Department)  

---

## Executive Overview
This repository contains the comprehensive product decision kit and artifact workspace addressing NovaLend's critical dual crisis during its 30-day beta: an unsustainable **14% default rate** (against a mandatory 6% Risk target) and a severe **66.1% offer abandonment rate** under an immovable 6-week regulatory deadline mandated by the CBN.

Rather than applying broad, friction-heavy solutions that worsen user drop-off, this strategy strictly decouples conversion fixes from risk controls to ensure regulatory survival, capital preservation, and long-term Q4 growth.

---

## Repository Structure & Artifacts

The workspace contains five core artifacts and documentation files required for the assessment:

1. **`NovaLend_Data_Driven_Decision_Comprehensive.docx`**  
   *Deconstructs the beta funnel diagnostics, proves the presence of adverse selection (permissive 92.2% approval paired with rigid flat terms), details the three core bottlenecks (rigid amounts, inflexible tenors, non-risk-adjusted pricing), and outlines a 5-day "Painted Door" validation experiment.*

2. **`NovaLend_PRD_Offer_Screen_Comprehensive.docx`**  
   *The comprehensive Product Requirements Document for the post-verification risk-tiered offer screen. Features bounded flexibility via dynamic amount sliders and tenor toggles, real-time pricing recalculations, Material Design 3 UI specs, React Native engineering guidelines, and the 1-tap Decline-Reason Feedback UI.*

3. **`NovaLend_Prioritized_Backlog_Comprehensive.docx`**  
   *A RICE-prioritized backlog mapping features to the strict 6-week engineering constraint. Explicitly de-scopes heavy initiatives like full machine learning model rebuilds (>4-week effort) and prioritizes backend risk cutoffs, tiered pricing engines, and conversion UI.*

4. **`NovaLend_Go_No_Go_Recommendation_Comprehensive.docx`**  
   *Executive recommendation outlining why we must launch with severe restrictions (avoiding front-end payment friction like card tokenization to protect conversion). Includes structural risk justifications, identification of core assumptions, and hard 14-day post-launch kill criteria.*

5. **`NovaLend_Stakeholder_One_Pagers_Comprehensive.docx`**  
   *Tailored, single-page alignment briefs designed specifically for:*
   * **Executive Sponsor:** Focusing on market momentum, risk trade-offs, and Q4 ROI scaling.
   * **Compliance & Risk:** Detailing audit readiness, adverse selection mitigation, automated cutoff thresholds, and 100% upfront fee transparency.
   * **Engineering:** Outlining the 6-week scope lockdown, strict TypeScript guidelines, state transitions, and gesture handling.

6. **`AI_USAGE.md`**  
   *Transparent documentation of AI tooling utilized during the design process, detailing where AI initial suggestions required rigorous human calibration—specifically regarding regulatory fee transparency, avoiding front-end payment friction traps, and bridging structural feature gaps.*

---

## Core Strategic Pillars

*   **The Risk Pillar (Fixing the 14% Default Rate):** Enforces a hard backend **Risk-Tier Strict Cutoff** to automatically decline the bottom quartile of credit applicants before an offer is generated, instantly compressing default trajectories toward the 6% target.
*   **The Conversion Pillar (Fixing the 66.1% Abandonment Rate):** Replaces rigid "all-or-nothing" flat offers with **Post-Verification Risk-Tiered Pricing, Dynamic Amount Sliders, and Tenor Toggles**, giving verified users complete control within safe, pre-approved risk bands.
*   **The Learning Loop:** Integrates a lightweight **Decline-Reason Feedback UI** upon offer rejection to capture precise friction data, feeding future iterations without harming active conversion flows.

---
*Prepared and structured for review by the FirstBank Digital Factory Assessment Panel.*
