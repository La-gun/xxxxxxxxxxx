# WS-001 memo: Assessment science (occupational/organisational psychologist seat)

**Date:** 2026-11-20 · **Seat:** Assessment science (sub-agent, no authority) · **Status:** draft for synthesis. Sources were accessed 2026-11-20. **[V]** marks a claim I could not check against a primary source.

## 1. Verdict: venture-scale, **yes with conditions** (today the science is at "not yet")

There is no measurement asset yet. Investors and enterprise buyers pay for **evidence that scores predict outcomes fairly**, not for the engine. Two conditions would turn this into a clear yes:

1. **One local criterion study.** One role, at least 250 people, with a pre-registered plan. It must show an uncorrected validity of at least .20 against a business outcome (early attrition, QA score, cash shortages), and impact ratios of at least 0.80 by gender and language, or an explained, documented gap.
2. **A credentialed I-O psychologist owns the technical manual.** This means a co-founder or chief science officer with equity, not an advisor.

I challenge two of the founder's pillars:
- **The outcome-data moat (pillar 3) compounds slowly.** Criteria are noisy (supervisor ratings have an interrater reliability of about .52, Viswesvaran et al., 1996 **[V]**), differ by employer, and every new role needs its own job analysis.
- **"Multi-country from the start" (pillar 4) cuts sample sizes.** Each country and language version needs its own invariance and adverse-impact evidence. Go deep first, then wide.

## 2. Niche ranking (by how well each niche can be validated)

1. **A, frontline hiring.** It has the strongest literature, high volume, outcomes within 3–6 months and a clear decision. **For the first role, pick the one with the cleanest outcome data, not the biggest market.** Contact centres and in-house fintech support or sales staff have digital QA, handle-time and attrition data. Agent-banking field agents are often not employees, and their outcomes are noisy **[V]**.
2. **D (my addition): development and onboarding of current frontline staff.** I see it as a wedge, not a destination. The stakes are low, it fits Ọjà Lab's reflective DNA, and it builds the incumbent dataset that validation needs.
3. **C, MSME credit.** Repayment is a clean criterion, but faking and coaching incentives are extreme and the evidence is thin and mixed (see LenddoEFL). Enter later, from a validated platform.
4. **B, founder and programme selection.** The criterion (venture success) is rare, slow (3–7 years) and confounded, and cohorts are tiny. It can be sold, but it cannot be validated at venture pace.

## 3. My seat's view

**Constructs for A.** They should come from a proper job analysis: critical-incident interviews, SME panels of field supervisors and an incumbent task survey. My prior list to test:
- dependability with cash and float;
- integrity, meaning resistance to counterproductive behaviour and fraud;
- customer orientation and emotional regulation under pressure;
- practical numeracy (reconciling, commission);
- following procedures;
- sales drive, for sales roles only.

Build scenarios around **job tasks**, not traits. Assessment-centre research shows that simulation scores cluster by exercise more than by dimension.

