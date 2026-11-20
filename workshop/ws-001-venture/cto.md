# WS-001 memo: CTO seat

**Seat:** CTO (sub-agent, no authority) · **Date:** 2026-11-20 · **Status:** draft for the Board. No decision.

## 1. Verdict: venture-scale, yes with conditions

The technology is not the obstacle and will not be the moat. A solo founder can build a credible pilot product. What makes it a venture is evidence plus data: validated scores and a working outcome-data loop. From my seat, two conditions would change the verdict:

1. **Outcome data has to flow, not just be promised.** At least one employer must send back retention or performance data that we can match to a pseudonymous candidate ID within 90 days of hire. If outcomes only arrive as one-off spreadsheets that nobody owns, the "compounding moat" is a slide, and this is a lean consultancy.
2. **Identity at volume has to be cheap.** Proxy test-takers (someone else holding the phone) are a bigger threat in frontline hiring than AI copy-paste. If identity checks cost more than roughly 20–30% of the per-candidate price **[V]**, the unit economics break.

## 2. Niche ranking (technical fit)

1. **A, frontline hiring: best fit.** Short, structured tasks, offline mobile, high volume and low compute per candidate. It plays to every Ọjà Lab strength.
2. **B, programme selection: easiest build, weakest venture.** The simulator nearly works as it is. But volumes are low and cohort-based, the stakes for cheating are moderate, and there is little outcome data to learn from. It is a good **paid pilot channel** for A, not the company.
3. **C, MSME credit: worst fit for now.** It needs BVN and credit-bureau links, model-risk governance, and adversarial robustness. Borrowers learn to game known signals; LenddoEFL's mixed record is the warning. The security and regulatory build is larger than the product.

I add no D. A UK angle means competing with incumbents on integrations and compliance paperwork, which is their strength and our weakness.

## 3. The seat's view

**Architecture.** This is a split design, and it differs from Ọjà Lab in one key way. In Ọjà Lab the engine and all its rules run on the phone. In assessment, **the scoring key is a secret** and must never ship to the client. So:
- The **client** runs the task engine (scenes, branching, seeded variants) and records an append-only **response log**: choices, timings and the order of events.
- The **server** replays that log through the same engine version, extracts features and computes the score.
- Every score can be rebuilt from `(taskVersion, seed, responseLog, scorerVersion)`. That gives us something to show a candidate who challenges a result, an auditor doing a NYC LL144-style bias audit, or an EU AI Act conformity file. The Act's high-risk employment duties were proposed to move from 2 August 2026 to 2 December 2027, but sources conflict on whether that is final ([DLA Piper, 2026](https://knowledge.dlapiper.com/dlapiperknowledge/globalemploymentlatestdevelopments/2026/The-Digital-AI-Omnibus-Proposed-deferral-of-high-risk-AI-obligations-under-the-AI-Act); [Euronews, 19 Nov 2025](https://www.euronews.com/2025/11/19/european-commission-delays-full-implementation-of-ai-act-to-2027)) **[V]**.

**Mobile and offline.** Ọjà Lab's first paint is about 100 KB gzipped, and its offline play is verified in desktop Chrome only (`poc/README.md`). **It has never been tested on a low-end Android phone**, and that is exactly the target device. In Nigeria, 88% of smartphone users are on Android, and Tecno, Infinix and Itel together hold about 59% of the market ([KPMG/Orange, Sept 2026](https://kpmg.com/ng/en/insights/2026/09/nigeria-smartphone-study.html)). 1 GB of data rose to ₦431.25 after the January 2025 tariff rise ([TechCabal, 6 Aug 2025](https://techcabal.com/2025/08/06/nigeria-loses-one-million-internet-users/)). So an assessment of 3 MB or less costs the candidate about ₦1–2, which is fine. Audio in local languages is the heavy part, so use short, pre-recorded clips. The offline rule: **start online** (ID check, seed issued by the server) and **finish offline** within a set window, with the session flagged as offline-completed.

