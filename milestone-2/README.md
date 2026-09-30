# Milestone 2 — Sell/Buy Order Creation

**Project Catalyst 1400024 — Cardano Bond Exchange: Trading Zero-Coupon Bond (RWA)**
**Milestone 2 — Implement Sell/Buy Order Creation screen**
Milestone page: https://milestones.projectcatalyst.io/projects/1400024/milestones/2

In the app the product is called **Zero Coupon**.

| | |
|---|---|
| Testnet app | https://app.zerocoupon.site |
| Network | Cardano **Preview** |
| Wallet | Eternl |
| Explorer | https://preview.cardanoscan.io |

---

## Acceptance criteria and evidence

| # | Acceptance criterion | Evidence |
|---|---|---|
| 1 | Users can connect a Testnet Eternl wallet to the DEX interface and submit buy/sell orders of Zero-Coupon Bonds successfully. | Screen recordings ([below](#screen-recordings)) and the screenshots of each wallet in [`screenshots/02-wallet-1-addr_test1qq5d0/`](screenshots/02-wallet-1-addr_test1qq5d0/) and [`screenshots/03-wallet-2-addr_test1qz8r8/`](screenshots/03-wallet-2-addr_test1qz8r8/) |
| 2 | At least 10 Sell/Buy orders are successfully created and visible on-chain with transaction hashes viewable in a Cardano Testnet explorer. | [TRANSACTIONS.md](TRANSACTIONS.md): 9 sell orders and 8 buy orders, each with its time, block, amounts and Cardanoscan link, all read from the chain. Each transaction's folder also holds its Eternl record and its Cardanoscan page. |
| 3 | User guide enables any community tester to complete the workflow without developer assistance. | [USER_GUIDE.md](USER_GUIDE.md), with a screenshot for every step, and two public test wallets in [TEST_WALLETS.md](TEST_WALLETS.md). |

---

## Test wallets

| Wallet | Address | In this test |
|---|---|---|
| Wallet 1 | `addr_test1qq5d0puzqsp70uut68m9kj7djwfhq2gy88gxj5g6mke8f7qudwk64wkcpnsyu9mcg2nu3kxkuyspwrh5x5ghj0u94ucsvz7r3n` | creates sell orders, updates and cancels one, buys from wallet 2 |
| Wallet 2 | `addr_test1qz8r8mdqunhr5cl0d0936274upx2qwuhhcnrfurxudxuxlj62s4ndurtq2k8pf8laeqzpgnn9rcgrp8wpae58wnsa3dqgkwfy0` | buys from wallet 1 (a whole order and part of one), creates sell orders, updates and cancels one |

Each wallet created four pools for this test, and each pool minted its PT to that wallet: see the Eternl history of [wallet 1](screenshots/02-wallet-1-addr_test1qq5d0/01-before-any-order/00-eternl-create-pool-transactions.png) and [wallet 2](screenshots/03-wallet-2-addr_test1qz8r8/01-before-any-order/00-eternl-create-pool-transactions.png).

| Token | Wallet 1 | Wallet 2 | Minimum order |
|---|---|---|---|
| ADA | 1,000 | 500 | 90 ADA |
| USDC | 1,000 | 500 | 30 USDC |
| DJED | 1,000 | 500 | 30 DJED |
| SNEK | 100,000 | 50,000 | 37,313 SNEK |

Both wallets are public. Anyone can restore one in Eternl and test with the PT and tokens it already holds: see [TEST_WALLETS.md](TEST_WALLETS.md).

---

## Screen recordings

All recordings, screenshots and transactions in this package were made by our team. Each recording runs from the first click to the confirmed transaction, and the Eternl signing window is visible; recordings are trimmed for length. The file name starts with the transaction's number from [TRANSACTIONS.md](TRANSACTIONS.md).

| Wallet | Recording | What it shows |
|---|---|---|
| Wallet 1 | [`01-S1-sell-PT-ADA.mp4`](videos/wallet-1-addr_test1qq5d0/01-S1-sell-PT-ADA.mp4) | S1: a sell order of 200,000,000 PT ADA at 12%, the pool-minimum check, signing in Eternl, the order on the book and in My Account |
| Wallet 1 | [`02-S2-sell-PT-DJED.mp4`](videos/wallet-1-addr_test1qq5d0/02-S2-sell-PT-DJED.mp4) | S2: connecting Eternl, then a sell order of 50,000,000 PT DJED at 14% |
| Wallet 1 | [`03-S3-sell-PT-USDC.mp4`](videos/wallet-1-addr_test1qq5d0/03-S3-sell-PT-USDC.mp4) | S3: connecting Eternl, then a sell order of 10,000,000,000 PT USDC at 10% |
| Wallet 1 | [`04-S4-sell-PT-SNEK.mp4`](videos/wallet-1-addr_test1qq5d0/04-S4-sell-PT-SNEK.mp4) | S4: connecting Eternl, then a sell order of 40,000 PT SNEK at 10% |
| Wallet 1 | [`05-U1-U2-C1-update-and-cancel-PT-ADA.mp4`](videos/wallet-1-addr_test1qq5d0/05-U1-U2-C1-update-and-cancel-PT-ADA.mp4) | U1, U2, C1: updating the PT ADA order twice (amount and APY, then APY only) and cancelling it |
| Wallet 1 | [`06-S5-sell-PT-ADA.mp4`](videos/wallet-1-addr_test1qq5d0/06-S5-sell-PT-ADA.mp4) | S5: a new sell order of 200,000,000 PT ADA at 12%, for wallet 2 to buy |
| Wallet 2 | [`01-B1-buy-PT-ADA-whole-order.mp4`](videos/wallet-2-addr_test1qz8r8/01-B1-buy-PT-ADA-whole-order.mp4) | B1: buying the whole 200,000,000 PT ADA order S5, matched against one order at 12% |
| Wallet 2 | [`02-B2-buy-PT-USDC-part-of-order.mp4`](videos/wallet-2-addr_test1qz8r8/02-B2-buy-PT-USDC-part-of-order.mp4) | B2: buying 4,000,000,000 of the 10,000,000,000 PT USDC order S3; 6,000,000,000 stay on the book |
| Wallet 2 | [`03-B3-buy-PT-SNEK-whole-order.mp4`](videos/wallet-2-addr_test1qz8r8/03-B3-buy-PT-SNEK-whole-order.mp4) | B3: buying the whole 40,000 PT SNEK order S4 |
| Wallet 2 | [`04-B4-buy-PT-DJED-part-of-order.mp4`](videos/wallet-2-addr_test1qz8r8/04-B4-buy-PT-DJED-part-of-order.mp4) | B4: buying 15,000,000 of the 50,000,000 PT DJED order S2; 35,000,000 stay on the book |
| Wallet 2 | [`05-S6-sell-PT-ADA.mp4`](videos/wallet-2-addr_test1qz8r8/05-S6-sell-PT-ADA.mp4) | S6: reselling the 200,000,000 PT ADA bought in B1, at 14% |
| Wallet 2 | [`06-S7-sell-PT-USDC.mp4`](videos/wallet-2-addr_test1qz8r8/06-S7-sell-PT-USDC.mp4) | S7: a sell order of 10,000,000,000 PT USDC at 14% |
| Wallet 2 | [`07-S8-sell-PT-SNEK.mp4`](videos/wallet-2-addr_test1qz8r8/07-S8-sell-PT-SNEK.mp4) | S8: a sell order of 45,000 PT SNEK at 14% |
| Wallet 2 | [`08-S9-sell-PT-DJED.mp4`](videos/wallet-2-addr_test1qz8r8/08-S9-sell-PT-DJED.mp4) | S9: a sell order of 100,000,000 PT DJED at 14% |
| Wallet 1 | [`07-B5-buy-PT-ADA-whole-order.mp4`](videos/wallet-1-addr_test1qq5d0/07-B5-buy-PT-ADA-whole-order.mp4) | B5: buying the whole 200,000,000 PT ADA order S6 |
| Wallet 1 | [`08-B6-buy-PT-USDC-part-of-order.mp4`](videos/wallet-1-addr_test1qq5d0/08-B6-buy-PT-USDC-part-of-order.mp4) | B6: buying 3,000,000,000 of the 10,000,000,000 PT USDC order S7; 7,000,000,000 stay on the book |
| Wallet 1 | [`09-B7-buy-PT-SNEK-part-of-order.mp4`](videos/wallet-1-addr_test1qq5d0/09-B7-buy-PT-SNEK-part-of-order.mp4) | B7: buying 5,000 of the 45,000 PT SNEK order S8; 40,000 stay on the book |
| Wallet 1 | [`10-B8-buy-PT-DJED-whole-order.mp4`](videos/wallet-1-addr_test1qq5d0/10-B8-buy-PT-DJED-whole-order.mp4) | B8: buying the whole 100,000,000 PT DJED order S9 |
| Wallet 2 | [`09-U3-U4-C2-update-and-cancel-PT-USDC.mp4`](videos/wallet-2-addr_test1qz8r8/09-U3-U4-C2-update-and-cancel-PT-USDC.mp4) | U3, U4, C2: updating the PT USDC order S7 twice (amount and APY, then APY only) and cancelling it |

---

## Contents

```
README.md               this page
USER_GUIDE.md           step-by-step guide, with screenshots
TRANSACTIONS.md         every order, with its Cardanoscan link
TEST_WALLETS.md         the two public test wallets, ready to restore in Eternl
screenshots/
  00-setup-restore-test-wallet-in-eternl/    restoring a test wallet in Eternl
  01-app-overview/                           Market and My Account before connecting, and the Market with both wallets' orders
  02-wallet-1-addr_test1qq5d0/
    01-before-any-order/                     the four pools in Eternl, the Market per token, the sell dialog per PT, My Account
    02-connect-eternl-wallet/                connecting Eternl
    03-create-sell-orders/                   one folder per sell order, e.g. S1-sell-PT-ADA-200M-at-12pct-tx-6a6a404c/
    04-update-and-cancel-sell-orders/        U1-update-…, U2-update-…, C1-cancel-…
    05-buy-orders/                           one folder per buy from wallet 2 (B5–B8)
  03-wallet-2-addr_test1qz8r8/
    01-before-any-order/                     as for wallet 1
    02-buy-orders/                           one folder per buy from wallet 1 (B1–B4)
    03-create-sell-orders/                   one folder per sell order (S6–S9)
    04-update-and-cancel-sell-orders/        U3-update-…, U4-update-…, C2-cancel-…
videos/
  wallet-1-addr_test1qq5d0/                  one recording per action, named after its transactions
  wallet-2-addr_test1qz8r8/

Inside each transaction folder, files are numbered in the order they happened, and named after where the
screenshot comes from: app-… (the Zero Coupon app), eternl-… (the wallet), cardanoscan-… (the explorer).
```

---

## Notes

- **The *Buy order* column shows "—".** In this milestone a buy is filled straight away against the sell orders on the book. The *Buy order* column is part of Milestone 3.
- **Maturity.** On Preview, bonds mature one day after their pool is created, and a year counts as 36.5 hours, so even a one-day bond trades at a clear discount. PT can be listed and bought until maturity; after that it is redeemed for the underlying token.
