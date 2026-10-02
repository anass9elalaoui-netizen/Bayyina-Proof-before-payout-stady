# Bayyina research

Research behind the Bayyina concept: where the insurance market is going in 2026, why evidence trust was chosen, who else is in the space, and what the POC must prove.

Research date: October 2026.

## 1. Summary

Insurers increasingly pay claims on photos, and generative AI now makes those photos easy to fake. Existing vendors either estimate damage, score fraud on claim data, or secure the camera. None joins proof of capture, forensic checks and policy reasoning in one flow for mid-size insurers and multilingual markets. Bayyina does, and it can be shown in a convincing six-week POC by one AI / full-stack engineer.

## 2. Market scan

Eight opportunity areas were reviewed against four criteria: market pain, crowding, whether one engineer can build a credible POC, and fit with an AI/ML + full-stack profile.

| Opportunity | Situation in 2026 | Crowding | Solo POC | Fit |
|---|---|---|---|---|
| **Evidence trust in claims** | AI-faked claim photos rising; capture SDKs exist but are rarely tied to claims reasoning | Gap | Yes | ★★★★★ |
| Insurance for AI agents | Major carriers added AI exclusions in early 2026; new specialists launching | Early | Partly | ★★★★ |
| Agentic claims automation | Main industry trend; most insurers still at POC stage | Very | Yes | ★★★ |
| Parametric climate cover | Premiums projected from $16bn (2024) to $51bn (2034) | Medium | Partly | ★★★ |
| Underwriting copilot | Strong ROI, needs carrier rules | Medium | Partly | ★★★ |
| AI Act governance tools | High-risk deadline moved to 2 Dec 2027 | Medium | Yes | ★★ |
| Sales through AI assistants | Disrupting brokers; many vendors | Very | Yes | ★★ |
| Photo damage estimation | Dominated by specialists with years of data | Very | Hard | ★ |

Stars are a judgement based on the sources below.

## 3. The problem in numbers

- US insurance fraud across all lines: about **$308.6bn a year** (2025 estimate), of which about **$45bn** in property and casualty.
- Allianz: **+300%** doctored claim photos between 2022 and 2023.
- Verisk: **98%** of insurers say AI editing tools increase digital fraud.
- Current image models can fabricate the exact kind of photos claims workflows rely on (Debevoise, January 2026).
- Insurers' current defences: multi-angle photos, original files by post, live video inspections, AI-image detectors. Each adds cost or friction, and detectors age.

## 4. Competition

| Player | Strength | Gap Bayyina fills |
|---|---|---|
| Tractable | Photo-to-estimate, used by about 25 of the top 100 insurers | Not focused on evidence authenticity or policy reasoning |
| Shift Technology | Fraud and claims AI in 35+ countries | Works on claim data after the fact; capture integrity not its core |
| Truepic | C2PA secure-capture SDK | Capture only; no assessment |
| SAS | Agentic fraud screening with vision, OCR and LLM reasoning | Detection after upload; enterprise-only |
| PhotoDetective | Detects AI-generated, edited and reused photos | Detection only |

**Positioning:** Bayyina is the trust layer and the first-pass assessor. It works with damage estimators and fraud platforms rather than replacing them.

## 5. Why now

1. Photorealistic image generation is mainstream.
2. Provenance standards (C2PA "Content Credentials") and open mobile libraries are mature enough to build on.
3. Multimodal LLMs can read photos, policy wording and mixed-language stories in one call and return structured output.
4. Regulators expect human oversight and logging of AI in insurance, which Bayyina has by design.

## 6. Hypotheses

| # | Hypothesis | Test |
|---|---|---|
| H1 | Signed capture removes most fake-photo risk with little friction | Capture completed in < 2 min; 100% of post-capture edits detected |
| H2 | Forensics catch most fakes among unsigned uploads | Recall ≥ 85% at ≤ 10% false alarms on a labelled benchmark |
| H3 | An LLM applies policy clauses reliably when forced to cite them | ≥ 85% agreement with an expert on 50 claims; all citations valid |
| H4 | Multilingual intake works with real customer language | ≥ 90% same incident type across Darija, Arabic, French, mixed |
| H5 | Handlers save time and trust the file | Minutes instead of days; usefulness ≥ 4/5 |