**Proctoring, identity and anti-cheating.** Vendor data on cheating is noisy. CodeSignal says 35% of proctored assessments were flagged in 2025, and entry-level roles were hit hardest ([CodeSignal blog, 2025](https://codesignal.com/blog/prevent-and-detect-cheating-in-recruiting/)). HireVue says cheating is rare ([HireVue, Oct 2025](https://www.hirevue.com/blog/hiring/mitigating-cheating-enhancing-candidate-experience-ai-hiring)). Both are vendors **[V]**. My layered plan avoids webcam proctoring, which is heavy on bandwidth and creates biometric data:
- **Per-candidate seeded variants issued by the server.** This reuses ADR-018 §4.3: "the server picks the story number … answers cannot be passed around".
- **Time pressure and structured choices.** Asking a phone AI mid-scene is slow and shows up in the timing log.
- **NIN check plus a selfie liveness check** at the start, and once more at random. Indicative prices are $0.04–$0.35 per check ([Didit](https://didit.me/solutions/countries/nigeria/), [Dojah, 2026](https://dojah.io/blog/best-identity-verification-api-africa-2026)). Smile ID's price is quote-only **[V]**.
- **A short on-site confirmation task for shortlisted candidates.** This is the real defence. ADR-018 admits replay "cannot prove who was holding the phone".

**Scoring pipeline.** Response log → deterministic feature extraction (versioned) → **transparent scoring key** (weights set by the I-O psychologist; no black-box machine learning in the MVP) → score band plus written reasons → adverse-impact monitor (four-fifths rule by group, where lawful to collect) → **a human recruiter decides**. Ọjà Lab's ADR-001 rule becomes stricter here: **the LLM never scores a person and never reads free text to judge it.** The LLM may help write scenarios at authoring time, with native-speaker review, and nothing runs live in the MVP.

**ATS and HRIS integrations.** Most Nigerian frontline employers probably run hiring on spreadsheets, WhatsApp and agency lists, not Workday **[V]**. The MVP needs SMS/WhatsApp invite links, a results dashboard, CSV export, one webhook and a CSV outcome upload.

Later, for multinational buyers, a unified ATS API: Merge lists 50+ ATS systems, with write endpoints for Greenhouse, SmartRecruiters and Workday ([Merge docs](https://docs.merge.dev/merge-unified/ats/integrations/overview); some are marked beta) **[V]**.

**Scale.** The content is static, the logs are small and scoring is cheap. 100,000 candidates a month is trivial on serverless hosting (Ọjà Lab already replays on a Netlify function). Variable cost is messaging, ID checks and support, not compute.

**Security.** Almost all of this is new. Ọjà Lab holds no personal data and has no accounts beyond the ADR-018 proposal. We need per-employer tenant isolation, encryption, identity and score stores joined only by a pseudonymous key, access logs, a data-residency decision (NDPA/GAID cross-border rules) and an external penetration test before the first live candidate.

**MVP build estimate (judgement, not measured).** The MVP is one role (agent-banking field agent), 4–6 tasks totalling about 20 minutes, the candidate app, the employer dashboard, server replay and scoring, a vendor ID check, an adverse-impact report and an audit log.
- **Engineering, solo with AI help:** about 10–14 weeks to pilot grade. Reusing Ọjà Lab saves an estimated 30–40% **[V]**.
- **Production hardening** (security review, penetration test, monitoring, data-subject rights tooling): another 8–12 weeks.
- **Content and job analysis are the critical path.** That is 4–8 weeks in parallel, and it needs the psychologist.

## 4. What carries over and what is new

**Carries over (as patterns, not code):** the seeded PRNG with substreams, integer maths, the hash-chained ledger (it becomes the audit trail), server replay (ADR-018 addendum), the slot validator and adversarial mock, scenario-as-data with provenance, the small offline PWA shell, and the governance habit.

The PoC is labelled "must not be merged into a production codebase without the Development Readiness Gate". So we **extract and re-review** the core into a new repository; we do not copy the spike.

**Must be new:** server-only secret scoring, timing capture outside the engine (Ọjà Lab bans `Date.now` inside it), identity checks, accounts and multi-tenancy, an item bank, adverse-impact monitoring, the outcome-data join, consent and data-rights flows, and integrations.

SCN-005's eight-area dual score is a UX idea for the candidate feedback report only. Its weights are uncalibrated and must not be reused as a scoring model.

**Challenges to the founder's points:**
- Point 3, the outcome-data moat, is mostly a data-engineering and contract problem, not a modelling one.
- Point 4, multi-country from the start: **architect** for it (per-country locale, norms and storage), but **launch** in one country. Every new country multiplies the norm groups and validation work.

## 5. Risks and red lines

**Red lines:** no LLM in scoring; no score that cannot be replayed exactly; no stored video or face templates beyond the ID check; no black-box model in the MVP; no candidate data near Ọjà Lab's systems.

**Risks:** low-end devices fail in the field; item banks leak via WhatsApp; offline windows are used to get help; ID-check cost and NIN database uptime (98% average in 2024, [TechCabal, 29 Nov 2024](https://techcabal.com/2024/11/29/smile-id-releases-nigerias-first-ever-ekyc-report-hits-200m-identity-verification-checks/)); and the solo founder is a single point of failure for security and on-call.

## 6. First 90 days

1. **Extract the core and add server replay plus timing capture.** Pass: 1,000 seeded sessions produce byte-identical scores on the server and on 3 device types, with zero drift.
2. **Field test on low-end Android:** 20 people, sub-$120 phones, poor signal. Pass: at least 95% completion, median data use under 3 MB, no crashes, and at least 95% recovery from forced offline drop-outs.
3. **Red-team the cheating defences:** 10 testers, using AI help and proxy takers. Pass: AI-assisted runs score no better than honest runs (threshold to be set with the psychologist), and at least 90% of proxy attempts are caught by the ID check plus the confirmation task.
4. **Pilot plumbing with one employer.** Pass: at least 200 candidates go from invite to result to CSV, at least 90% need no manual work from the founder, and one outcome file is matched at 80% or better.
5. **Security gate.** Pass: the privacy impact assessment (DPIA) is drafted, the external penetration test is complete, and no high or critical findings are open before the first live candidate.
