# Smart Contracts

All Builders.meme contracts are deployed on **BNB Smart Chain (BSC) Mainnet**.

## Core Contracts

| Contract | Address | Verified |
|----------|---------|----------|
| **LaunchFactory** (Proxy) | `0xbb9803474b0F32205457D1c4638207184861dccF` | UUPS Proxy |
| **BuildersMeme** (Token Impl) | `0xE08E57a7333313b0705b53Ab1f43159bBA8E1939` | [BscScan](https://bscscan.com/address/0xE08E57a7333313b0705b53Ab1f43159bBA8E1939#code) |
| **DividendTracker** | `0x34a8D276D72B7639FBDFB3fF6ffb555d84F277Cd` | — |
| **PlatformWallet** | `0xf889421E0Fa1351Ab7E2BdC31661dCB216683702` | — |
| **ReferralVault** | `0xeA784DBA8B2828Ef64A94Be36Be7edcf246386C2` | — |
| **CashbackVault** | `0x3652B390c5e9edDe4Ad580F5d3728884b3d63C5E` | — |

## Architecture

### LaunchFactory
The main contract that handles:
- Token creation (clone pattern using CREATE2)
- Bonding curve trading (buy/sell)
- Graduation to PancakeSwap
- Fee distribution (platform, referral, cashback)
- Referral binding

The factory uses a **UUPS upgradeable proxy** pattern for future improvements.

### BuildersMeme (Token)
Each token is a minimal clone of the BuildersMeme implementation:
- Standard BEP-20 token
- Transfer lock during bonding phase
- Configurable buy/sell tax (active after graduation only)
- Auto-burn, auto-LP, dividend distribution
- Fully renounced — no admin functions

### ReferralVault
Holds referral rewards with multi-token support:
- Supports BNB and all ERC-20 base tokens
- 30-day expiry on unclaimed rewards
- Claimable by referrers anytime

### CashbackVault
Holds cashback rewards with multi-token support:
- Supports BNB and all ERC-20 base tokens
- Claimable by traders anytime

## Token Creation Process

1. Factory creates a **CREATE2 clone** of BuildersMeme
2. Token is initialized with name, symbol, total supply
3. Factory stores token info (creator, graduation amount, etc.)
4. Optional: tax config and dividend tracker are set up
5. Optional: initial buy is executed in the same transaction

## Security Features

- **Balance Invariant Check** — Factory balance must always be ≥ total BNB reserves
- **Reentrancy Guard** — All state-changing functions are protected
- **CEI Pattern** — State changes before external calls
- **Transfer Lock** — Tokens cannot be transferred during bonding
- **Rate Limit** — 1 minute cooldown between token deployments
- **Fee Validation** — Fee shares cannot exceed 100%
- **Slippage Protection** — 1% max slippage on graduation liquidity
