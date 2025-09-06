# Contributing

Before you start, read `.cursorrules`. It defines:
* **Architecture**: Clean Architecture boundaries; DTO/contracts at all edges.
* **Guardrails (non-optional)**: Accessibility, i18n, API ergonomics, Data/Privacy,
  Tooling/DX, AI/Agent Safety (if used), Governance/ADRs.

## Workflow
1. Branch from `master`: `git checkout -b agent/<area>-<short-desc>`
2. Keep PRs small; prefer incremental patches.
3. Fill the PR template completely (all checklist items must be ✅).
4. Ensure CI is green (typecheck, lint, tests, contract/codegen if applicable).

## Commit & PR conventions
- Use **Conventional Commits**: `feat:`, `fix:`, `docs:`, `refactor:`, `test:`, `chore:`, `ci:`.
- Link issues/ADRs in PR description.

## Testing
- Pyramid: unit → contract/integration → e2e (only where needed).
- Mock only at Port boundaries. Don’t mock within domain logic.

## Accessibility & i18n (if UI)
- WCAG AA (axe/Lighthouse) must pass in CI for touched views/components.
- No hard-coded user-facing strings; externalize; UTC internally.

## Public APIs
- Update contracts (OpenAPI/Schema/IDL) **first**; regenerate SDKs/clients.
- Document breaking changes with migration notes.

