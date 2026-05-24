# TON Tact Jetton Contract

In 2026, the **The Open Network (TON)** ecosystem has experienced unprecedented growth due to its direct integration within Telegram. Unlike the sequential execution model of EVM chains, TON uses a highly asynchronous, actor-model architecture based on shards and messages.

This repository provides a professional-grade reference implementation for a **Jetton** (TON's standard for fungible tokens, equivalent to ERC-20) written in **Tact**, a statically-typed, actor-oriented programming language designed specifically for TON.

## Architecture Highlights
- **Sharding-Native Design:** The master contract acts as the central token coordinator, while individual user wallets are separate child contracts. This design allows infinite horizontal scalability across shards.
- **Asynchronous Messaging:** Employs safe asynchronous message passing with precise gas management and bounce handling to revert state if an operation fails midway.
- **Gas Bounding:** Optimized storage allocation to significantly reduce blockchain storage fees (rent).

## Compile & Deploy
1. Install dependencies: `npm install`
2. Compile the Tact contract code: `npm run build`
3. Execute the deployment script via Blueprint framework: `npm run deploy`

## Technical Details
- **Language:** Tact 1.5.x
- **Token Standard:** TEP-74 (Jetton Standard)
- **Framework:** Blueprint / TypeScript
