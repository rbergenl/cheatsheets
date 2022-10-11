# Format

## Setup: Prettier

- Run `npm install --save husky lint-staged prettier`.
- Add to `package.json` (taken from [here](https://create-react-app.dev/docs/setting-up-your-editor/#formatting-code-automatically)).
```json
"scripts": {
  "format": "prettier --write \"src/**/*.{js,jsx,ts,tsx,json,css,scss,md}\""
},
"husky": {
  "hooks": {
    "pre-commit": "lint-staged"
  }
},
"lint-staged": {
  "src/**/*.{js,jsx,ts,tsx,json,css,scss,md}": [
    "prettier --write"
  ]
}
```
- Replace the `src` with `{folder1,folder2}`.
- Create a `.prettierrc` file with the config (taken from [here](https://prettier.io/docs/en/configuration.html)):
```json
{
    "trailingComma": "es5",
    "tabWidth": 4,
    "semi": false,
    "singleQuote": true,
    "printWidth": 120
}
```
- First time, run `npm run format`.
- Read the `CONTRIBUTING.md` file for more information.

## Optional extras

- Use setup as explained here: https://create-react-app.dev/docs/setting-up-your-editor/
- Run `touch .editorconfig` (see editor configuration https://editorconfig.org).
