# WS-001 memo: CTO seat

**Seat:** CTO (sub-agent, no authority) · **Date:** 2026-11-20 · **Status:** draft for the Board. No decision.

## 1. Verdict: venture-scale, yes with conditions

The technology is not the obstacle and will not be the moat. A solo founder can build a credible pilot product. What makes this a venture is evidence plus data: validated scores and a working outcome-data loop. Two conditions from my seat would change the verdict:

1. **Outcome data must flow, not just be promised.** At least one employer must send retention or performance data that we can match to a pseudonymous candidate ID within 90 days of hire. If outcomes arrive only as one-off spreadsheets, the "compounding moat" is a slide and this is a lean consultancy.
2. **Identity at volume must be cheap.** In frontline hiring, proxy test-takers (someone else holding the phone) are a bigger threat than AI copy-paste. If identity checks cost more than about 20–30% of the per-candidate price **[V]**, the unit economics break.

## 2. Niche ranking (technical fit)

1. **A, frontline hiring: best fit.** It uses short structured tasks, offline mobile, high volume and little compute per candidate. Every Ọjà Lab strength applies.
2. **B, programme selection: easiest build, weakest venture.** The simulator nearly works as it is. But volumes are low and come in cohorts, and there are few outcomes to learn from. It is a good **paid pilot channel** for A, not the company.
3. **C, MSME credit: worst fit now.** It needs BVN and credit-bureau links, model-risk governance and robustness against borrowers who learn to game known signals. LenddoEFL's mixed record is the warning. The security and regulatory build would be bigger than the product.

I add no D. A UK angle means competing with incumbents on integrations and compliance paperwork, which is their strength and our weakness.

## 3. The seat's view

