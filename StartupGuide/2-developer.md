# 2. Developer

## Project

- Make sure the Supergraph is created in Apollo GraphQL Studio.
- Make sure Auth and Firestore Region is enabled and a Web Token and Regions is set in the Firebase Project Settings.
- Create 2 Service Accounts:
    - Firebase Admin - use in the backend code to be able to work with Auth and Firestore in Functions.
    - Firebase CICD - use in the pipeline to be able to deploy to Firebase.
- Locally create a new Project folder.
- Update `~/.gitconfig` to set a specific `name` and `email` for `[user]` the local Project folder.
    - Test this by creating a test folder and running `git init` and check `git config user.email`.

## GraphQL

- Create a new Repo in Github Organisation with name `graphql`.
- Clone the 
- Run `npx firebase init`.
    - Choose Auth, Functions and Firestore.
    - Fix Eslint Errors by setting `tsconfigRootDir: __dirname,` in the `.eslintrc.js` file.
- Run `firebase emulators:start` to verify everything is working.
- Run `firebase deploy --only functions` to verify deployment succeeds.
- Inside `functions` folder run `npm install graphql @apollo/server` (make sure its apollo server v4).
- Create an GraphQL endpoint according Apollo documentation and an example project.
- Deploy the GraphQL function and add the endpoint with subgraph to Apollo GraphQL Studio.
    - Bonus: set CORS to only allow the Supergraphq endpoint.

### Seed Data

- Run `firebase emulators:start`.
    - Add a User (authentication) and create a collection Users (firestore).
- Run `firebase emulators:export .seeds`.
- Run `firebase emulators:start --import .seeds (--debug)`.

### Typescript

- See docs: https://www.apollographql.com/docs/apollo-server/workflow/generate-types/
- Move `typeDefs` to a `<root>/schema/schema.graphql` file.)
- Add script `"generate": "graphql-codegen --config codegen.yml"`

### User

- See docs: https://www.apollographql.com/docs/apollo-server/security/authentication

### Github Actions

> TODO: Setup Github Actions

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