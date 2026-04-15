# How It Works

Builders.meme uses a **bonding curve** model for fair token launches on BNB Smart Chain.

## The Lifecycle of a Token

### 1. Creation
Anyone can create a token by providing a name, symbol, description, and image. Optionally, creators can configure tax settings (buy/sell tax, burn, dividends, LP).

### 2. Bonding Phase
After creation, the token enters the **bonding phase**. During this phase:
- Users buy and sell tokens directly through the bonding curve
- Price increases as more tokens are bought
- Price decreases as tokens are sold
- There is a 1% trading fee on all transactions
- Token transfers are locked (only buy/sell through the platform)

### 3. Graduation
When the bonding curve is completely filled (all 800,000,000 tokens sold), the token **graduates**:
- Liquidity is automatically deposited to PancakeSwap
- LP tokens are sent to the dead address (burned forever)
- Token transfers are unlocked
- Tax settings activate (if configured by creator)
- The token is now freely tradeable on PancakeSwap

### 4. Post-Graduation
After graduation, the token behaves like any normal BEP-20 token on PancakeSwap with the creator's tax settings applied.

## Key Numbers

| Parameter | Value |
|-----------|-------|
| Total Supply | 1,000,000,000 tokens |
| Bonding Curve Supply | 800,000,000 tokens (80%) |
| PancakeSwap LP Supply | 200,000,000 tokens (20%) |
| Trading Fee | 1% |
| Graduation Fee | 5% (4% creator, 1% platform) |
| Create Fee | 0.0001 BNB |
