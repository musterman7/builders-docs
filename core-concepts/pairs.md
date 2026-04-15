# Supported Pairs

Builders.meme supports creating tokens paired with 7 different base tokens on BNB Smart Chain.

## Available Pairs

| Token | Contract | Decimals |
|-------|----------|----------|
| BNB | Native (0x0000...0000) | 18 |
| USDT | 0x55d398326f99059fF775485246999027B3197955 | 18 |
| USDC | 0x8AC76a51cc950d9822D68b83fE1Ad97B32Cd580d | 18 |
| USD1 | 0x8d0D000Ee44948FC98c9B98A4FA4921476f08B0d | 18 |
| U | 0xcE24439F2D9C6a2289F741120FE202248B666666 | 18 |
| CAKE | 0x0E09FaBB73Bd3Ade0a17ECC321fD13a19e81cE82 | 18 |
| FIST | 0xC9882dEF23bc42D53895b8361D0b1EDC7570Bc6A | 6 |

## Choosing a Pair

- **BNB** — Most popular, highest liquidity on BSC
- **USDT/USDC/USD1/U** — Stablecoin pairs, price not affected by BNB volatility
- **CAKE** — PancakeSwap ecosystem token
- **FIST** — Community token (note: 6 decimals)

## How Non-BNB Pairs Work

For non-BNB pairs:
1. Creator selects the base token when creating
2. Buyers need the base token in their wallet to purchase
3. At graduation, liquidity is added as TOKEN/BASE_TOKEN pair on PancakeSwap
4. Trading fees and referral rewards are paid in the base token (not converted to BNB)
