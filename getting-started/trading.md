# Trading

## Buying Tokens

### On the Bonding Curve
1. Go to the token's detail page
2. Enter the amount of BNB (or other base token) to spend
3. Click **Buy**
4. Confirm the transaction

Quick buy buttons (0.1, 0.5, 1 BNB) are available for convenience.

### Slippage Protection
All trades have a default **15% slippage tolerance**. This protects you from front-running and sandwich attacks. You can adjust this in the slippage settings (gear icon).

### MEV Protection
Toggle **MEV Protection** to route your transaction through a private mempool, preventing front-running bots from extracting value from your trade.

## Selling Tokens

### On the Bonding Curve (Before Graduation)
1. Go to the token's detail page
2. Switch to the **Sell** tab
3. Enter the amount of tokens to sell (use 25%, 50%, 100% buttons)
4. Click **Sell**
5. First time selling: approve token spending, then the sell executes automatically

### On PancakeSwap (After Graduation)
After a token graduates, you can sell on PancakeSwap or any DEX aggregator.

## Price Mechanics

The bonding curve uses a **constant product formula**:
- Price starts low and increases as more tokens are bought
- Selling tokens decreases the price
- The curve guarantees there's always liquidity available

## Reading the Chart

The trading chart shows:
- **Candlestick** — Open, High, Low, Close prices per time interval
- **Volume bars** — Trading volume per candle
- **Timeframes** — 1m, 5m, 15m, 1h, 4h, 1D
- **Scale modes** — Auto, Logarithmic (log), Percentage (%)
