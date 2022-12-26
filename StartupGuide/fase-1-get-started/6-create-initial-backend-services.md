# Backend Services

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