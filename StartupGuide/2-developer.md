# 2. Developer

## GraphQL

- Make sure the Supergraph is created in Apollo GraphQL Studio.
- Make sure Auth and Firestore Region is enabled and a Web Token and Regions is set in the Firebase Project Settings.
- Create a new Repo in Github Organisation with name `graphql`.
- Run `npx firebase init`.
    - Enable Auth, Functions and Firestore.
- Run `firebase emulators:start` to verify everything is working.
- Run `firebase deploy --only functions` to verify deployment succeeds.
- Inside `functions` folder run `npm install graphql @apollo/server` (make sure its apollo server v4).
- Create an GraphQL endpoint according Apollo documentation and an example project.
- Deploy the GraphQL function and add the endpoint with subgraph to Apollo GraphQL Studio.

## NextJS


## User Authentication
