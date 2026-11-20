# WS-001 memo: Compliance and risk lead

**Seat:** Compliance and risk (a sub-agent with no authority; this is **not legal advice**) · **Date:** 2026-11-20 · **Sources:** checked 2026-11-20 unless stated. **[V]** = unverified, check with counsel.

## 1. Verdict: venture-scale, **yes with conditions**

The law does not block option A. It does make speed and scale more expensive. Two conditions would change my view:

1. **A human decides, and the score only informs.** If the product makes or drives "solely automated" rejections, every target country's law pushes it towards consent-based processing. Consent from job seekers is weak, so the design becomes fragile. With a real human reviewer, the legal path is workable.
2. **The outcome-data moat must have its own lawful basis, not just a clause in the client contract.** An employer cannot sign away its candidates' data-protection rights. If the venture cannot lawfully pool outcome data across clients, founder point 3 (a moat that compounds) fails, and A becomes a services business.

## 2. Niche ranking from this seat

1. **B, programme selection: lowest legal exposure.** The volumes are smaller. Buyers (donors and accelerators) already expect fairness reporting. It is probably not "employment" under the EU AI Act Annex III, though access to vocational training could be argued **[V]**. It is a good place to build validation and governance muscle, but it is a smaller prize.
2. **A, frontline hiring: workable if built in from day one.** It is high-risk under the EU AI Act. It touches anti-discrimination law everywhere, and in South Africa it hits a specific psychometric-testing rule (see below).
3. **C, MSME credit: highest exposure. Do not start here.** It sits under financial regulation, consumer protection and data law at once. Creditworthiness scoring is also high-risk under EU AI Act Annex III. LenddoEFL's mixed record shows how hard it is to prove the validity that regulators and lenders will demand.

D (UK) is not a first market. The UK's rules on automated decisions became more permissive on 5 February 2026, but the Equality Act duties on indirect discrimination and reasonable adjustments still apply in full.

## 3. The seat's view: the legal perimeter

