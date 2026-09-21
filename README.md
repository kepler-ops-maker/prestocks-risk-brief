# Pre-IPO Risk Brief

A read-only, explainable risk screen for tokenized pre-IPO exposure on Solana, built for the STOCKLANA 2026 PreStocks bounty.

## Wedge

The PreStocks API exposes token and mark prices, valuations, supply, company metadata, and contract addresses. This app turns those fields into a transparent market-friction brief:

- price dislocation versus published mark price
- supply sensitivity as a limited proxy, explicitly not liquidity depth
- explainable 0-100 score with visible inputs
- honest warnings about data the API does not expose

It never connects a wallet, trades, or makes personalized recommendations.

## Run

```bash
npm install
npm run dev
```

Production build: `npm run build`.

## Data

Live public endpoint: https://prestocks.com/api/prestocks

## Risk model

The score is deterministic and client-side. It weights absolute token/mark price gap, displayed token supply, and implied valuation. It is a screening heuristic, not investment advice. The interface identifies missing order-book depth, redemption terms, and mark methodology rather than fabricating precision.
