# Active investigation checks

**Only these 18 original IDs remain active.** They are a small menu of measurements and consequential questions, **not** 18 scores or a compulsory questionnaire. Start with primary outcomes, then select diagnostics or assurance questions only when relevant. Retired and reframed decisions are documented in [ADRs](../../../../docs/adr/README.md).

## Outcome measurements

| ID | Outcome |
|---|---|
| D01 | End-to-end lead time: request enters process → requested capability is available |
| D02 | Deployment frequency: real production deliveries per period |
| D04 | Recovery time: user-impacting failure → useful operation restored |
| D22 | User-facing unavailability: time core service activity was unavailable |

Additional conditional outcomes: first-pass acceptance yield and change-related user disruption, only when naturally defined (see [metrics](metrics.md)).

## Diagnostics (only if informative)

| ID | Measure or targeted question |
|---|---|
| D03 | Change failure rate when linked events exist; otherwise ask about the last failed release |
| D09 | **Non-universal diagnostic:** requirement-to-test linkage when meaningful links exist; otherwise ask how a critical acceptance requirement is verified |
| D14 | **Non-universal diagnostic:** observed flaky tests / slow or misleading test feedback; identify consequential examples |
| D23 | Detection time for user impact when timestamps exist; otherwise ask how degradation is discovered |

D03 and D09 can be **simple in a suitable environment**. Do not downgrade simplicity merely because current records are missing. **D09 and D14 are deliberately retained despite not being universal**; use them only when relevant ([ADR-0017](../../../../docs/adr/0017-retain-non-universal-diagnostics.md)).

## Essential assurance questions

| ID | Question for evidence, **not a numerical performance metric** |
|---|---|
| D07 | Can we trace a deployed release back to a trustworthy artifact and source revision? |
| D08 | Can we safely reverse or mitigate a damaging release, including data changes? |
| D12 | Do actual tests demonstrate detection of important defects, rather than only execute code? |
| D15 | Have service-critical performance, resilience or accessibility risks been demonstrably checked? |
| D17 | Are critical security rules actually enforced, with outstanding high-impact findings handled? |
| D18 | Are material security and privacy threats understood and mitigated? |
| D19 | Are dependencies/provenance controlled and known critical supply-chain risks addressed? |
| D20 | Are privileges, secrets and release approvals sufficiently protected? |
| D25 | If AI is used, are context, permissions and independent verification bounded? |
| D30 | Does monitoring detect meaningful user impact and enable effective response? |

No generic architecture conformance percentage: inspect architecture when evidence indicates delivery delays, failures or control bypasses. No postmortem score: review corrective actions only when significant incidents warrant it. Document material exceptions only when they affect the judgment. Missing information is **unknown**, never a failing score.
