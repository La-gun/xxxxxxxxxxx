# Workshop synthesis WS-001: a behavioural assessment venture

- **Date:** 2026-11-20
- **Inputs:** [00-brief.md](00-brief.md), [ceo.md](ceo.md), [cfo-finance-lead.md](cfo-finance-lead.md), [cto.md](cto.md), [compliance-risk-lead.md](compliance-risk-lead.md), [growth-marketing-lead.md](growth-marketing-lead.md), [assessment-science-lead.md](assessment-science-lead.md)
- **Status:** Draft. It recommends only; the Board decides. The seats are sub-agents, not real experts. Figures are assumptions unless sourced in the memos, and **[V]** means unverified.

## Combined verdict: YES, it can be a venture, but NOT YET fundable. GO for a 90-day validation sprint

| Seat | Verdict | Core reason |
|---|---|---|
| CEO | Yes with conditions; "not yet" today | It's a venture only if it sells against a loss line (fraud, disputes, churn), not an HR budget, and shows one hard-outcome validation result |
| CFO | **Not yet** (close to yes with conditions) | USD 10M ARR works on paper but needs 4–6 countries. The Nigerian field-agent ROI is under 1× at USD 3 unless fraud is counted |
| CTO | Yes with conditions | The tech is neither the obstacle nor the moat. Outcome data must actually flow, and ID checks must stay cheap |
| Compliance | Yes with conditions | A human decides, so no automated rejections. Pooling outcome data needs its own lawful basis |
| Growth | Yes with conditions | One anchor buyer at 1,000+ candidates a month sharing outcomes, plus one distribution partner |
| Assessment science | Yes with conditions; the science is "not yet" | One local criterion study (r ≥ .20, impact ratios ≥ 0.80), and an I-O psychologist with equity who signs the validity claims |

**In one paragraph:** Five of six seats say a behavioural assessment business *can* be venture-scale. All six say it is **not fundable today**. Nothing has been measured yet: no validity evidence, no buyer, no psychologist and no real user has touched the engine. The gap is evidence, not technology. The founder's engine skills are a genuine head start; the seats think it is worth about 30–40% of the build. But investors and buyers pay for **proof that scores predict outcomes fairly**, and that proof takes months 4–7 to arrive at the earliest. So the 90 days below set up that proof cheaply. They are not a production build.

## The niche: A wins, but the first role needs a decision

| Seat | Ranking |
|---|---|
| CEO | D (agent-network onboarding and conduct risk) > A > B > C |
| CFO | A, tilted to contact centres, BPO and bank sales > C > B > D (UK) |
| CTO | A > B (pilot channel) > C |
| Compliance | B (lowest legal risk) > A (workable if built in) > C |
| Growth | A, through agent networks and contact centres > B (side door) > C |
| Assessment science | A, with the cleanest-outcome role first > D (development of current staff) > C > B |

**Agreed:**
- **A, frontline hiring, is the core.** Even the CEO's "D" is a re-cut of A.
- **C, MSME credit, comes later for everyone.** It is the biggest prize, but heavily regulated, LenddoEFL's evidence is mixed, and the cycles are long.
- **B, programme selection, is a bridge, not the venture.** It is easiest to build and lowest in legal risk, but it has a low ceiling, donor-funded budgets, and, the science seat warns, it **cannot be validated at venture pace**: venture success is rare and takes 3–7 years to show.
- **No UK in year one.**

**The real split: which role first?**

| | Agent-banking field agents | Contact-centre and customer-support agents |
|---|---|---|
| For | CEO and Growth: a CBN rule from October 2025 makes principals answer for their agents. There is huge volume (Moniepoint alone is put at 400k+ agents) and a fast fintech sale | CFO: buyer ROI is about 3.3× against 0.8×. Science: clean digital outcomes (QA, handle time, attrition). Compliance: these are real employees, so the legal frame is clear |
| Against | Agents are independent merchants, not employees. That makes it onboarding risk (closer to C), outcomes are noisy, and the legal frame is unclear | Smaller headline volume; buyers are more price-sensitive |

**Synthesis recommendation:** run the **first validation study on contact-centre and customer-support agents**. Buyers include fintechs' in-house support teams, for example OPay, which runs both an agent network and high-volume contact-centre hiring, and BPOs such as Outsource Global. Keep **agent onboarding as the second study and as the "why now" story** in the pitch. The same fintech buyer can host both, which turns the disagreement into a sequence.

## The founder's four venture tests, as challenged

