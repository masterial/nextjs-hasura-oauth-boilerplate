## Features

This boilerplate is built on top of [Next.js](http://nextjs.org/) and [Hasura](https://hasura.io/). So, you get all the benefits and features that these two softwares provide. However, the following features are the most important ones:

1. **Automatic compilation and bundling** of Next.js which ensures optimized code during production builds.
2. **Pre-rendering of pages** at build time (SSG) or request time (SSR).
3. Support for **TypeScript**.
4. **File-system routing** which helps in adding new routes to your application.
5. Support for **optimized images** out of the box.
6. Instant **real-time** GraphQL APIs.
7. Built-in **authorization** and **authentication**.

## Overview

This boilerplate is built using the following technologies:

- [Chakra UI](https://chakra-ui.com/)
- [Emotion](https://emotion.sh/)
- [GraphQL](https://graphql.org/)
- [Apollo](https://www.apollographql.com/)
- [NextAuth](https://next-auth.js.org/)
- [TypeScript](https://www.typescriptlang.org/)

It supports GraphQL Query, Mutation and Subscription out of the box.

## Requirements

- [Node.js - ^12.19.0 || ^14.15.0 || ^16.13.0](https://nodejs.org/)
- [npm](https://www.npmjs.com/)
- [Docker](https://www.docker.com/)

## Packages

- [**Frontend**](/frontend): Next.js application

This application is the primary user-facing application. Once it’s up and running (see Development section), it’s available on [http://localhost:3000](http://localhost:3000/).

- [**Backend**](/backend): Dockerized Hasura application

[Hasura](https://hasura.io/) is an open source engine that connects to our databases & micro-services and auto-generates a production-ready GraphQL backend. It’s very easy to get Hasura up and running on our local system. All the migrations are set up in the [migrations](/backend/migrations) directory.

## Installation

1. Run the bootstrap script by running the following command from the root of your project:

   ```bash
   cd nextjs-hasura-boilerplate && yarn bootstrap
   ```

2. Create a Google OAuth Client from https://console.developers.google.com/apis/credentials/oauthclient and copy the credentials to `GOOGLE_CLIENT_ID` and `GOOGLE_CLIENT_SECRET` in your `.env` file inside the `frontend` directory.

3. Start Docker and run both the applications by running the following command from the root of your project:

   ```bash
   yarn dev
   ```

We need to start Docker and then run the above command. The Hasura console will be available at [http://localhost:8080/console](http://localhost:8080/console). The Hasura GraphQL endpoint will be up and running on [http://localhost:8080/v1/graphql](http://localhost:8080/v1/graphql). The Next.js application will be available at [http://localhost:3000/](http://localhost:3000/).

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).
