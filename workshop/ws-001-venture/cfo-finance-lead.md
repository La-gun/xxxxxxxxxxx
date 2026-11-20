# CFO memo: WS-001, behavioural assessment venture

- Date: 2026-11-20 · Seat: CFO / finance lead (sub-agent, no authority, no outreach, no spending) · Status: draft for synthesis
- **[A]** = my assumption. **[V]** = unverified claim. Sourced figures carry a URL and access date (all accessed 2026-11-20).
- FX **[A]**: USD 1 = NGN 1,355, close to the reported official rate on 16 Nov 2026 (parallel market about 1,390) ([techeconomy.ng](https://techeconomy.ng/dollar-to-naira-exchange-rate-today-november-16-2026), news report, not CBN data **[V]**).

## 1. Verdict: Not yet. It is close to "yes, with conditions", but it is not a lean business

The model can reach USD 10M ARR on paper, but only if three things hold: the venture sells well beyond Nigeria, it charges a blended price of about USD 3.50–4 per assessment, and it runs about 2.6M assessments a year (section 3). Today none of the inputs has been tested. There is no product, no validity evidence, no psychologist and no buyer.

Two conditions would move me to **yes, with conditions**:
1. **A buyer ROI case of at least 3×.** Using real data from 2–3 buyers, the money saved per hire (from lower early attrition or losses) must be at least three times the assessment spend per hire.
2. **Committed volume.** At least two buyers must state 10,000+ assessments a year at USD 3 or more, and one must sign a paid pilot LOI.

**Challenging the founder's four tests:**
- **#2 Volume.** Volume is necessary, but emerging-market unit prices are low, so the volume has to be very large.
- **#3 Outcome data.** It is only a moat if contracts require regular HRIS feeds. Buyers will want a discount for that, so budget about 10–15% of price **[A]**.
- **#4 Multi-country from the start.** No. Every new role in every new country needs its own norming and validation, at about USD 30–60k each **[A]**. Stay in two countries at most until ARR reaches USD 1M.

## 2. Niche ranking (CFO seat)

| Rank | Niche | Reason |
|---|---|---|
| 1 | **A, weighted towards contact centres/BPO and bank sales roles** | These have the most hires per buyer and a real cost when hires leave early. BPOs earn in USD, so they can pay in USD. |
| 2 | **C, MSME credit** | Very high value per decision and huge volume. But it needs loan-loss data, a regulatory opinion and 12–24 month cycles. LenddoEFL's pricing (integration fee, scorecard build, per-score price with monthly minimums) shows the shape of the model, not the price ([Caribou](https://caribou.global/publications/can-your-personality-get-you-a-credit-score/)). Treat it as a later expansion, not a starting point. |
| 3 | **B, programme selection** | Cheapest to validate and closest to Ọjà Lab. But the revenue ceiling is about USD 2–5M **[A]** and grant money is lumpy. Use it as a cash bridge only. |
| 4 | **D, UK** | Higher prices (about USD 10–40 per assessment **[A]**), but the market is crowded and Equality Act exposure is high. Revisit after the evidence exists. |

**Candid point on A:** Nigerian POS "agents" are mostly independent merchants who are onboarded, not employees who are hired. There are about 2M of them, and since April 2026 the CBN requires each agent to work with a single principal ([TechCabal, 7 Oct 2025](https://techcabal.com/2025/10/07/cbn-bans-agents-owning-multiple-moniepoint-opay-palmpay-terminals/)). The decision there is really about risk and fraud, which drifts towards C.

## 3. Seat view

**Pricing model.** Charge per completed assessment, sold as prepaid annual credits with a platform minimum. Add a self-serve subscription tier for the mid-market.
- **Reject per-hire pricing.** The vendor carries the hire-rate risk, it needs ATS data, and cash arrives slowly.
- **Global anchor.** TestGorilla Core runs about USD 1,620–1,700 a year. The 750-credit tier is USD 2,580, which is about USD 3.44 per credit ([Noon, read 28 Sep 2026](https://www.noon.ai/blog/articles/326-testgorilla-pricing-2026); [G2](https://www.g2.com/products/testgorilla/pricing)) **[V, aggregators]**.
- **Currency.** Price in USD, or in NGN indexed to USD.

**Price points [A]**

| Segment | USD per assessment |
|---|---|
| Nigeria: fintech agents, retail | 1.50–3 |
| Nigeria: banks, BPO | 3–5 |
| SA / Kenya / Egypt BPO | 4–8 |
| UK (D) | 10–40 |

**Buyer ROI test [A]** (this sets the price ceiling)

| | SA contact centre | NG fintech field agents |
|---|---|---|
| Hires a year | 500 | 2,000 |
| Candidates assessed per hire × price | 6 × USD 5 | 3 × USD 3 |
| Assessment spend | USD 15,000 | USD 18,000 |
| Cost per early leaver | USD 2,000 | USD 150 |
| 5-point drop in early attrition, saved | USD 50,000 | USD 15,000 |
| **ROI** | **3.3×** | **0.8×** |

Reported South African contact-centre attrition is 20–40% a year ([Shiftmate](https://shiftmate.co.za/resources/blog/burnout-south-africa-call-centres-hiring-problem-2026)) **[V, vendor blog]**. A relayed Deloitte figure puts the fully loaded replacement cost at USD 10–20k per agent ([Outsource Accelerator](https://www.outsourceaccelerator.com/glossary/call-center-attrition/)) **[V, developed-market]**. My USD 2,000 is deliberately conservative.

**Conclusion:** Nigerian field agents do not pay back at USD 3 unless fraud and float losses are counted.

**Unit economics per assessment [A]**

| Line | Base | Stress |
|---|---|---|
| Price | 3.50 | 2.00 |
| LLM (words only) + hosting | 0.06 | 0.15 |
| Identity / liveness check | 0.25 | 0.50 |
| Candidate data or airtime | 0.10 | 0.30 |
| Support, QA, payments/FX | 0.22 | 0.30 |
| **Gross margin** | **82%** | **38%** |

**Revenue path to about USD 10M ARR (clients × price × volume) [A]**

| Segment | Clients | Assessments per client a year | USD each | ARR |
|---|---|---|---|---|
| BPO / contact centres (SA, KE, EG, NG) | 25 | 40,000 | 5.00 | 5.0M |
| Banks and fintech agent networks (NG, KE, GH) | 20 | 50,000 | 2.50 | 2.5M |
| Retail, logistics and staffing (mid-market) | 150 | 4,000 | 3.50 | 2.1M |
| Platform and integration fees | | | | 0.4M |
| **Total** | **195** | **2.6M assessments** | **about 3.85 blended** | **about 10.0M** |

That is about 7,000 assessments a day across 4–6 countries, roughly 6–8 years after seed **[A]**. Nigeria alone cannot carry it: at USD 3, it would need about 3.3M Nigerian assessments a year.

**LTV/CAC [A]**

| | Enterprise base | Enterprise stress | Mid-market self-serve |
|---|---|---|---|
| ACV (annual contract value) | USD 100k | USD 40k | USD 8k |
| Gross margin × life | 75% × 4 yrs | 60% × 2.5 yrs | 75% × 2 yrs |
| LTV | 300k | 60k | 12k |
| CAC (including the pilot validation) | 60k | 60k | 3k |
| **LTV/CAC** | **5×** | **1×** | **4×** |

What drives LTV/CAC is volume per client, not the price per assessment.

**Cash needs [A]**

| Stage | Low | Base | High |
|---|---|---|---|
| **To first validation study (one role, about 500 candidates, 90-day outcomes, 6–9 months):** | | | |
| I-O psychologist (contract) | 15k | 35k | 50k |
| MVP build (reusing engine patterns) | 15k | 25k | 40k |
| Job analysis and local language | 5k | 7k | 10k |
| Legal and privacy (NDPA DPIA, consent, outcome-data clauses) | 8k | 12k | 20k |
| Candidate incentives, identity checks, hosting | 3k | 5k | 8k |
| Founder stipend (9 months) | 0 | 18k | 27k |
| Contingency 20% | 9k | 20k | 31k |
| **Total to first validity data** | **about 55k** | **about 120k** | **about 185k** |
| **To seed-ready** (1 study, 3–5 paying clients, ARR USD 150–300k; 5 people at about USD 35k/month for 18 months) | 450k | 650k | 900k pre-seed |

The seed round itself would be about USD 2–4M. AVCA puts the 2025 median VC deal across all stages at USD 4.0M ([AVCA](https://www.avca.africa/media/umlh132j/avca25-15-vc-annual-report_4.pdf)), and BusinessDay puts the median equity deal at USD 3M ([BusinessDay](https://businessday.ng/technology/article/seed-surge-mega-deal-drought-as-africas-venture-capital-market-enters-new-normal/)). One source reports that only about 5% of African seed rounds convert to Series A ([Technext](https://technext24.com/aphz)) **[V]**.

## 4. What carries over from Ọjà Lab, and what must be new

**Carries over:** integer money and the hash-chained ledger (auditable per-assessment metering and billing); deterministic replay (cheap evidence if a candidate or regulator challenges a result); LLM cost discipline (words only, caps, template fallback, so LLM cost stays under 2% of price); the USD pricing policy and assumptions register; offline play on low-end Android (lower candidate data costs).

**Must be new:** credit-based billing and revenue recognition for prepaid credits; contracts that give rights to outcome data; a validation budget line for every role in every country; professional-indemnity insurance at about USD 5–15k a year **[A]**; an enterprise sales hire.

**Worth nothing commercially:** the SCN-005 scores, because their weights are uncalibrated.

## 5. Risks and red lines

**Risks:** price compression (global self-serve tools already sell at about USD 3.44 per credit); validation fails or shows weak lift, which collapses the ROI case; 6–12 month sales cycles; FX moves; customer concentration; seed-to-Series A attrition.

**Red lines:** never charge candidates (no pay-to-apply); no paid scoring before validity evidence exists; no fee that rewards rejecting candidates; no single client above 40% of revenue; no multi-year NGN contract without USD indexation; no revenue from C before a regulatory opinion.

## 6. First 90 days

These are the CFO-side actions for the Board. I can do none of them myself.

| # | Action | Pass | Fail |
|---|---|---|---|
| 1 | Price and volume interviews with 15 buyers (BPOs, banks, fintech agent networks) | 3 or more buyers state 10k+ assessments a year at USD 3 or more, and 1 paid-pilot LOI of USD 10k or more | Median acceptable price below USD 1.50 |
| 2 | ROI model built on real data from 3 buyers (hires, candidates per hire, 90-day attrition, cost per early leaver) | Savings per hire at least 3× assessment spend per hire | Below 1.5× |
| 3 | Get quotes for the validation study (I-O psychologist plus legal) | All-in cost of USD 120k or less, with first outcome data within 9 months | Above USD 200k |
| 4 | Cost spike: one completed assessment on a low-end Android phone, including the identity check | USD 0.75 or less | Above USD 1.50 |
| 5 | Funding: commitments from non-dilutive grants, pilot fees or pre-seed investors | USD 150k or more, enough to cover the study | Below USD 60k, so stay lean and run B as the bridge |

A real accountant is needed on entity choice, VAT, withholding tax and USD receipts before any invoice is issued.
