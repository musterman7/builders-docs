# Graduation

## What is Graduation?

Graduation is the moment when a token transitions from the bonding curve to PancakeSwap. This happens automatically when all 800,000,000 tokens on the curve are sold.

## What Happens During Graduation

1. **Liquidity Deposit** — All raised funds (minus graduation fee) plus 200,000,000 reserved tokens are deposited as liquidity on PancakeSwap V2.
2. **LP Burned** — The LP tokens are sent to the dead address (`0x000...dead`), making the liquidity permanent and unruggable.
3. **Transfers Unlocked** — Token transfers are enabled. Before graduation, tokens can only be bought/sold through the bonding curve.
4. **Tax Activated** — If the creator configured buy/sell tax, it becomes active after graduation.
5. **Graduation Fee** — A 5% fee is deducted from the raised funds:
   - 4% goes to the token creator
   - 1% goes to the platform

## Graduation Tiers

Each base token has multiple graduation tiers, determining how much needs to be raised:

| Tier | BNB | USDT/USDC/USD1/U | CAKE | FIST |
|------|-----|-------------------|------|------|
| Test | 0.032 | 20 | 8 | 20 |
| Tier 1 | 6 | 4,000 | 3,000 | 8,000 |
| Tier 2 | 10 | 8,000 | 6,000 | 16,000 |
| Tier 3 | 18 | 12,000 | 10,000 | 24,000 |

Higher tiers mean more liquidity in the PancakeSwap pool after graduation.

## Slippage Protection

Graduation uses a maximum 1% slippage when adding liquidity to PancakeSwap, ensuring fair pricing.
