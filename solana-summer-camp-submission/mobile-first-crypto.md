---
description: 'PhantomConnect: Enable Native iOS Solana Wallet Functionality'
---

# 🤳 Mobile-First Crypto

Currently there is not a great solution for enabling non-custodial wallet-driven experiences within a native iOS application, but fortunately [we just shipped an open-source solution ](https://github.com/Tokr-Labs/phantom-connect)for this very problem.

At [Rhove](https://rhove.com/) we enable anyone to invest in real estate with as little as $1. We break down barriers. This North Star is why we choose to build on Solana. Solana of course provides low latency, high transaction throughput, and low transaction fees, but more than that these combined qualities coupled with a native iOS experience gave us the unique opportunity to simultaneously engage our crypto-native user base while on-ramping new users to crypto with a near-frictionless experience.

One of the biggest challenges we face as an industry is at the intersection of front-end UX and back-end technological complexity. If we’re all here to on-ramp the next million+ users to crypto, we must meet users where they’re at.

### PhantomConnect <a href="#9fd8" id="9fd8"></a>

When we dug into how we could pull off onboarding new users, we first [integrated Web3Auth into our account creation process](on-ramp.md). This involved spinning up non-custodial Solana wallets for every new user, and doing so using a design pattern they’re used to — authenticating with an email and password. The question then became, how do we enable a frictionless experience for our crypto-native userbase?

The Solana ecosystem has empowered React applications with a robust toolset to interact with Solana, but Rhove is a native iOS application written in Swift. To date, native iOS applications have been left behind with example projects, tutorials, and documentation to allow developers to integrate directly into the Solana ecosystem. So in the spirit of onboarding the next million users, we decided to build the toolset we needed to enable a frictionless crypto-native experience and open-source it to our crypto friends (that’s you!).

Enabling a Phantom wallet connection in our app became a clear starting point for two reasons: first, Phantom is the most ubiquitous non-custodial wallet in Solana and therefore will benefit the most users, and second Phantom just released a series of [deeplinks](https://phantom.app/blog/introducing-phantom-deeplinks) to enable core functionality of their wallet.

### Open Source Repo <a href="#a585" id="a585"></a>

Our team published [PhantomConnect](https://github.com/Tokr-Labs/phantom-connect), an open-source Swift package that abstracts cumbersome logic to implement the following deeplinks into phantom:

* Connecting
* Disconnecting
* Send & Signing Transactions

We’ve included an example project and detailed Readme instructions to make implementation as easy as possible.

To get a sense of what the package can do, here’s the Rhove app connecting to a user’s Phantom wallet and setting an NFT as the user’s PFP.

{% embed url="https://vimeo.com/729389601?" %}

For those with a keen eye, you'll also notice that we enable PFP verification natively in the Rhove app. We built upon the [Solflare PFP service](https://github.com/solflare-wallet/solana-pfp-program) to lay the foundation for additional experiences within the app that we'll dive into next.&#x20;

{% embed url="https://github.com/Tokr-Labs/phantom-connect" %}
Access the repo here
{% endembed %}
