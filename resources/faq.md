# FAQ

## General

### What is Builders.meme?
Builders.meme is a fair launch token platform on BNB Smart Chain. Anyone can create and trade tokens with bonding curve mechanics and automatic graduation to PancakeSwap.

### Is it free to create a token?
Almost — there's a tiny 0.0001 BNB creation fee (~$0.06) plus gas fees.

### What wallets are supported?
Any wallet that supports WalletConnect or BNB Smart Chain: MetaMask, OKX Wallet, Trust Wallet, Rabby, and more.

## Trading

### What is the trading fee?
1% on every buy and sell transaction on the bonding curve.

### What happens if I buy the last tokens on the curve?
If your purchase would exceed the remaining curve supply, you receive only the remaining tokens and the excess is automatically refunded.

### Can I sell after graduation?
Yes. After graduation, you can sell on PancakeSwap or through any DEX aggregator.

### What is MEV protection?
MEV (Maximal Extractable Value) protection routes your transaction through a private mempool, preventing front-running bots from seeing and exploiting your trade.

## Token Creation

### Can I change my token after creating it?
No. Token contracts are immutable and fully renounced after deployment. Make sure your settings are correct before creating.

### What is the vanity address suffix?
Tokens automatically get a vanity address ending in `0000` (no tax) or `6969` (with tax) for easy identification.

### Why can't I create another token?
There's a 1-minute cooldown between token deployments per wallet to prevent spam.

### What happens to unsold tokens after graduation?
Any remaining tokens in the factory are sent to the dead address (burned).

## Graduation

### When does a token graduate?
When all 800,000,000 tokens on the bonding curve are sold.

### Can graduation fail?
Graduation is designed to be resilient. Even if tax configuration fails, the token still graduates and transfers are unlocked.

### Is the liquidity locked?
Yes — LP tokens are sent to the dead address (`0x000...dead`), making the liquidity permanent and irremovable.

## Earning

### How do I earn referral rewards?
Share your referral link. When someone clicks it and trades, you earn 10% of their trading fees.

### How long do I have to claim cashback?
Cashback doesn't expire. You can claim anytime.

### How long do I have to claim referral rewards?
Referral rewards expire after 30 days if unclaimed. Claim regularly.

### How are airdrop points calculated?
10 points per $1 trading volume, 1 point per token deployed, and graduation bonuses for creators (5,000 points) and top 10 holders (250-1,500 points).