| Founder's test | Board view |
|---|---|
| 1. It informs real decisions about people, where budgets sit | **Holds, with a correction.** In Nigeria the money sits with **risk and operations** (fraud, disputes, attrition), not HR. Sell against a number the buyer's CFO already tracks |
| 2. It is built on volume (per candidate) | **Holds, but prices are low** (about USD 1.50–5 per assessment [A]). That means a few very large buyers and **concentration risk**. LTV/CAC depends on volume per client, not price |
| 3. Outcome data builds a moat that compounds | **The weakest claim, according to every seat.** Clients resist sharing, outcomes are noisy, and each learning cycle takes 6–12 months. Legally, pooling data across clients makes the venture a **data controller in its own right**, and a contract clause does not create a lawful basis. The early moat is more likely **workflow position** (being the default screen inside a staffing firm), **local norms** and the **audit trail** |
| 4. It is multi-country from the start | **Rejected as an operating plan, kept as the pitch.** Each country and language needs its own norms, invariance, adverse-impact and transfer work. **Build the architecture for many countries and launch in one.** The tension: the CFO shows **Nigeria alone cannot reach USD 10M ARR**, so the venture case depends on later expansion to SA, Kenya and Egypt BPO markets, from about year 3 |

## The numbers (CFO; all assumptions)

- **Pricing:** per completed assessment, sold as prepaid annual credits with a platform minimum. Per-hire pricing is rejected. Price in USD, or in NGN indexed to USD. The global anchor is TestGorilla at about USD 3.44 a credit [V].
- **Gross margin:** about 82% in the base case, about 38% under stress. The swing costs are the ID check and candidate data, not the LLM.
- **Path to about USD 10M ARR:** about 195 clients, about 2.6M assessments a year, about USD 3.85 blended, across 4–6 countries. That is roughly 6–8 years after seed.
- **LTV/CAC:** 5× for enterprise in the base case, 1× under stress, 4× for mid-market self-serve.
- **Cash to first validity data:** about **USD 120k** (range 55–185k) over 6–9 months. The largest line is the I-O psychologist.
- **To be seed-ready** (1 study, 3–5 paying clients, USD 150–300k ARR): a **USD 450–900k pre-seed**. Seed itself would be about USD 2–4M.
- **Buyer ROI test:** contact centres about 3.3×; Nigerian field agents about 0.8× at USD 3, **unless fraud and float losses count**.

## The build (CTO)

- **MVP: 10–14 weeks solo to pilot grade, plus 8–12 weeks of hardening.** The critical path is **content and job analysis, which needs the psychologist**, not code.
- **The architecture change from Ọjà Lab:** the scoring key is secret and **lives on the server**. The phone records an append-only response log. The server replays it through the same engine version, so every score can be rebuilt exactly. That answers candidate challenges and future bias audits.
- **The LLM never scores a person** and never judges free text. It doesn't run during a live assessment.
- **Cheating:** **proxy test-takers beat AI as the main threat.** The defences are an ID and liveness check, per-candidate seeded variants, timing logs, and a short **on-site confirmation task for shortlisted candidates**.
- **The honest gap:** **Ọjà Lab has never been tested on a low-end Android phone**, which is exactly the target device.
- **Integrations:** WhatsApp/SMS invites, CSV export and outcome upload come first. ATS marketplaces come much later.
- **Carry patterns, not code:** extract the core into a new repository and review it again. Ọjà Lab is still a PoC without its Readiness Gate.

## The science (assessment science)

- **What a fair pitch can claim:** "Good simulations predict job performance at about r = .25–.35 in US research. We have not yet shown this locally."
  - **Sackett et al. (2022)** revised Schmidt & Hunter (1998) downward: work samples about .33 (was .54) and SJTs about .26.
  - Local transportability is **untested**.
- **Fairness is not automatic.** Work samples showed sizeable subgroup gaps (d ≈ .73), mostly driven by reading and cognitive load. Social-skill exercises showed much smaller gaps. **Design rule:** low reading load, audio prompts, and local languages (English, Pidgin, then Yoruba, Hausa and Igbo).
- **Measure job tasks, not traits.** Base it on a proper job analysis: critical incidents, SME panels and a task survey. Candidate constructs: dependability with cash, integrity, customer orientation under pressure, practical numeracy and following procedures.
- **Validation timeline:**

| Stage | Months | Sample |
|---|---|---|
| Job analysis | 0–2 | |
| Pilot, no decisions | 2–4 | n ≈ 150 |
| Concurrent study | 4–7 | 250–300 current staff |
| Predictive study | 6–18 | 500+ hires |