**Nigeria (first market)**
- **Automated decisions (NDPA 2023, s.37):** people have a right not to be subject to decisions based *solely* on automated processing that have legal or similarly significant effects. Exceptions include explicit consent, and human review and contest rights apply ([Mondaq](https://www.mondaq.com/nigeria/privacy-protection/1650166/automated-decisions-profiling-and-data-subject-rights-in-nigeria), 2025; [Templars, AI recruitment](https://www.templars-law.com/app/uploads/2025/08/Legal-Boundaries-of-AI-Driven-Recruitment-in-Nigeria.pdf), Aug 2025).
- **The GAID 2025:** issued 20 March 2025 ([NDPC text](https://ndpc.gov.ng/wp-content/uploads/2025/07/NDP-ACT-GAID-2025-MARCH-20TH.pdf)). It makes a DPIA (data protection impact assessment) mandatory for profiling or scoring and for automated decisions with significant effects. Commentators read it as requiring express consent plus bias safeguards for solely automated decisions ([DLA Piper](https://privacymatters.dlapiper.com/2025/06/nigeria-ndpc-issues-gaid-key-compliance-insights/), Jun 2025). The exact wording is **[V]**.
- **Registration and audit:** registration as a data controller or processor "of major importance", a Data Protection Officer and annual compliance audit returns are all likely **[V on thresholds]**.
- **Employment anti-discrimination:** this is thinner than in the UK. The Constitution (s.42) and the Disability Act 2018 still create claims risk **[V]**. Reputational risk from ethnic, state-of-origin, religious or gender skew is high.

**Ghana:** the Data Protection Act 2012 (s.41) gives a right to reconsideration of solely automated decisions. A replacement bill covering AI and automated decisions was announced in March 2026 and has not been passed ([GNA](https://gna.org.gh/2026/03/govt-to-introduce-new-data-protection-bill-to-regulate-ai-cross-border-data-flows/), Mar 2026).

**Kenya:** the Data Protection Act 2019 (s.35) restricts solely automated decisions with significant effects, has a consent exception and requires reconsideration. Controllers must register with the ODPC (the data regulator), and a DPIA is needed for profiling ([Act text](https://www.odpc.go.ke/wp-content/uploads/2024/02/TheDataProtectionAct__No24of2019.pdf)).

**South Africa:**
- POPIA s.71 restricts solely automated decisions and requires a chance to make representations.
- **The bigger issue is the Employment Equity Act s.8:** psychological tests of employees must be shown to be valid, reliable, fair and unbiased, and certified by the HPCSA (the health professions regulator) or another authorised body **[V on current certification practice]**. This is a hard gate before entering South Africa.

**EU AI Act**
- Under the Digital Omnibus, Annex III high-risk obligations (employment and creditworthiness included) now apply from **2 December 2027**. The Omnibus entered into force on 27 July 2026 ([Lewis Silkin](https://www.lewissilkin.com/insights/2026/07/27/the-digital-omnibus-on-ai-enters-into-force-today-102nedo), 27 Jul 2026; [Orrick](https://www.orrick.com/en/Insights/2026/07/EU-AI-Act-Update-Digital-Omnibus-Finalizes-8-Compliance-Changes), Jul 2026).
- It applies wherever outputs are used in the EU, so it matters for multinational clients.
- The **Article 5 ban on emotion recognition in the workplace has applied since February 2025.** No voice or face "stress" inference, ever.

**UK:** the Data (Use and Access) Act replaced Article 22 with new Articles 22A–22D from 5 February 2026. Automated decisions are now generally allowed, with safeguards, unless special category data is involved ([Travers Smith](https://www.traverssmith.com/knowledge/knowledge-container/uks-data-protection-reforms-take-effect-a-new-era-for-automated-decision-making/), 2026).

**NYC LL144:** requires an annual independent bias audit and publication of a summary. Enforcement was found weak in the December 2025 State Comptroller audit, which signals tightening ([OSC](https://www.osc.ny.gov/state-agencies/audits/2025/12/02/enforcement-local-law-144-automated-employment-decision-tools), 2 Dec 2025). This is only relevant much later.

**Consent and power imbalance:** a job seeker cannot freely refuse a test the employer requires. So:
- Do **not** rely on consent as the legal basis for running the assessment. Use the employer's legitimate interests or steps before a contract, as the law allows.
- Keep consent only for genuinely optional uses: research, reuse of data for norming, and voluntary demographic data.
- The GAID's consent requirement for automated decisions is another reason to keep a human in the loop.

**Fairness and adverse-impact testing**
- Collect demographic data (ethnicity, religion and disability are sensitive data) **voluntarily, separately and firewalled from scoring**.
- Test impact ratios by group, using the four-fifths rule only as an alarm, not a safe harbour. Minimum sample sizes must be set with an I-O (occupational) psychologist.
- Test for **proxy bias that is local to Nigeria:** Pidgin versus English versions, device class, offline versus online, region, and state of origin. On low-end Android, connectivity tracks income and region.

**Rights to outcome data**
- The employer is the controller of candidate data, and the venture is its processor for the assessment. Once the venture pools retention or performance data across clients to improve models, it becomes a **controller in its own right**.
- That needs four things: notice to the candidate at the time data is collected, a compatible purpose, pseudonymisation, and a retention limit.
- Contract terms give access to the data. They do not give a legal basis to use it.

**Cross-border transfers:** cloud hosting outside Nigeria is a transfer. It needs a Commission adequacy decision or an approved transfer instrument under GAID Article 45 and Schedule 5 ([Digital Policy Alert](https://digitalpolicyalert.org/event/33614-data-protection-commissions-general-application-and-implementation-directive-including-cross-border-data-transfer-regulation-ndpcndp-act-gaid012025-enters-into-force), 2025). Being "multi-country from the start" (founder point 4) multiplies these regimes. Start in one country, with a regional data architecture.

**Credit (option C)**
- FCCPC (the consumer protection commission) digital lending rules (the DEON Regulations 2025) ban scraping of contacts, call logs and photos, and require lenders to register ([Chambers Fintech 2026](https://chambers.com/practice-guides/guides/fintech-2026/nigeria/law-and-practice)).
- The CBN's 2019 consumer protection framework binds licensed lenders.
- Sharing scores across lenders may count as credit bureau activity needing a CBN licence **[V]**.
- A credit denial is a textbook "significant decision" under s.37.

## 4. What carries over from Ọjà Lab, and what must be new

**Carries over (a real asset):**
- The deterministic, replayable engine and the hash-chained ledger give reproducible scores and tamper-evident logs. Those are exactly what EU AI Act record-keeping and contest rights need.
- The "LLM writes words only" rule means no LLM does the scoring, which makes scores explainable.
- The habits of a decision log, privacy screening and a claims evidence file become the starting point for technical documentation.

**Must be new:**
- a lawful-basis map for each processing purpose;
- a controller/processor contract template;
- candidate notices in plain English and Pidgin;
- a disability accommodation route;
- a human-review and appeal workflow;
- adverse-impact monitoring;
- a retention schedule;
- transfer instruments;
- breach response;
- a new founding red-lines decision, because DEC-001 does not bind this venture.

**SCN-005's uncalibrated weights must never inform a live decision.**

## 5. Risks and red lines

**Red lines (proposed for a founding decision):**
- no solely automated rejection;
- no emotion, face or voice-affect inference;
- no sensitive data used as scoring inputs;
- no sale or sharing of candidate data outside the hiring purpose (no blacklists);
- no validity claims without evidence;
- no candidates under 18;
- no scraping of device data.

**Top risks:**
- a public bias incident, such as ethnic or regional skew;
- NDPC enforcement over a missing DPIA or an unlawful transfer;
- the outcome-data basis failing;
- South African certification blocking expansion;
- clients misusing scores as hard cut-offs.

## 6. The first 90 days

1. **Get a written perimeter opinion from Nigerian data protection counsel** on s.37, the GAID and the outcome-data plan. *Pass:* the opinion is in hand by day 45 and confirms the human-in-the-loop design and a lawful basis for pooling outcome data. *Fail:* pooling is unlawful, so redesign the moat.
2. **Complete a GAID-format DPIA before any live candidate.** *Pass:* signed off, with residual risk not "high", or the NDPC has been consulted.
3. **Run the first pilot in shadow mode.** Scores are hidden from hiring managers and used only for validation. *Pass:* at least 1 employer signs the contract and DPA (data processing agreement) with an outcome-data clause, and at least 80% of 20 test candidates correctly explain the notice back.
4. **Pre-register an adverse-impact protocol with an I-O psychologist.** *Pass:* the protocol is written before data collection, with minimum subgroup sizes and a halt rule (any impact ratio below 0.8 with adequate sample size stops decision use).
5. **Decide hosting and transfers.** *Pass:* data stays in Nigeria, or there is a documented approved transfer basis before go-live.
