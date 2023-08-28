This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `pages/index.js`. The page auto-updates as you edit the file.

[API routes](https://nextjs.org/docs/api-routes/introduction) can be accessed on [http://localhost:3000/api/hello](http://localhost:3000/api/hello). This endpoint can be edited in `pages/api/hello.js`.

The `pages/api` directory is mapped to `/api/*`. Files in this directory are treated as [API routes](https://nextjs.org/docs/api-routes/introduction) instead of React pages.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## Setup Local Environment

You need to setup a few API keys for this project to be setup correctly otherwise you won't see any videos.

- [Magic Server and Publishable Key](https://magic.link/docs)
- [Hasura Admin URL and JWT Secret](https://hasura.io/docs/latest/graphql/cloud/projects/create.html#create-project)
- [Youtube API Key](https://developers.google.com/youtube/v3/getting-started)

For that, you need to create a .env.local file in your project as [shown in docs](https://nextjs.org/docs/basic-features/environment-variables#loading-environment-variables) that will look like this:

```
NEXT_PUBLIC_HASURA_ADMIN_URL=<REPLACE THIS>
JWT_SECRET=<REPLACE THIS>
NEXT_PUBLIC_HASURA_ADMIN_SECRET=<REPLACE THIS>
MAGIC_SERVER_KEY=<REPLACE THIS>
NEXT_PUBLIC_MAGIC_PUBLISHABLE_API_KEY=<REPLACE THIS>
YOUTUBE_API_KEY=<REPLACE THIS>
```

You can retrieve the above environment values by referring their docs linked above and once retrieved, paste above accordingly.

### **_ Important: Videos from Youtube _**

During local development, we recommend you to add the environment variable `DEVELOPMENT=true` as that won't fetch videos from the Youtube API and instead access it from `data/videos.json`. Youtube API does have a [quota](https://developers.google.com/youtube/v3/determine_quota_cost?hl=en) and this way you can continue doing local development without worrying about running out of API calls.

## Packages Used

- @magic-sdk/admin - The Magic Admin SDK lets developers secure endpoints, manage users, and create middlewares via easy-to-use utilities.
- magic-sdk - The Magic JavaScript SDK empowers developers to provide frictionless web3 onboarding to their end-users while preserving their security and privacy using non-custodial wallets.
- classnames - A simple JavaScript utility for conditionally joining classNames together.
- cookie - Basic HTTP cookie parser and serializer for HTTP servers.
- framer-motion - An open source motion library for React, made by Framer.
- jose - jose is JavaScript module for JSON Object Signing and Encryption, providing support for JSON Web Tokens (JWT), JSON Web Signature (JWS), JSON Web Encryption (JWE), JSON Web Key (JWK), JSON Web Key Set (JWKS), and more.
- jsonwebtoken - An implementation of JSON Web Tokens.
- react-modal - Accessible modal dialog component for React.JS

## Work Throughs

- Design and Planning
- Authentication with Magic
- Incremental Static Regeneration
- Hasura GraphQL
- Authentication with Hasura (JWT)
- Rating and My List Pages (Services)
