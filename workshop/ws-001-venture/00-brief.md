# Board workshop WS-001: a behavioural assessment venture

**Date:** 2026-11-20 · **Asked by:** the founder (Board) · **Prepared by:** Claude · **Status:** brief for the executive team. Drafts only, no decision.

## The founder's question

> "Setting out this way, can we not make it a full venture?"

The founder wants to know whether a **behavioural assessment business** can be a **venture-scale company** (fundable, built for large growth), not just a lean consultancy or lifestyle business. They also want to know which vertical niche to go deep in.

Each member writes **one memo** from their own seat. The founder then gets one synthesis.

## What this is, and what it is not

- **A new, standalone venture.** It is *not* a pivot of Ọjà Lab, and Ọjà Lab's rules (including its DEC-001, "data never used against an individual") do **not** bind it. This venture will make or inform decisions about individuals, so its own fairness, consent and legal rules must be designed from scratch.
- **It draws on Ọjà Lab as capability, not as product.** The founder has built Ọjà Lab (`/home/user/ojalab`, **read-only, do not edit**), an Africa-tailored business simulator with these features:
  - a deterministic, seeded, replayable engine with integer money and a hash-chained ledger;
  - "the engine owns every number, the LLM only writes words in validated slots" (ADR-001, in `docs/18-decisions/`);
  - offline play on low-end Android, with Nigerian context and Pidgin voices;
  - a self-reflection "growth profile" (SCN-005) that scores 8 areas twice: from what the player says and from how they play. Its weights are uncalibrated.
  
  It also has heavy governance discipline: a decision log, privacy impact screening and a claims evidence file. No real playtest of Ọjà Lab has happened yet.
- **Solo founder.** The specialist roles are these sub-agents, with no real authority. No occupational psychologist is involved yet.

## Starting hypothesis (to test, not to accept)

**Lead option A: behavioural job simulations for high-volume frontline hiring in emerging markets.**
- **Roles:** agent-banking and fintech field agents, contact centres, retail, logistics, and sales agents.
- **Format:** short, realistic tasks (for example a cash dispute or an angry customer) that measure behaviour under pressure.
- **Delivery:** mobile-first, offline-capable, in local languages and normed on local candidates.
- **Why it might work:**
  - it resists AI cheating better than knowledge tests;
  - it charges per candidate;
  - outcome data (retention, performance) feeds back to improve prediction.
- **Rollout:** start with one role type in Nigeria, then expand pan-African, then to other emerging markets.

**Alternatives to compare against A:**
- **B: founder, accelerator and programme selection.** Simulation-based readiness assessment used by accelerators, donor programmes and investors to select entrepreneurs.
- **C: behavioural credit assessment for MSME lenders.** Psychometric and behavioural signals for thin-file borrowers. This is the biggest prize, and the most regulated and ethically heavy.
- **D, optional, if your seat sees it:** a UK or other developed-market angle, or a different niche you think beats A–C.

**Founder's working view on what makes it a venture rather than a lean business:**
1. It informs real decisions about people, where budgets sit.
2. It is built on volume (per candidate), not bespoke.
3. It has contractual rights to outcome data, which builds a moat that compounds.
4. It is multi-country from the start.

Challenge any of these.

## Known context and caveats

- **Precedents:** SHL (acquired), Pymetrics (raised venture money, later acquired by Harver), HireVue, TestGorilla, Criteria, Plum, Thomas International, Hogan, LenddoEFL (psychometric credit, mixed results). Verify anything you cite.
- **Regulation:**
  - Nigeria: NDPA 2023 and its General Application and Implementation Directive (GAID) of 2025.
  - EU AI Act: employment uses are high-risk, and dates have been moving.
  - UK: UK GDPR and the Equality Act.
  - US: NYC Local Law 144 and EEOC adverse impact.
  - Ghana, Kenya and South Africa data-protection laws, if relevant.
- **AI-enabled cheating** is undermining unproctored knowledge and ability tests industry-wide (2025–26).
- All prices, market sizes and dates you use are estimates unless you cite a primary source. Mark unverified claims **[V]**.

## What each memo should cover (about 900–1,200 words, plain English)

1. **Your verdict on the founder's question:**
   - **Venture-scale: yes**, or **yes with conditions**;
   - **Lean business only**;
   - **Not yet**;
   - **No**.
   
   Give the one or two conditions that would change it.
2. **Your niche ranking:** A, B, C (and D if you add one), ranked from your seat, with the reason.
3. **Your seat's view.** See the seat questions below.
4. **What carries over from Ọjà Lab, and what must be new**, from your seat.
5. **Risks and red lines.**
6. **The first 90 days:** 3–5 concrete actions, each with a pass/fail threshold.

### Seat questions

| Seat | Focus |
|---|---|
| **CEO** | Is this a venture? Market and buyer (who signs, who pays, how often), competition and the wedge, why now, team gaps (co-founder?), the fundraising story, kill signals |
| **CFO** | Pricing model (per assessment, per hire, subscription), emerging-market price points, unit economics, the revenue path to venture scale (what it takes to reach roughly USD 10M ARR, with clients × price × volume), cash needed to the first validation study and to a seed round, LTV/CAC. All figures are assumptions |
| **CTO** | Architecture: reuse of the Ọjà Lab engine patterns (determinism, replay, LLM words only), mobile/offline delivery, proctoring, identity and anti-cheating, scoring pipeline, ATS/HRIS integrations, scale, security, build estimate for an MVP |
| **Compliance and risk** | Legal perimeter by niche and country, consent in employment (power imbalance), automated decision-making, fairness and adverse-impact testing, data rights to outcomes, cross-border transfers, what must exist before the first live candidate |
| **Growth and marketing** | Go-to-market by niche: the first 10 named target buyer types or organisations, channel (direct, staffing firms, ATS marketplaces, partners), candidate experience, positioning against global incumbents, the funnel and sales cycle |
| **Assessment science (new seat: occupational/organisational psychologist)** | What to measure for option A (constructs, job analysis), simulation-based assessment validity evidence, reliability, norms, the validation study design and timeline, adverse-impact methodology, what the SCN-005 work can and cannot become, the credibility bar buyers and investors will apply, and whether the founder needs an I-O psychologist co-founder |

## Rules for this workshop

- You may do **light web research**: up to about 8 searches. Cite sources inline with a URL and a date. Mark anything unverified **[V]**.
- Read Ọjà Lab files only if useful to your seat. Never edit anything under `/home/user/ojalab`.
- Write your memo to `/home/user/xxxxxxxxxxx/workshop/ws-001-venture/<your-seat>.md`. Don't edit any other file.
- You hold no approval, signing or spending authority. The Board decides.
