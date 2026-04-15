# Fees

## Fee Structure

### Creation Fee
- **0.0001 BNB** — Flat fee to create a token
- Paid to the platform wallet

### Trading Fee
- **1%** of every buy and sell transaction on the bonding curve
- Split between:

| Recipient | Share | Effective Rate |
|-----------|-------|----------------|
| Platform | 70% | 0.70% |
| Cashback (to trader) | 20% | 0.20% |
| Referral (to referrer) | 10% | 0.10% |

If the trader has no referrer, the referral share goes to the platform.

### Graduation Fee
- **5%** of total raised amount at graduation
- Split between:

| Recipient | Share |
|-----------|-------|
| Token Creator | 4% |
| Platform | 1% |

### Post-Graduation Tax
After graduation, the creator's configured tax applies:
- Buy tax: 0-10%
- Sell tax: 0-10%
- 0.1% of creator's tax goes to the platform

## Non-BNB Pair Fees

For non-BNB pairs (USDT, CAKE, etc.):
- Trading fees are collected in the base token
- Fees are sent directly to vaults without conversion
- Cashback and referral rewards are paid in the base token
