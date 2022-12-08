# Dev

## Quality Assurance

- [Format Pre-commit Hook](../quality/hook_format.md)
- [Lint Pre-commit Hook](../quality//hook_lint.md)
- [Security Analysis](../quality/analyse_security.md)
- [Performance Analysis](../quality/analyse_performance.md)
- [Code Analysis](../quality/analyse_code.md)
- [Unit Test](../quality/test_unit.md)
- [Integration Test](../quality/test_integration.md)
- [E2E Test](../quality/test_e2e.md)
- [Smoke Test](../quality/test_smoke.md)


## CiCd Checklist

- [ ] Build (run > publish artifact)
- [ ] Test: Unit Test (run > publish report > publish coverage report)
- [ ] Test: Integration Test (run > publish report)
- [ ] Test: E2E Test (run > publish report)
- [ ] Deploy: Tst (run > verify)
- [ ] Deploy: Acc (run > verify)
- [ ] Deploy: Prd (run > verify > publish release)
- [ ] Analyse: Security Audit (run > publish report)
- [ ] Analyse: Performance Audit (run > publish report)
- [ ] Analyse: Unit Test (run > publish report > publish coverage report)
- [ ] Analyse: Code Audit (run > publish report)

## Format Pre-commit Hook

- Setup instructions: `
- Manual run: `npm run format`
- Automatic run: before finilizing the command `git commit`

## Lint Pre-commit Hook

- Manual run: `npm run lint`
- Automatic run: before finilizing the command `git commit`

## Security Audit

- Manual run: `npm run security`
- Automatic run: scheduled in the pipeline for the main branch
- Report: available in the last pipeline run scheduled for the main branch

## Performance Audit

- Manual run: `npm run performance`
- Automatic run: scheduled in the pipeline for the main branch
- Report: available in the last pipeline run scheduled for the main branch

## Static Analysis

- Manual run: `npm run static`
- Automatic run: scheduled in the pipeline for the main branch
- Report: available in the last pipeline run scheduled for the main branch

## Unit Tests

- Manual run: `npm run test`
- Automatic run: on each `git push` in the pipeline
- Report: available in the pipeline run for each branch
- Coverage Report: available in the last pipeline run scheduled for the main branch

## Integration Tests

- Manual run: `npm run integration`
- Automatic run: on each `git push` in the pipeline
- Report: available in the pipeline run for each branch

## Functional E2E Tests

- Manual run: `npm run e2e`
- Automatic run: on each `git push` in the pipeline
- Report: available in the pipeline run for each branch

>>>>>>>>>>>>>> - Visual Report: ??

## Smoke Tests

- Manual run: `npm run smoke`
- Automatic run: on each `git push` in the pipeline
- Report: available in the pipeline run for each branch

>>>>> ## Release

- Deploy
- Verify
- Notify
- Version
