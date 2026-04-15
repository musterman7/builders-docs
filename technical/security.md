# Security

## Smart Contract Security

### Audit Status
The LaunchFactory V3 contract has undergone internal security review with the following findings addressed:

- **Balance Invariant** — Factory balance is checked against reserves after every BNB trade
- **Reentrancy Protection** — Custom reentrancy guard on all state-changing functions
- **CEI Pattern** — Checks-Effects-Interactions pattern enforced on buy/sell
- **Transfer Lock** — Tokens cannot be transferred during bonding phase
- **Fee Validation** — Fee share setters validate total ≤ 100%
- **Graduation Slippage** — Max 1% slippage when adding PancakeSwap liquidity
- **Emergency Functions** — Owner can withdraw excess BNB (above reserves only) and rescue stuck tokens
- **Rate Limiting** — 1 minute cooldown between token deployments per wallet

### What Makes It Safe

1. **No Rug Pull** — LP tokens are burned at graduation. Liquidity is permanent.
2. **No Mint Function** — Total supply is fixed. No new tokens can be created.
3. **Renounced Tokens** — Token contracts have no admin/owner functions.
4. **Transfer Lock** — During bonding, tokens can only be traded through the factory.
5. **On-Chain Reserves** — All bonding curve reserves are held in the factory contract, verifiable on-chain.

### Known Limitations

- Balance invariant only covers BNB-based token reserves. Non-BNB token reserves rely on ERC-20 balance tracking.
- Emergency withdraw is limited to excess BNB above reserves. Full rescue requires the contract to be paused.

## User Safety Tips

- Always verify the token contract address on BscScan
- Check the bonding curve progress before buying
- Use slippage protection (default 15%)
- Enable MEV protection for large trades
- Never share your private keys or seed phrase