**Architecture.** One key change from Ọjà Lab. In Ọjà Lab every rule runs on the phone. In assessment, **the scoring key is secret** and never ships to the phone.
- The **client** runs the task engine (scenes, branching, seeded variants) and records an append-only **response log**: choices, timings and the order of events.
- The **server** replays that log through the same engine version and computes the score.
- Any score can be rebuilt exactly from `(taskVersion, seed, responseLog, scorerVersion)`. That answers a candidate's challenge and supports a NYC LL144-style bias audit or an EU AI Act file. The Act's high-risk employment duties were proposed to move from 2 August 2026 to 2 December 2027, and sources conflict on whether that is final ([DLA Piper, 2026](https://knowledge.dlapiper.com/dlapiperknowledge/globalemploymentlatestdevelopments/2026/The-Digital-AI-Omnibus-Proposed-deferral-of-high-risk-AI-obligations-under-the-AI-Act); [Euronews, 19 Nov 2025](https://www.euronews.com/2025/11/19/european-commission-delays-full-implementation-of-ai-act-to-2027)) **[V]**.

**Mobile and offline.** Ọjà Lab's first paint is about 100 KB gzipped. But its offline play is verified only in desktop Chrome, and it has **never been tested on a low-end Android phone** (`poc/README.md`). That is exactly our target device. In Nigeria, 88% of smartphone users run Android, and Tecno, Infinix and Itel hold about 59% of the market ([KPMG/Orange, Sept 2026](https://kpmg.com/ng/en/insights/2026/09/nigeria-smartphone-study.html)). 1 GB of data costs ₦431.25 since the January 2025 tariff rise ([TechCabal, 6 Aug 2025](https://techcabal.com/2025/08/06/nigeria-loses-one-million-internet-users/)). So a 3 MB assessment costs the candidate about ₦1–2. Local-language audio is the heavy part, so keep clips short and pre-recorded. The rule is: **start online** (ID check, server-issued seed), **finish offline** within a set window, and flag the session as completed offline.

**Proctoring, identity and anti-cheating.** Vendor data on cheating is noisy. CodeSignal says 35% of proctored assessments were flagged in 2025, with entry-level roles hit hardest ([CodeSignal, 2025](https://codesignal.com/blog/prevent-and-detect-cheating-in-recruiting/)). HireVue says cheating is rare ([HireVue, Oct 2025](https://www.hirevue.com/blog/hiring/mitigating-cheating-enhancing-candidate-experience-ai-hiring)) **[V]**. I propose layers, with no webcam proctoring, which costs bandwidth and creates biometric data:
- **Server-issued, per-candidate seeded variants,** reusing ADR-018 §4.3, where the server picks the story so "answers cannot be passed around".
- **Time pressure and structured choices.** Asking a phone AI mid-scene is slow, and the delay shows in the timing log.
- **A NIN check plus a selfie liveness check** at the start and once at random. Indicative prices are $0.04–$0.35 per check ([Didit](https://didit.me/solutions/countries/nigeria/); [Dojah, 2026](https://dojah.io/blog/best-identity-verification-api-africa-2026)). Smile ID quotes on request **[V]**.
- **A short on-site confirmation task for shortlisted candidates.** This is the real defence: ADR-018 admits replay "cannot prove who was holding the phone".

**Scoring pipeline.** The score is built in fixed steps:
1. The response log goes through versioned, deterministic feature extraction.
2. A **transparent scoring key** turns features into scores. The I-O psychologist sets the weights; there is no black-box machine learning in the MVP.
3. The output is a score band with written reasons.
4. An adverse-impact monitor applies the four-fifths rule by group, where it is lawful to collect group data.
5. **A human recruiter decides.**

ADR-001 gets stricter here: **the LLM never scores a person and never judges free text.** It may help draft scenarios at authoring time, with native-speaker review. No LLM runs during a live assessment.

**ATS and HRIS integrations.** Most Nigerian frontline employers probably hire through spreadsheets, WhatsApp and agencies, not Workday **[V]**. The MVP needs SMS or WhatsApp invite links, a dashboard, CSV export, one webhook and a CSV outcome upload. Later, multinational buyers will need a unified ATS API. Merge lists 50+ ATS systems, including Greenhouse, SmartRecruiters and Workday, some still in beta ([Merge docs](https://docs.merge.dev/merge-unified/ats/integrations/overview)) **[V]**.

**Scale.** Content is static, logs are small and scoring is cheap. 100,000 candidates a month is trivial on serverless hosting; Ọjà Lab already replays runs in a Netlify function. The variable costs are messaging, ID checks and support, not compute.

**Security.** This is almost all new, because Ọjà Lab holds no personal data and has no accounts. We need:
- isolation between employers' data;
- encryption;
- identity and scores kept in separate stores, linked only by a pseudonymous key;
- access logs;
- a data-residency decision under the NDPA and GAID cross-border rules;
- an external penetration test before the first live candidate.

**MVP build estimate (judgement, not measured).** Scope is one role (agent-banking field agent) with 4–6 tasks lasting about 20 minutes in total. It covers the candidate app, an employer dashboard, server replay and scoring, a vendor ID check, an adverse-impact report and an audit log.
- **Engineering, solo with AI help:** 10–14 weeks to pilot grade. Reuse saves about 30–40% **[V]**.
- **Production hardening:** another 8–12 weeks.
- **The critical path is content and job analysis:** 4–8 weeks in parallel, and it needs the psychologist.

## 4. What carries over and what is new

**What carries over, as patterns rather than code:**
- the seeded random-number generator with substreams;
- integer-only money maths;
- the hash-chained ledger, which becomes the audit trail;
- server replay (ADR-018 addendum);
- the slot validator and adversarial mock;
- scenario-as-data, with a source for every number;
- the small offline web-app shell;
- the governance habit.

The PoC says it must not enter a production codebase without the Development Readiness Gate. So we **extract and re-review** the core into a new repository rather than copy the spike.

**What must be new:**
- secret, server-only scoring;
- timing capture outside the engine (Ọjà Lab bans `Date.now` inside it);
- identity checks;
- accounts for many employers;
- an item bank;
- adverse-impact monitoring;
- the outcome-data join;
- consent and data-rights flows;
- integrations.

SCN-005's eight-area dual score is useful only as a design idea for candidate feedback. Its weights are uncalibrated, and it must not become the scoring model.

**Two challenges to the founder's points:**
- **Point 3, the outcome-data moat,** is mainly a data-engineering and contract problem, not a modelling one.
- **Point 4, multi-country from the start:** build the architecture for many countries, but **launch in one**. Each new country multiplies the norm and validation work.

## 5. Risks and red lines

**Red lines:**
- No LLM in scoring.
- No score that cannot be replayed exactly.
- No stored face data beyond the ID check.
- No black-box model in the MVP.
- No candidate data near Ọjà Lab's systems.

**Risks:**
- Low-end phones fail in the field.
- Items leak on WhatsApp.
- Candidates use the offline window to get help.
- ID-check costs, and NIN database uptime, which averaged 98% in 2024 ([TechCabal, 29 Nov 2024](https://techcabal.com/2024/11/29/smile-id-releases-nigerias-first-ever-ekyc-report-hits-200m-identity-verification-checks/)).
- The founder is the only person on security and on-call.

## 6. First 90 days

1. **Extract the core; add timing capture and server replay.** Pass: 1,000 seeded response logs recorded on 3 device types replay on the server to byte-identical ledgers and scores.
2. **Field test on low-end Android.** 20 people use sub-$120 phones on poor signal. Pass: at least 95% complete, median data use is under 3 MB, nothing crashes, and at least 95% of forced offline drop-outs recover.
3. **Red-team the cheating defences.** 10 testers try AI help and proxy takers. Pass: AI-assisted runs beat honest runs by no more than a margin set with the psychologist, and at least 90% of proxies are caught.
4. **Pilot plumbing with one employer.** Pass: 200 or more candidates go from invite to result to CSV, 90% or more need no manual work, and one outcome file matches at 80% or better.
5. **Security gate.** Pass: the privacy impact assessment is drafted, the penetration test is done, and no high or critical findings are open before the first live candidate.
