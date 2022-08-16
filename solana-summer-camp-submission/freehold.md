---
description: Solana NFTs made easy
---

# 🎊 Freehold

### 🔮 Overview

Freehold is an NFT service that aims to make the creation and exploration of NFTs on the Solana blockchain as easy as possible. While existing solutions predominantly focus on catering to generative art projects, Freehold is focused on unlocking the utility of NFTs.

Current features include:

* A simple UI for creating NFTs with custom metadata
* Automatic collection verification
* Easily find owned and created NFTs
* Token-gated experience facilitation
* An easy-to-use API that enables automated edition printing

As an example of the last bullet point above, [Rhove](https://rhove.com/) utilizes Freehold's API to reward investors on its platform with an editioned NFT commemorating their investment. A separate party could then also utilize Freehold's API to filter a user's owned NFTs to just those matching the Rhove collection and provide additional utility if there's a match.

There are big plans in store for Freehold's future. View our [Roadmap](https://github.com/Tokr-Labs/freehold#-roadmap) section to learn more.

### 🧑‍💻 Running Locally

In order to run this repository locally, you must first copy the contents of `.env.sample` to `.env.local`. The only required environment variables are `NEXT_PUBLIC_RPC_DEVNET` and `NEXT_PUBLIC_RPC_MAINNET_BETA` which have the publicly available RPC nodes from the Solana Foundation included by default.

If you wish to utilize the built-in API, the `SOLANA_PRIVATE_KEY` variable will also need set. To prevent unauthorized access to the endpoints that interact with that private key, basic auth credentials can be set via the `BASIC_AUTH_USER` and `BASIC_AUTH_PASSWORD` variables.

Once `.env.local` is set up, simply start the local server with:

```
next dev
```

You should see your environment variables being loaded as well as confirmation that the server is now running on `http://localhost:3000`.

```
ready - started server on 0.0.0.0:3000, url: http://localhost:3000
info  - Loaded env from [...]/freehold/.env.local
wait  - compiling...
event - compiled client and server successfully in 1770 ms (1813 modules)
```

### 📑 Repository Structure

Top-level directories:

```
├── components/      # Reusable React components
├── contexts/        # Custom React contexts
├── pages/           # File-based page routing, see next.js docs for more info
│    └── api/        # File-based API endpoints, see next.js docs for more info
├── public/          # Publicly available files such as images and logos
├── styles/          # Theming related files (light mode, dark mode, and global)
└── utils/           # Utility functions for the API
```

Notes and resources:

* Next.js file-based [page routing](https://nextjs.org/docs/basic-features/pages) and [API endpoints](https://nextjs.org/docs/api-routes/introduction)
* Filenames beginning with an underscore within the `pages/` directory are excluded from showing up as a page or API endpoint
* The `utils/` directory includes functions that are able to be used within the API endpoint files (which cannot utilize contexts or hooks as they are not React components)

### 🦾 Tech Stack

| **Library**     | **Repository link**                                                         | **Description**                  |
| --------------- | --------------------------------------------------------------------------- | -------------------------------- |
| **Next.js**     | [vercel/next.js](https://github.com/vercel/next.js)                         | React framework                  |
| **NextUI**      | [nextui-org/nextui](https://github.com/nextui-org/nextui)                   | UI component library and theming |
| **React Icons** | [react-icons/react-icons](https://github.com/react-icons/react-icons)       | Iconography                      |
| **Metaplex**    | [metaplex-foundation/js](https://github.com/metaplex-foundation/js)         | NFT SDK                          |
| **Solflare**    | [solflare-wallet/solana-pfp](https://github.com/solflare-wallet/solana-pfp) | PFP program and SDK              |
| **Solana Labs** | [solana-lab/wallet-adapter](https://github.com/solana-labs/wallet-adapter)  | Walllet Adapter                  |
| **Vercel**      | [vercel](https://github.com/vercel)                                         | Hosting and deployments          |

### 🚀 Roadmap

Here's a sneak peek of what we plan to grow Freehold into:

* [ ] &#x20;Ability to create collection NFTs that adhere to the new standard introduced in Metaplex v1.3
* [ ] &#x20;Usable NFTs for communities that wish to create their own utility
* [ ] &#x20;Collection analysis tools (e.g., metadata insight, distribution, transfer tracking, etc.)
* [ ] &#x20;Bulk action tool (e.g., printing many editions at once, burning junk NFTs to recover SOL, etc.)
* [ ] &#x20;On-chain programs to facilitate more advanced functionality

Have an idea that isn't listed here? We'd love to hear about it! Please create a post in the discussion board.

{% embed url="https://github.com/Tokr-Labs/freehold" %}