## 7. Data plan

- **Real damage photos:** public car-damage datasets and photos taken with the capture flow.
- **Fakes:** generated damage photos, edited real photos (paste, inpaint, clone), and reused internet images, all labelled. This benchmark is useful whatever product follows.
- **Policies:** 4–6 synthetic policies across countries and currencies (MAD, EUR, AED…), with numbered clauses and exclusions.
- **Claims:** 50 synthetic claims in four languages, including hard cases: dates outside the policy, uncovered guarantees, story and photo mismatches, missing police report.
- **Later:** 20 anonymised real claims from the pilot insurer under a data agreement.

## 8. Risks

| Risk | Mitigation |
|---|---|
| A browser cannot prove pixels came from the camera | Freshness checks and guided capture in the POC; native app with hardware attestation and C2PA in the pilot |
| Detectors age | Forensics is one signal among several, never a verdict alone |
| LLM coverage errors | Mandatory clause citations, "needs information" option, rules engine, human decision |
| Customer friction | Measure completion time; capture must be as easy as sending a WhatsApp photo |
| Privacy | Regional storage, encryption, short retention, optional blurring |

## 9. Bold alternative: risk scoring for insuring AI agents

Since January 2026, large carriers have added AI exclusions to general liability, D&O and E&O policies, while most large companies deploy AI agents. New specialists (Klaimee, Corgi, HSB AI liability) are trying to fill the gap, but underwriters lack a standard way to measure how risky an agent is. A POC could run a company's agent through test scenarios (wrong actions, data leaks, prompt injection, invented commitments), review its guardrails and logs, and produce an underwriting score. It is very original, but the buyers are fewer and harder to reach. Kept as phase 2.

## 10. Sources

- Debevoise, *Use of AI-generated images for fake insurance claims* (Jan 2026): https://www.debevoise.com/insights/publications/2026/01/use-of-ai-generated-images-for-fake-insurance
- SAS, *Insurers grapple with new fraud threat: AI-generated images* (May 2026): https://www.sas.com/en_us/news/press-releases/2026/may/synthetic-images-ai-insurance-fraud.html
- Qorus, *PhotoDetective* (2026): https://www.qorusglobal.com/innovations/30701-photodetective-detecting-ai-generated-and-internet-sourced-fraud
- CAS, *Deepfakes put insurers in deep water* (2026): https://digital.casact.org/issue/may-june-2026/deepfakes-put-insurers-in-deep-water/
- CoinLaw, *Insurance fraud statistics*: https://coinlaw.io/insurance-fraud-statistics/
- Truepic, *Tamper-evident imagery*: https://www.truepic.com/blog/truepics-technology-provides-authenticity-and-content-verification-via-tamper-evident-imagery
- C2PA specification explainer: https://c2pa.org/specifications/specifications/1.4/explainer/Explainer.html
- Content Authenticity Initiative, C2PA iOS example: https://opensource.contentauthenticity.org/docs/sdk-repos/c2pa-ios-example/
- Analytics Insight, *10 leading AI-powered insurtech companies in 2026*: https://www.analyticsinsight.net/artificial-intelligence/10-leading-ai-powered-insurtech-companies-in-2026
- FinTech Global, *Shift Technology $220m round*: https://fintech.global/?p=57730
- Y Combinator, *Klaimee*: https://www.ycombinator.com/companies/klaimee
- Insurance Business, *Insurers face hidden AI liability*: https://www.insurancebusinessmag.com/us/news/breaking-news/insurers-face-hidden-ai-liability-as-agent-risks-multiply-582433.aspx
- Cloud Security Alliance, *Agentic AI liability insurance gap*: https://labs.cloudsecurityalliance.org/research-rb/csa-research-note-agentic-ai-liability-insurance-gap-2026050/
- ScienceSoft, *Q1 2026 insurance AI trends*: https://www.scnsoft.com/blog/q1-2026
- Gibson Dunn, *EU AI Act Omnibus agreement*: https://www.gibsondunn.com/eu-ai-act-omnibus-agreement-postponed-high-risk-deadlines-and-other-key-changes/
- SOA, *Parametric insurance* (Jan 2026): https://www.soa.org/communities/general-insurance/newsletter-articles/2026/january/2026-01-gi-cappelletti2/