**Validity evidence, stated precisely:**
- **Schmidt & Hunter (1998)**, *Psychological Bulletin* 124(2): work samples .54, general mental ability (GMA) .51, GMA plus work sample .63. These are *corrected* operational validities from mostly older US data ([PDF](https://is.muni.cz/el/econ/jaro2021/MPH_AHMR/111328406/Schmidt_1998_vyber_selection_methods.pdf)).
- **Sackett, Zhang, Berry & Lievens (2022)**, *J. Applied Psychology* 107(11). They showed that earlier meta-analyses **over-corrected for range restriction**, especially in concurrent studies. Estimates fall by about .10–.20: work samples to about .33 and GMA to about .31 ([SIOP TIP](https://www.siop.org/tip-article/is-cognitive-ability-the-best-predictor-of-job-performance); [Sackett et al., 2023](https://resolve.cambridge.org/core/services/aop-cambridge-core/content/view/A20984B138319E3D432E643978BF026D/S175494262300024Xa.pdf/revisiting-the-design-of-selection-systems-in-light-of-new-findings-regarding-the-validity-of-widely-used-predictors.pdf)).
- In the 2022 revision, structured interviews rank top at about .42 and SJTs come in at about .26 **[V]**.
- **McDaniel et al. (2007)**: SJT validity is about .20–.26, depending on response instructions ([PDF](https://mcdaniel97.github.io/Publications/McDaniel,%20Hartman,%20Whetzel%20&%20Grubb%20(2007)%20pp%20SJT.pdf)).
- **Fair pitch claim:** "Good simulations predict performance at about r = .25–.35 in US research. We have not yet shown this locally." Transportability to Nigeria is **untested**.

**Fairness is not automatic.** In applicant samples, work samples showed Black–White gaps of d ≈ .73, not the earlier .38 (Roth, Bobko, McFarland & Buster, 2008, *Personnel Psychology* 61). Gaps were much smaller for social-skill exercises (d ≈ .21–.27) than for cognitive and knowledge-heavy ones (d ≈ .80) ([record](https://bvbvf1.bib-bvb.de/vufind/PrimoRecord/cdi_proquest_journals_220143196)). **Design rule:** keep the reading load low and use audio prompts in local languages, so that literacy does not become the hidden construct.

**Reliability.** Alpha is the wrong statistic for simulations. Use alternate-form and test–retest reliability, plus generalisability theory if humans or LLMs score anything. The target is at least .70 for the decision composite.

**Norms.** Build applicant norms, not incumbent norms, with at least 300–500 per role and country **[V, rule of thumb]**. Refresh them yearly. Cut scores tied to validity data and SME standard-setting matter more than percentiles.

**Validation design and timeline:**

| Phase | Months | Sample | Output |
|---|---|---|---|
| Job analysis | 0–2 | 8+ SMEs, 100+ survey respondents | Construct and criterion plan |
| Pilot (no decisions) | 2–4 | 150 | Reliability, DIF across languages, device completion |
| Concurrent study | 4–7 | 250–300 incumbents | First validity and adverse-impact estimates |
| Predictive study | 6–18 | 500+ hires | Validity against 6-month attrition and performance |

Detecting r = .20 with 80% power needs about 194 people. Range restriction and criterion noise push that to 250–300.

**Adverse-impact method:**
- impact ratios (four-fifths rule) with significance tests;
- standardised mean differences (d);
- differential prediction (moderated regression), which needs about 100 or more people per subgroup **[V]**;
- item-level DIF and measurement invariance across English, Pidgin, Yoruba, Hausa and Igbo versions (adapted under the ITC translation guidelines);
- the groups gender, ethnicity or state of origin, region, urban vs rural, age, disability and **device type**.

Ethnicity is sensitive data under the NDPA. Collect it voluntarily, store it apart from scores, and use it only for monitoring.

## 4. What carries over from Ọjà Lab, and what must be new

**Carries over:**
- seeded determinism, which gives cheap parallel forms against item exposure and WhatsApp answer-sharing;
- replay and the hash-chained ledger, for audit and for re-scoring after a key changes;
- a written reason for every score, which supports feedback and ISO 10667 reporting;
- offline play on low-end Android, with Pidgin voices;
- "engine owns numbers, LLM writes words", provided any LLM-varied wording in scored content is shown to be equivalent, or frozen.

**SCN-005 cannot become a selection tool:**
- its 8 "grass to grace" areas are a development framework, not job-analytic constructs;
- its weights are uncalibrated;
- its self-report half will be faked under high stakes;
- its "blind spot" gaps are difference scores, which are less reliable than either part;
- it is bound by DEC-001.

**It can become** a developmental instrument (niche D, after a study). Its "you said vs you played" design is also a ready template for multi-trait multi-method construct validation.

**Must be new:** job-analysis constructs and scoring keys, a technical manual, a fairness protocol, consent built for the employment power imbalance, and its own governance.

## 5. Risks, red lines and the credibility bar

**Red lines:**
- No live hiring decisions on unvalidated scores. Use is advisory until the concurrent study passes.
- No meta-analytic validities presented as our own.
- No unexplained LLM scoring of free text in high-stakes use.
- No "bias-free" claims.

**Risks:**
- **"Resists AI cheating" is plausible but unproven.** Screen-reading agents can play simulations, so red-team it **[V]**.
- **South Africa.** EEA section 8 requires tests that are valid, reliable, fair and unbiased. The HPCSA certification clause 8(d) appears to have been deleted from 1 January 2025. Confirm in the Gazette ([Acts Online](https://www.acts.co.za/employment-equity-act/8__psychological_testing_and_other_similar_assessments.php)).

**The credibility bar:**
- **Nigerian buyers** will ask for a technical manual, local references and adverse-impact reports.
- **Multinationals and investors** will benchmark against the **SIOP Principles** (5th ed., 2018; [Cambridge](https://resolve.cambridge.org/core/journals/industrial-and-organizational-psychology/article/principles-for-the-validation-and-use-of-personnel-selection-procedures/730C076329F88919D5C81C6E7D304FE2)) and **ISO 10667-1/-2:2020** (a revision is in progress; [ISO](https://www.iso.org/standard/74717.html)).
- The **EFPA Test Review Model** ([v2025](https://www.infocop.es/wp-content/uploads/2025/09/efpa_test_review_model_v2025_5.pdf)) and **BPS registration** (5-year certificate; the page says submissions are paused, [BPS](https://www.bps.org.uk/about-bps-test-reviews-and-registration-0)) are year-2 credentials. Write the manual to their template now.

**Co-founder: yes.** Get a Chartered Occupational Psychologist, an HPCSA-registered industrial psychologist, or a PhD-level I-O psychologist, ideally with African field experience. Start fractional if necessary, but make it an equity role before any seed round. Due diligence will ask, "Who signs the validity claims?"

## 6. The first 90 days

| # | Action | Pass/fail |
|---|---|---|
| 1 | Sign a credentialed I-O lead | **Pass:** signed by day 45. **Fail:** no live candidates and no validity claims |
| 2 | Job analysis for one role with one design-partner employer | **Pass:** 40+ critical incidents, 8+ SMEs, 100+ survey responses, and at least 5 constructs rated critical by 75% or more of SMEs |
| 3 | Pilot 3–4 scenarios (n ≥ 150, no decisions) | **Pass:** retest or alternate-form reliability ≥ .70; completion ≥ 85% on low-end Android; no large DIF between English and Pidgin |
| 4 | Secure criterion data | **Pass:** agreements signed covering 300+ incumbents with named outcome metrics from 2 or more employers |
| 5 | Pre-register the validation and fairness analysis plan | **Pass:** an external I-O reviewer finds no blocking issues |
