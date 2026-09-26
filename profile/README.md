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
**CERT token** on Robinhood Chain: [`0xb01356A005403C38c0fb01bd0aAfe51e81Ab9B07`](https://robinhoodchain.blockscout.com/token/0xb01356A005403C38c0fb01bd0aAfe51e81Ab9B07)

A UseCert certificate — `uTSLA`, `uSPY`, `uQQQ`, `uNVDA`, `uAAPL`, `uMSFT` — is an ERC-20 you hold like any
other token. It tracks the stock, sits in your wallet, and redeems at oracle price whenever
you want out. No funding tab to watch, no margin to top up, no liquidation price.

Underneath, each certificate is backed by a delta-hedged perpetual position plus margin. The
backing is attested on-chain per batch, and **the age of that proof is published next to it** —
the dashboard says how old the figure is, and says so plainly when it is stale.

### Live on Robinhood Chain mainnet

Six certificates run on Robinhood Chain **mainnet** (chain `4663`), collateralised in **USDG**
and hedged on **Robinhood Chain Lighter**. A mint escrows your USDG, the hedge is opened on the
venue, and certificates are issued only once the venue confirms the fill. Redeeming closes the
hedge on chain, with no key involved.

Governance of every contract is a **2-of-3 Safe multisig**
(`0x848c91323f720DEf985adbCC85FA40E3405B70DF`), and the source of every contract is verified on
[Sourcify](https://sourcify.dev). Certificates are synthetic: no dividends, no shareholder
rights, and they are not available where synthetic equity exposure is restricted.

What is live, what is being built, and what is still open is published at
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

<sub>Not affiliated with Robinhood Markets, Inc. UseCert is infrastructure, not investment advice; nothing here is an offer of any financial instrument.</sub>