- **Credibility bar:** a technical manual written to the SIOP Principles, ISO 10667 and the EFPA review model. BPS registration is a year-2 credential.
- **SCN-005 (Ọjà Lab's growth profile) cannot become a selection tool.** Its weights are uncalibrated, its self-report half will be faked, and its "blind spot" difference scores are unreliable. Its **"you said vs you played"** design is a useful template for construct validation and for a later development product.

## The law (compliance; not legal advice)

- **Nigeria first:**
  - NDPA 2023 s.37 gives a right not to be subject to *solely* automated decisions with significant effects.
  - GAID 2025 makes a **DPIA mandatory** for profiling and scoring.
  - Registration, a Data Protection Officer and audit returns are likely [V].
- **Don't rely on consent** to run the assessment, because job seekers can't freely refuse. Use legitimate interests or pre-contract steps. Keep consent for optional uses only: research, norming reuse and voluntary demographics.
- **Outcome-data pooling:** the venture becomes a controller and needs notice to candidates at collection, a compatible purpose, pseudonymisation and retention limits. **If counsel says pooling is unlawful, the moat fails and A becomes a services business.**
- **Hosting outside Nigeria is a cross-border transfer** and needs an approved basis.
- **EU AI Act:** employment is high-risk from **2 December 2027** (Digital Omnibus). The **ban on workplace emotion recognition has applied since February 2025**, so never infer stress from a face or voice.
- **South Africa:** Employment Equity Act s.8 requires valid, reliable, fair and unbiased tests. **The seats disagree on whether HPCSA certification is still required**: compliance says yes [V], science says clause 8(d) appears to have been deleted from 1 January 2025. That needs counsel before any SA entry.
- **Credit (C):** FCCPC digital-lending rules (DEON 2025), the CBN consumer framework, and possible credit-bureau licensing.

## Team gaps (agreed)

1. **An I-O psychologist with equity**, as co-founder or chief science officer, not just an advisor. Every seat implies it and the science seat insists. Due diligence will ask "who signs the validity claims?" No live candidates and no validity claims without one.
2. **A commercial co-founder** with Nigerian fintech or BPO enterprise relationships (CEO).
3. **A distribution partner**, either a staffing firm or a job board (Growth). One founder selling one enterprise at a time is not venture scale.

## Proposed founding red lines (a new decision log; Ọjà Lab's DEC-001 does not bind this venture)

1. **No solely automated rejection.** A human decides, and scores inform.
2. **No live decision on unvalidated scores.** Pilots run in **shadow mode**, with scores hidden from hiring managers, until the concurrent study passes.
3. **No LLM in scoring**, and no score that can't be replayed exactly.
4. **No emotion, face or voice-affect inference.** No stored face data beyond the ID check.
5. **No sensitive data as scoring inputs.** Demographics are voluntary, kept separate and used for monitoring only.
6. **No candidate ever pays.** No fee that rewards rejecting people.
7. **No validity claims beyond the evidence.** Never present published meta-analytic figures as our own. No "bias-free", "AI-proof" or "reduces fraud by X%" claims.
8. **No sale or sharing of candidate data outside the hiring purpose.** No blacklists, no under-18s, no device-data scraping.
9. **No credit use (C)** without a regulatory opinion and the right licence.
10. **Halt rule:** any impact ratio under 0.80 on an adequate sample stops decision use until it is explained or fixed.

## Recommended 90-day plan

| # | Action | Owner | Pass threshold |
|---|---|---|---|
| 1 | **Sign a credentialed I-O psychologist** (fractional is fine, with equity) | Founder | Signed by day 45–60 |
| 2 | **20–25 discovery calls:** fintech support and agent networks, contact centres and BPOs, banks, staffing firms | Founder | 3 or more put a **naira number on a loss** and name a budget owner. 3 or more state **10k+ assessments a year at USD 3 or more**. Fail if the median acceptable price is under USD 1.50 |
| 3 | **Design-partner LOI** | Founder | 1 signed: a 500+ candidate pilot *or* 250–300 current staff for a concurrent study, **with outcome data shared under a DPA**. Ideally paid (USD 10k or more) |
| 4 | **Counsel perimeter opinion** (s.37, GAID, outcome pooling, hosting), then a **GAID-format DPIA** | Founder + Nigerian counsel | Opinion by day 45 confirming the human-review design and a lawful basis for pooling. DPIA signed before any live candidate |
| 5 | **Job analysis for one contact-centre or support role** with the design partner | I-O lead | 40+ critical incidents, 8+ SMEs, 100+ survey responses, and 5 or more constructs rated critical by at least 75% of SMEs |
| 6 | **Extract the engine core; add server replay and timing capture** | Founder (CTO role) | 1,000 seeded logs from 3 devices replay to byte-identical scores |
| 7 | **Field test on sub-USD-120 Android phones**, plus a cheating red-team | Founder | 85% or more complete, median time under 15 minutes, under 3–5 MB of data. 90% or more of proxy test-takers caught. AI help gives no gain beyond the agreed margin |
| 8 | **Shadow pilot of 3–4 scenarios** (n ≥ 150, no decisions) | I-O lead | Reliability ≥ .70, no large DIF between English and Pidgin, average fairness rating ≥ 4/5 |
| 9 | **Buyer ROI model** on real data from 3 buyers | Founder (CFO role) | Savings per hire at least 3× assessment spend. Fail if under 1.5× |
| 10 | **Funding for the study** (grants, pilot fees, pre-seed angels) | Founder | USD 150k or more committed. If under USD 60k, stay lean and run B as the bridge |
| 11 | **Channel:** pitch Workforce Group, Jobberman and one other staffing firm | Founder | 1 agrees to co-run a pilot with one of its clients |
| 12 | **Commercial co-founder search** | Founder | 3 credible candidates met |

**The first validity result comes in months 4–7**, from the concurrent study. That is the real "fundable or not" moment, so plan pre-seed conversations around it, not before.

## Kill signals (stop, or drop to a lean business)

- No buyer names a measurable loss and a budget owner after about 20–25 calls.
- No buyer will share outcome data under contract.
- The median acceptable price is under USD 1.50, or buyer ROI is under 1.5×.
- No I-O psychologist is signed by about day 60–90.
- Counsel says cross-client outcome pooling is unlawful. Redesign the moat, or accept a services business.
- No lift over a simple baseline, such as a reference check, or adverse impact that can't be fixed.
- The top two fintech principals say they will build it in-house.

## What carries over from Ọjà Lab, and what doesn't

**Carries over, as patterns:**
- the deterministic, seeded engine and hash-chained ledger, which become the audit trail and also give parallel forms and exact re-scoring;
- "the engine owns the numbers, the LLM writes words", tightened here so the LLM never scores;
- the offline, light shell;
- Pidgin voice craft;
- written reasons for scores;
- governance habits (decision log, DPIA, claims evidence file);
- USD-indexed pricing.

**Must be new:**
- job-analysed constructs and scoring keys;
- a technical manual, norms and validation;
- server-side scoring, identity checks and an item bank;
- multi-employer accounts, security, and data residency;
- consent built for the employer–candidate power imbalance;
- a human-review and appeal route;
- adverse-impact monitoring;
- outcome-data contracts;
- a separate, serious B2B brand. A "business game" brand weakens trust with risk and HR buyers.

**Keep apart:** no candidate data anywhere near Ọjà Lab's systems.

## Board decisions requested

1. **Accept the verdict:** venture-scale is possible but not yet fundable. Approve the 90-day validation sprint, with no production build.
2. **Approve A as the core niche**, with the **first study on contact-centre and support roles** and **agent onboarding as the second study**. Or choose agents first, against the CFO and science view.
3. **Approve B as a cash and evidence bridge only**, and park C (credit) and the UK.
4. **Adopt the ten founding red lines** as this venture's first decisions.
5. **Authorise recruiting an I-O psychologist with equity**, and set the equity range.
6. **Authorise the Nigerian counsel opinion and the DPIA** before any live candidate.
7. **Set the sprint budget** (the CFO's base case is about USD 120k to first validity data) and decide the founder stipend.
8. **Decide on a commercial co-founder search.**
9. **Commission a working name and trademark check** for a separate B2B brand.
10. **Brief counsel on the South Africa EEA s.8 question** before any SA plans.

## Caveats

- The seats are sub-agents with light web research (about 5–8 searches each). Several figures come from vendor blogs, aggregators or press estimates, and are marked [V] in the memos.
- Agent counts, local buyers' current assessment tools, Nigerian price tolerance, NDPA thresholds, the exact GAID wording and SA certification practice are all unverified.
- No buyer has been spoken to. Ọjà Lab, the source of the reusable patterns, has had no real playtest and no low-end Android test.
- Every price, cost and timeline is an assumption to test in the 90 days, not a forecast.
