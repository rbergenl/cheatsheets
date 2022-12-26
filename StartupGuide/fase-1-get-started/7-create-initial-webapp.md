# NX Monorepo

## NX React

- Make sure to have the VSCode Extensions installed (https://www.apollographql.com/docs/devtools/editor-plugins/)
- Create a new Repo in Github Organisation with name `webapps`.
- Run `npx create-nx-workspace@latest --preset=apps` call it `webapps`.
- Inside the folder run `git remote add origin <url>`. And then `git branch -M main` and `git push -u origin main`.
- Run `npm install -D @nrwl/react` and then `npx nx g @nrwl/react:app <name>`. (see docs: https://nx.dev/packages/react).
    - Choose `styled-components` and `React Router`.
- Run `npx firebase init`.
    - Choose Hosting.
    - Set the public path to `dist/apps/<name>`.
- Run `firebase deploy --only hosting`.
- Creat the following libraries with the command `nx g @nrwl/react:library <name>`: util-testing, util-analytics, util-auth, ui-components, data-access-graphql and feature-something.

### Data-Access-GraphQL
- Run `npm install @apollo/client graphql`. And continue with steps described here: https://www.apollographql.com/docs/react/get-started
    - Make sure to set correct CORS settings in Apollo GraphQL Studio. (add `http://localhost:4200` to the `origins` list)
- Typescript Codegen. See docs: https://www.apollographql.com/docs/react/development-testing/static-typing

## Github Actions
- See docs: https://firebase.google.com/docs/hosting/github-integration
- Run `firebase init hosting:github`.

## User

- Run `npm install firebase`.
- Add:
```typescript
import {initializeApp} from "firebase/app"
import {getAuth} from "firebase/auth";
initializeApp(firebaseConfig);
const auth = getAuth();
```

# Libs UI: Components

# Libs Data-Access: GraphQL

# Libs Feature: Accounts

# Libs Feature: Products

# Libs Util: Analytics

# Libs Util: Testing
- FakeSate
- Mocks
