# WS-001 memo: CTO seat

**Seat:** CTO (sub-agent, no authority) · **Date:** 2026-11-20 · **Status:** draft for the Board. No decision.

## 1. Verdict: venture-scale, yes with conditions

Technology is neither the obstacle nor the moat; a solo founder can build a credible pilot. Validated scores plus a working outcome-data loop make it a venture. Two conditions would change my verdict:

1. **Outcome data must flow, not just be promised.** At least one employer must send retention or performance data that we can match to a pseudonymous candidate ID within 90 days of hire. Otherwise the "compounding moat" is a slide.
2. **Identity at volume must be cheap.** Proxy test-takers (someone else holding the phone) are a bigger frontline threat than AI copy-paste. If identity checks cost more than about 20–30% of the per-candidate price **[V]**, the unit economics break.

## 2. Niche ranking (technical fit)

1. **A, frontline hiring: best fit.** Short structured tasks, offline mobile, high volume, little compute per candidate.
2. **B, programme selection: easiest build, weakest venture.** The simulator nearly works as is, but volumes are low and outcomes few. A good **paid pilot channel** for A.
3. **C, MSME credit: worst fit now.** Credit-bureau links, model-risk governance and borrowers gaming known signals (LenddoEFL's mixed record) make the regulated build bigger than the product.

No D: a UK angle means fighting incumbents on integrations and compliance paperwork, their strength.

## 3. The seat's view

**Architecture.** One key change: in Ọjà Lab every rule runs on the phone; here **the scoring key is secret** and stays on the server.
- The **client** runs the task engine (scenes, branching, seeded variants) and records an append-only **response log**: choices, timings and the order of events.
- The **server** replays that log through the same engine version and computes the score.
- Any score can be rebuilt exactly from `(taskVersion, seed, responseLog, scorerVersion)`. That answers candidate challenges, NYC LL144-style bias audits and EU AI Act files. The Act's high-risk employment duties were proposed to move from 2 August 2026 to 2 December 2027, and sources conflict on whether that is final ([DLA Piper, 2026](https://knowledge.dlapiper.com/dlapiperknowledge/globalemploymentlatestdevelopments/2026/The-Digital-AI-Omnibus-Proposed-deferral-of-high-risk-AI-obligations-under-the-AI-Act); [Euronews, 19 Nov 2025](https://www.euronews.com/2025/11/19/european-commission-delays-full-implementation-of-ai-act-to-2027)) **[V]**.

**Mobile and offline.** Ọjà Lab's first paint is about 100 KB gzipped. But its offline play is verified only in desktop Chrome, and it has **never been tested on a low-end Android phone** (`poc/README.md`). That is exactly our target device. In Nigeria, 88% of smartphone users run Android, and Tecno, Infinix and Itel hold about 59% of the market ([KPMG/Orange, Sept 2026](https://kpmg.com/ng/en/insights/2026/09/nigeria-smartphone-study.html)). 1 GB of data costs ₦431.25 since the January 2025 tariff rise ([TechCabal, 6 Aug 2025](https://techcabal.com/2025/08/06/nigeria-loses-one-million-internet-users/)). A 3 MB assessment costs about ₦1–2; keep local-language audio short and pre-recorded. The rule is: **start online** (ID check, server-issued seed), **finish offline** within a set window, and flag the session as completed offline.

**Proctoring, identity and anti-cheating.** Vendor data conflicts: CodeSignal flagged 35% of proctored assessments in 2025, worst at entry level ([CodeSignal, 2025](https://codesignal.com/blog/prevent-and-detect-cheating-in-recruiting/)); HireVue says cheating is rare ([HireVue, Oct 2025](https://www.hirevue.com/blog/hiring/mitigating-cheating-enhancing-candidate-experience-ai-hiring)) **[V]**. Layers, with no webcam proctoring (bandwidth, biometric data):
- **Server-issued, per-candidate seeded variants,** reusing ADR-018 §4.3, where the server picks the story so "answers cannot be passed around".
- **Time pressure and structured choices.** Asking a phone AI mid-scene is slow, and the delay shows in the timing log.
- **A NIN check plus a selfie liveness check** at the start and once at random. Indicative prices are $0.04–$0.35 per check ([Didit](https://didit.me/solutions/countries/nigeria/); [Dojah, 2026](https://dojah.io/blog/best-identity-verification-api-africa-2026)). Smile ID quotes on request **[V]**.
- **A short on-site confirmation task for shortlisted candidates.** This is the real defence: ADR-018 admits replay "cannot prove who was holding the phone".

**Scoring pipeline.** Response log → versioned deterministic features → **transparent scoring key** (weights set by the I-O psychologist, no black-box machine learning) → score band with written reasons → four-fifths adverse-impact monitor by group, where lawful → **a human recruiter decides**. ADR-001 gets stricter: **the LLM never scores a person or judges free text.** It may help draft scenarios, with native-speaker review, but never runs during a live assessment.

**ATS and HRIS integrations.** Nigerian frontline employers probably hire via spreadsheets, WhatsApp and agencies, not Workday **[V]**. The MVP needs SMS/WhatsApp invites, a dashboard, CSV export, one webhook and CSV outcome upload. Multinationals later need a unified ATS API; Merge lists 50+ ATS systems, including Greenhouse, SmartRecruiters and Workday, some still in beta ([Merge docs](https://docs.merge.dev/merge-unified/ats/integrations/overview)) **[V]**.

**Scale.** 100,000 candidates a month is trivial on serverless hosting (Ọjà Lab already replays in a Netlify function). Variable cost is messaging, ID checks and support.

**Security.** Almost all new: Ọjà Lab holds no personal data. We need per-employer isolation, encryption, identity and scores in separate stores linked by a pseudonymous key, access logs, an NDPA/GAID data-residency decision and a penetration test before the first live candidate.

**MVP build estimate (judgement).** One role (agent-banking field agent), 4–6 tasks totalling about 20 minutes, candidate app, employer dashboard, server scoring, vendor ID check, adverse-impact report and audit log.
- **Engineering, solo with AI help:** 10–14 weeks to pilot grade. Reuse saves about 30–40% **[V]**.
- **Production hardening:** another 8–12 weeks.
- **The critical path is content and job analysis:** 4–8 weeks in parallel, and it needs the psychologist.

## 4. What carries over and what is new

**Carries over, as patterns not code:** the seeded generator with substreams, integer maths, the hash-chained ledger (now the audit trail), server replay, the slot validator and adversarial mock, scenario-as-data with sources, the small offline shell, and the governance habit. The PoC must not enter production without its Readiness Gate, so we **extract and re-review** the core into a new repository.

**Must be new:** server-only scoring, timing capture outside the engine (Ọjà Lab bans `Date.now` inside it), identity checks, multi-employer accounts, an item bank, adverse-impact monitoring, the outcome-data join, consent flows and integrations.

SCN-005's dual score is a feedback-report idea only; its uncalibrated weights must not become the scoring model.

**Two challenges to the founder's points:**
- **Point 3, the outcome-data moat,** is mainly a data-engineering and contract problem, not a modelling one.
- **Point 4, multi-country from the start:** build the architecture for many countries, but **launch in one**. Each new country multiplies the norm and validation work.

## 5. Risks and red lines

**Red lines:** no LLM in scoring; no score that cannot be replayed exactly; no stored face data beyond the ID check; no black-box model in the MVP; no candidate data near Ọjà Lab's systems.

**Risks:** phones failing in the field; items leaking on WhatsApp; the offline window used for help; ID-check cost and NIN uptime (98% average in 2024, [TechCabal, 29 Nov 2024](https://techcabal.com/2024/11/29/smile-id-releases-nigerias-first-ever-ekyc-report-hits-200m-identity-verification-checks/)); a founder alone on security and on-call.

## 6. First 90 days

1. **Extract the core; add timing capture and server replay.** Pass: 1,000 seeded response logs recorded on 3 device types replay on the server to byte-identical ledgers and scores.
2. **Field test on low-end Android.** 20 people, sub-$120 phones, poor signal. Pass: 95% or more complete, median data under 3 MB, no crashes, 95% or more of forced drop-outs recover.
3. **Red-team the cheating defences.** 10 testers try AI help and proxies. Pass: AI help gives no gain beyond a margin set with the psychologist; 90% or more of proxies caught.
4. **Pilot plumbing with one employer.** Pass: 200 or more candidates go from invite to result to CSV, 90% or more need no manual work, and one outcome file matches at 80% or better.
5. **Security gate.** Pass: the privacy impact assessment is drafted, the penetration test is done, and no high or critical findings are open before the first live candidate.
