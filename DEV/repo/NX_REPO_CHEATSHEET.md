# NX Repo


# Getting Started
```bash
nvm install --lts && nvm alias default node
npx create-nx-workspace@latest # choose type "apps"
cd <projectname>
echo $(node -v) > .nvmrc # and git commit
# npm install -D @nrwl/react
# nx generate @nrwl/react:app myapp # choose styled-components and react-router "yes" > it install prettier eslint jest and cypress
```

<br />

# Quality Assurance

- [Format Pre-commit Hook](../quality/hook_format.md)
- [Lint Pre-commit Hook](../quality//hook_lint.md)
- [Security Analysis](../quality/analyse_security.md)
- [Performance Analysis](../quality/analyse_performance.md)
- [Static Analysis](../quality/analyse_static.md)
- [Unit Test](../quality/test_unit.md)
- [Integration Test](../quality/test_integration.md)
- [E2E Test](../quality/test_e2e.md)
- [Smoke Test](../quality/test_smoke.md)
