# Tokenomics & Tax

## Tax System

Creators can configure a tax on buy and sell transactions. Tax is **only active after graduation** — during the bonding phase, no tax is applied.

### Tax Configuration

- **Buy Tax Rate** — 0% to 10% on purchases
- **Sell Tax Rate** — 0% to 10% on sales

### Tax Allocation

The collected tax is distributed according to the creator's configuration:

| Allocation | Description |
|------------|-------------|
| **Funds Wallet** | Sent to the creator's designated wallet(s) for marketing, development, etc. |
| **Burn** | Tokens are permanently burned, reducing total supply (deflationary) |
| **Liquidity** | Tax is used to add more liquidity to the PancakeSwap pair |
| **Dividend** | Tax is distributed proportionally to all token holders above the minimum balance |

The total allocation must equal 100%.

### Multi-Wallet Tax Split

Creators can split the funds wallet portion among up to 5 different wallets using the TaxSplitter contract. This enables automatic revenue sharing between team members.

### Dividend Tracker

If dividends are enabled, a DividendTracker contract is automatically deployed. Holders above the minimum balance threshold receive proportional rewards from the tax.

## Token Properties

All tokens created on Builders.meme share these properties:

- **Fully Renounced** — Token ownership is renounced after deployment
- **Immutable** — Token code cannot be changed
- **Transfer Lock** — Transfers locked during bonding, unlocked at graduation
- **No Mint Function** — Total supply is fixed at creation
- **Verified Source** — BuildersMeme contract is verified on BscScan
