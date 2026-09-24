<div align="center">
  <img src="https://raw.githubusercontent.com/UseCert/usecert/main/public/logo.png" alt="UseCert" width="110">

  <h1>UseCert</h1>

  <p><strong>Stock certificates as plain tokens, on Robinhood Chain.</strong></p>

  <p>
    <a href="https://use-cert.com">Site</a> ·
    <a href="https://use-cert.com/roadmap">Milestones</a> ·
    <a href="https://use-cert.com/dashboard">Dashboard</a> ·
    <a href="https://x.com/use_cert">X</a> ·
    <a href="https://t.me/usecertonchain">Telegram</a>
  </p>
</div>

---

A UseCert certificate — `uTSLA`, `uSPY`, `uQQQ`, `uNVDA` — is an ERC-20 you hold like any
other token. It tracks the stock, sits in your wallet, and redeems at oracle price whenever
you want out. No funding tab to watch, no margin to top up, no liquidation price.

Underneath, each certificate is backed by a delta-hedged perpetual position plus margin. The
backing is attested on-chain per batch, and **the age of that proof is published next to it** —
the dashboard says how old the figure is, and says so plainly when it is stale.

### This is a testnet deployment

UseCert runs on Robinhood Chain **testnet** (chain `46630`). Nothing here holds real-world
value, the collateral is a test token from a faucet, and **the perp venue is a simulator this
project runs** — so every margin and position figure describes a simulated position, not a
market.

What is live, what is being built, and what has to be true before mainnet is published at
[use-cert.com/roadmap](https://use-cert.com/roadmap) — without dates, and with a way to check
each claim.

### Three decisions worth knowing

**Redemption is gated on nothing.** Exiting reads no health state and needs no keeper. It is
the one path with no preconditions, deliberately, so a holder can always leave.

**Minting pays for its own freshness.** The attester signs; whoever mints relays that
signature in their own transaction. Nobody funds an empty room.

**The dashboard does not invent data.** Where a series would need an indexer that does not
exist yet, it says so instead of drawing a plausible curve.

### Repositories

**[usecert](https://github.com/UseCert/usecert)** — the front end on `main`, the Solidity
contracts on `backend/contracts-c1`. Two independent histories, one repository. MIT licensed.

<sub>Not affiliated with Robinhood Markets, Inc. Testnet software; no offer of any financial instrument.</sub>
