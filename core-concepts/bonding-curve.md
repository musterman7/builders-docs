# Bonding Curve

## What is a Bonding Curve?

A bonding curve is a mathematical formula that determines the price of a token based on its supply. As more tokens are purchased, the price increases along the curve. As tokens are sold, the price decreases.

## How It Works on Builders.meme

Builders.meme uses a **constant product bonding curve** with the following parameters:

| Parameter | Value |
|-----------|-------|
| Total Supply | 1,000,000,000 |
| Curve Supply | 800,000,000 (available for trading) |
| LP Supply | 200,000,000 (reserved for PancakeSwap) |
| Virtual Token Reserve | 1,080,000,000 |
| Virtual Base Reserve | Graduation Amount × 35% |

### Price Formula

The price at any point is determined by:

```
Price = Virtual_Base / Virtual_Token
```

As tokens are bought, `Virtual_Token` decreases and `Virtual_Base` increases, pushing the price up. The reverse happens when tokens are sold.

### Example

For a token with 6 BNB graduation:
- Virtual BNB = 6 × 0.35 = 2.1 BNB
- Starting price ≈ 2.1 / 1,080,000,000 ≈ 0.00000000194 BNB per token
- As buying occurs, price increases along the curve
- At full curve (800M tokens sold), all 6 BNB is in the reserve

## Bonding Curve Progress

The **progress bar** on each token page shows how much of the curve has been filled:
- 0% — No tokens bought yet
- 50% — Half the curve supply sold
- 100% — Curve is full, token graduates to PancakeSwap
