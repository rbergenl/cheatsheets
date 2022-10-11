# Security Analysis

## Setup: NPM Audit

- Run `npm install --save-dev npm-audit-resolver@next`.
- Add to `package.json`
```json
"scripts": {
  "audit": "check-audit --production",
  "audit:resolve": "resolve-audit",
}
```

## Setup: OWASP Dependency Check

- T.b.c.
