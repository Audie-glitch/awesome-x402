# Awesome x402

A curated list of **HTTP 402** / **x402** resources for agent-native pay-per-request rails — especially **Base USDC**.

This is an original list. Descriptions are short and written here; links point at the projects themselves. PRs welcome if you keep blurbs brief and honest.

## Protocol & docs

- [x402.org](https://www.x402.org/) — Home of the open HTTP-native payment standard for agents and APIs.
- [x402 docs (quickstart for sellers)](https://docs.x402.org/getting-started/quickstart-for-sellers) — Add middleware, return `402 Payment Required`, settle with stablecoins.
- [Linux Foundation x402 Foundation announcement](https://x402.org/linux-foundation-announces-operational-launch-of-x402-foundation-to-standardize-internet-native-payments-for-ai-agents-and-applications/) — Neutral home for the standard.

## Facilitators

Facilitators help clients settle the payment named in a `402` response.

- [PayAI facilitator](https://facilitator.payai.network/) — Public facilitator used by many Base USDC sellers and discovery crawls.
- [Coinbase Developer Platform (x402)](https://docs.cdp.coinbase.com/) — CDP docs and tooling around x402 (account required for some flows).

## Discovery & indexes

- [x402scan](https://www.x402scan.com/) — Indexes live `402` origins and resources.
- [Agent402](https://agent402.tools/) — Agent tool router / index over paid endpoints (eligibility often gated on settlement history).
- [PayAI discovery / Bazaar](https://payai.network/) — Catalog surface that crawls facilitator traffic (metadata can lag a live `402`).

## Live SKUs (operated here)

Mute HTTP sellers on Base USDC. Expect `HTTP 402` with a `PAYMENT-REQUIRED` challenge when unpaid. Free-plan Workers hosts can return `429` near daily quota.

- [Clear-to-Send shop](https://premiumrewards.vip/) — Landing for the live worker shop.
- [`GET /fx` Spot FX](https://api.premiumrewards.vip/fx?from=USD&to=EUR&amount=100) — ~$0.01 USDC on Base. ECB-spot-style FX check.
- [Pulse pre-spend check](https://pulse.premiumrewards.vip/check) — ~$0.005 USDC on Base. Tiny probe before a larger spend.

x402scan origin (shop): `441bad1b-0ed0-4de6-a552-7f8234d2e501`  
Pulse origin: `34f12126` (confirm on x402scan if the short id rotates).

## Agent job boards (wallet / USDC, read the fine print)

Not all “agent” boards pay on-chain or skip KYC. Caveats matter.

- [TaskMarket / Daydreams](https://taskmarket.daydreams.systems/) — On-chain task market; wallet identity; check escrow and legal-bundle status per task.
- [Superteam Earn](https://earn.superteam.fun/) — Mixed board: some agent listings; many human listings need KYC / human claim for payout.
- Agent Hansa / similar no-KYC regs — Prefer boards that pay a wallet you control; skip stake/OAuth/KYC gates.

## Tooling

- Hono / Worker middleware patterns — Pair a Cloudflare Worker (or Node) with x402 payment middleware; keep SKUs mute and machine-shaped.
- Stablecoin on Base — USDC contract commonly used by sellers: `0x833589fCD6eDb6E08f4c7C32D4f71b54bdA02913`.

## Contributing

1. Open a PR with one link + a 1–2 sentence blurb you wrote.
2. Prefer live URLs that actually return `402` or clear docs.
3. No star-farming, paid starring, or scraped dumps of other awesome lists.

## License

List text in this repo is [CC0 1.0](./LICENSE) (public domain dedication). Linked projects keep their own licenses.
