## Summary
_What & why. One or two sentences. Link to issue/ADR if relevant._

## Architecture touchpoints
- **Layer boundaries:** Domain ⟷ Application ⟷ Interfaces ⟷ Infra unchanged? If changed, explain.
- **Ports/Adapters:** New or modified ports/adapters? Note DTOs and mappers.
- **Data model/contracts:** Any schema/IDL change? Versioning strategy?

## Risk & rollout
- Risk level: Low / Medium / High
- Rollout plan / behind flag? Rollback steps?

## Tests & evidence
- Unit: …
- Integration/contract: …
- Accessibility/i18n checks (if UI): …
- Screenshots/logs/traces (if helpful): …

## Checklist (must tick all)
- [ ] I read `.cursorrules` and this change **conforms** to Clean Architecture, DTO/contracts, and **non-optional guardrails** (Accessibility, i18n, API ergonomics, Data/Privacy, Tooling/DX, AI/Agent Safety when used, Governance/ADRs).
- [ ] Tests cover new/changed behavior; no flaky sleeps; deterministic.
- [ ] No secrets/PII in code/logs; sensitive data masked; least-privilege access.
- [ ] (If public API changed) Contracts & SDKs regenerated; docs/changelog updated; deprecations noted.
- [ ] (If infra/pipeline changed) IaC updated; drift checked; env vars documented.

## Docs
Link ADR(s), runbook, and any updated docs.

