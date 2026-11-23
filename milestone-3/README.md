# Milestone 3 — Bond DEX and price matching

**Project Catalyst 1400024 — Cardano Bond Exchange: Trading Zero-Coupon Bond (RWA)**
**Milestone 3 — Implement Bond Dex and Price matching**
Milestone page: https://milestones.projectcatalyst.io/projects/1400024/milestones/3

In the app the product is called **Zero Coupon**.

| | |
|---|---|
| Testnet app | https://app.zerocoupon.site |
| Network | Cardano **Preview** |
| Wallet | Eternl |
| Explorer | https://preview.cardanoscan.io |
| Smart contracts (GitHub) | https://github.com/haiphan1309/zero-coupon-aiken-contracts |

---

## Milestone outputs

| # | Output | Where |
|---|---|---|
| 1 | Testnet DEX page showing active open orders (order book). | The Market: [order book](screenshots/09-order-book-display/) and [order book after each phase](screenshots/15-order-book-snapshots/) |
| 2 | Price-matching functionality allowing trades to be executed. | [Buys](screenshots/07-buy-market-orders/) and [sells to bids](screenshots/08-sell-to-bids-market-orders/), explained in [MATCHING.md](MATCHING.md) |
| 3 | Trade history component showing executed trades with timestamps and maturity data. | [Trade history](screenshots/11-trade-history/): the trades of the connected wallet, each with its time; the trades of this test also show the maturity (date and hour) of their pool, see [HIST-05](screenshots/11-trade-history/HIST-05-W1-W2-time-and-maturity-of-each-fill) |
| 4 | Public user guide for matching and trade history. | [USER_GUIDE.md](USER_GUIDE.md): sections 9 (matching) and 10 (trade history) |

## Acceptance criteria and evidence

| # | Acceptance criterion | Evidence |
|---|---|---|
| 1 | Users can view all active orders and execute matching trades on Cardano Testnet. | Screen recordings ([below](#screen-recordings)) of the order book and of every trade in the test cases, from the first click to the confirmed transaction, and the screenshots in [`screenshots/`](screenshots/). |
| 2 | At least 10 successful trades executed and verified on-chain (with transaction hashes). | [TRANSACTIONS.md](TRANSACTIONS.md): 19 trades in the test cases (11 buys and 8 sells to bids), each with its time, block, amounts and Cardanoscan link, all read from the chain. The test wallets made two more buys, listed under [Other transactions](TRANSACTIONS.md#other-transactions-of-the-test-wallets): 21 trades in all. |
| 3 | Trade history updates automatically based on on-chain data. | The history page lists the trades of the connected wallet, on both books, and shows a new trade without a reload. The page reads the trades from on-chain data again every 30 seconds while it is open, with no reload or click. In [recording HIST-08](videos/11-trade-history/HIST-08-W1-history-updates-by-itself.mp4) wallet 1 keeps its History page open while it sells to a bid in another tab; when the History tab is shown again, the new row appears within the next refresh (about 30 seconds) and the count goes from 12 to 13 trades ([screenshots](screenshots/11-trade-history/HIST-08-W1-history-updates-by-itself-tx-241211ad)). The screenshots before and after a trade ([HIST-09](screenshots/11-trade-history/HIST-09-W1-history-before-and-after-one-trade)) show the difference. Every row comes from the chain and links to its transaction on Cardanoscan. |
| 4 | Public user guide enables community testers to replicate actions without developer support. | [USER_GUIDE.md](USER_GUIDE.md), with screenshots of the screens and dialogs it uses, and two public test wallets in [TEST_WALLETS.md](TEST_WALLETS.md). |

---

## Test wallets

| Wallet | Address | In this test |
|---|---|---|
| Wallet 1 | `addr_test1qq5d0puzqsp70uut68m9kj7djwfhq2gy88gxj5g6mke8f7qudwk64wkcpnsyu9mcg2nu3kxkuyspwrh5x5ghj0u94ucsvz7r3n` | sells and bids on its own pools A1–A5, buys from and sells to wallet 2's orders |
| Wallet 2 | `addr_test1qz8r8mdqunhr5cl0d0936274upx2qwuhhcnrfurxudxuxlj62s4ndurtq2k8pf8laeqzpgnn9rcgrp8wpae58wnsa3dqgkwfy0` | sells and bids on its own pools B1–B5, buys from and sells to wallet 1's orders |

These are the same two wallets as in Milestone 2. They are public: anyone can restore one in Eternl and test with the PT and tokens it holds, see [TEST_WALLETS.md](TEST_WALLETS.md).

### Pools prepared by our team

Our team prepared these ten pools before the test, five for each wallet. Each pool minted its PT to that wallet: see the transactions in [TRANSACTIONS.md](TRANSACTIONS.md#pools-prepared-before-the-test). Each pool's folder holds the wallet's Eternl record of its transaction.

| Pool | Wallet | Token | Liquidity | Minimum order | Pool id | Matures at (UTC) |
|---|---|---|---|---|---|---|
| A1 | Wallet 1 | ADA | 1,000 | 90 | …d90521 | 2026-11-05 17:00 |
| A2 | Wallet 1 | USDC | 1,000 | 30 | …7ef808 | 2026-11-05 17:00 |
| A3 | Wallet 1 | DJED | 1,000 | 30 | …758a67 | 2026-11-05 17:00 |
| A4 | Wallet 1 | SNEK | 100,000 | 37,313 | …aaaaa7 | 2026-11-05 17:00 |
| A5 | Wallet 1 | ADA | 500 | 90 | …a80043 | 2026-11-04 14:00 |
| B1 | Wallet 2 | ADA | 500 | 90 | …2724c7 | 2026-11-04 22:00 |
| B2 | Wallet 2 | USDC | 500 | 30 | …382405 | 2026-11-04 22:00 |
| B3 | Wallet 2 | DJED | 500 | 30 | …1604dc | 2026-11-04 22:00 |
| B4 | Wallet 2 | SNEK | 50,000 | 37,313 | …e13e5a | 2026-11-04 22:00 |
| B5 | Wallet 2 | USDC | 300 | 30 | …de19a6 | 2026-11-04 14:00 |

---

## Screen recordings

All recordings, screenshots and transactions in this package were made by our team. Each recording of a transaction runs from the first click to the confirmed transaction, and the Eternl signing window is visible. The file name starts with the case ID from [CASES.md](CASES.md). The recordings are grouped by the same numbered folders as the screenshots.

### 03 · Create sell orders

| Case | Wallet | Recording | What it shows |
|---|---|---|---|
| ASK-01 | Wallet 1 | [`ASK-01-W1-sell-PT-ADA-300M-at-12pct-pool-A1.mp4`](videos/03-sell-orders-create/ASK-01-W1-sell-PT-ADA-300M-at-12pct-pool-A1.mp4) | Wallet 1 lists 300,000,000 PT ADA (300 ADA at maturity, pool A1) at 12%. |
| ASK-02 | Wallet 1 | [`ASK-02-W1-sell-PT-ADA-200M-at-10pct-pool-A1.mp4`](videos/03-sell-orders-create/ASK-02-W1-sell-PT-ADA-200M-at-10pct-pool-A1.mp4) | Wallet 1 lists 200,000,000 PT ADA (200 ADA at maturity, pool A1) at 10%. |
| ASK-03 | Wallet 1 | [`ASK-03-W1-sell-PT-ADA-150M-at-8pct-pool-A1.mp4`](videos/03-sell-orders-create/ASK-03-W1-sell-PT-ADA-150M-at-8pct-pool-A1.mp4) | Wallet 1 lists 150,000,000 PT ADA (150 ADA at maturity, pool A1) at 8%. |
| ASK-04 | Wallet 1 | [`ASK-04-W1-sell-PT-USDC-30B-at-11pct-pool-A2.mp4`](videos/03-sell-orders-create/ASK-04-W1-sell-PT-USDC-30B-at-11pct-pool-A2.mp4) | Wallet 1 lists 30,000,000,000 PT USDC (300 USDC at maturity, pool A2) at 11%. |
| ASK-05 | Wallet 1 | [`ASK-05-W1-sell-PT-USDC-20B-at-9pct-pool-A2.mp4`](videos/03-sell-orders-create/ASK-05-W1-sell-PT-USDC-20B-at-9pct-pool-A2.mp4) | Wallet 1 lists 20,000,000,000 PT USDC (200 USDC at maturity, pool A2) at 9%. |
| ASK-06 | Wallet 1 | [`ASK-06-W1-sell-PT-USDC-10B-at-9pct-pool-A2.mp4`](videos/03-sell-orders-create/ASK-06-W1-sell-PT-USDC-10B-at-9pct-pool-A2.mp4) | Wallet 1 lists 10,000,000,000 PT USDC (100 USDC at maturity, pool A2) at 9%. |
| ASK-07 | Wallet 1 | [`ASK-07-W1-sell-PT-DJED-300M-at-10-5pct-pool-A3.mp4`](videos/03-sell-orders-create/ASK-07-W1-sell-PT-DJED-300M-at-10-5pct-pool-A3.mp4) | Wallet 1 lists 300,000,000 PT DJED (300 DJED at maturity, pool A3) at 10.5%. This order was cancelled and listed again with the same amount and yield; BUY-01 bought the relisted order. The relist is in screenshots 09 to 24 of the folder and in [TRANSACTIONS.md](TRANSACTIONS.md#other-transactions-of-the-test-wallets). |
| ASK-07 | Wallet 1 | [`ASK-07-W1-sell-PT-DJED-300M-at-10-5pct-pool-A3-relist.mp4`](videos/03-sell-orders-create/ASK-07-W1-sell-PT-DJED-300M-at-10-5pct-pool-A3-relist.mp4) | Wallet 1 lists ASK-07 again after cancelling it: 300,000,000 PT DJED (pool A3) at 10.5%, as before. BUY-01 bought this order. |
| ASK-08 | Wallet 1 | [`ASK-08-W1-sell-PT-DJED-200M-at-8-5pct-pool-A3.mp4`](videos/03-sell-orders-create/ASK-08-W1-sell-PT-DJED-200M-at-8-5pct-pool-A3.mp4) | Wallet 1 lists 200,000,000 PT DJED (200 DJED at maturity, pool A3) at 8.5%. |
| ASK-09 | Wallet 1 | [`ASK-09-W1-sell-PT-DJED-30M-at-9pct-pool-A3.mp4`](videos/03-sell-orders-create/ASK-09-W1-sell-PT-DJED-30M-at-9pct-pool-A3.mp4) | Wallet 1 lists 30,000,000 PT DJED (30 DJED at maturity, pool A3) at 9%. |
| ASK-10 | Wallet 1 | [`ASK-10-W1-sell-PT-DJED-30M-at-8pct-pool-A3.mp4`](videos/03-sell-orders-create/ASK-10-W1-sell-PT-DJED-30M-at-8pct-pool-A3.mp4) | Wallet 1 lists 30,000,000 PT DJED (30 DJED at maturity, pool A3) at 8%. |
| ASK-11 | Wallet 1 | [`ASK-11-W1-sell-PT-DJED-30M-at-7pct-pool-A3.mp4`](videos/03-sell-orders-create/ASK-11-W1-sell-PT-DJED-30M-at-7pct-pool-A3.mp4) | Wallet 1 lists 30,000,000 PT DJED (30 DJED at maturity, pool A3) at 7%. |
| ASK-12 | Wallet 1 | [`ASK-12-W1-sell-PT-DJED-30M-at-6pct-pool-A3.mp4`](videos/03-sell-orders-create/ASK-12-W1-sell-PT-DJED-30M-at-6pct-pool-A3.mp4) | Wallet 1 lists 30,000,000 PT DJED (30 DJED at maturity, pool A3) at 6%. |
| ASK-13 | Wallet 1 | [`ASK-13-W1-sell-PT-DJED-30M-at-5pct-pool-A3.mp4`](videos/03-sell-orders-create/ASK-13-W1-sell-PT-DJED-30M-at-5pct-pool-A3.mp4) | Wallet 1 lists 30,000,000 PT DJED (30 DJED at maturity, pool A3) at 5%. |
| ASK-14 | Wallet 1 | [`ASK-14-W1-sell-PT-SNEK-45000-at-12pct-pool-A4.mp4`](videos/03-sell-orders-create/ASK-14-W1-sell-PT-SNEK-45000-at-12pct-pool-A4.mp4) | Wallet 1 lists 45,000 PT SNEK (45,000 SNEK at maturity, pool A4) at 12%. |
| ASK-16 | Wallet 1 | [`ASK-16-W1-sell-PT-ADA-200M-at-9pct-pool-A5.mp4`](videos/03-sell-orders-create/ASK-16-W1-sell-PT-ADA-200M-at-9pct-pool-A5.mp4) | Wallet 1 lists 200,000,000 PT ADA (200 ADA at maturity, pool A5) at 9%. |
| ASK-17 | Wallet 2 | [`ASK-17-W2-sell-PT-ADA-150M-at-11pct-pool-B1.mp4`](videos/03-sell-orders-create/ASK-17-W2-sell-PT-ADA-150M-at-11pct-pool-B1.mp4) | Wallet 2 lists 150,000,000 PT ADA (150 ADA at maturity, pool B1) at 11%. |
| ASK-18 | Wallet 2 | [`ASK-18-W2-sell-PT-ADA-100M-at-9pct-pool-B1.mp4`](videos/03-sell-orders-create/ASK-18-W2-sell-PT-ADA-100M-at-9pct-pool-B1.mp4) | Wallet 2 lists 100,000,000 PT ADA (100 ADA at maturity, pool B1) at 9%. |
| ASK-19 | Wallet 2 | [`ASK-19-W2-sell-PT-USDC-15B-at-10pct-pool-B2.mp4`](videos/03-sell-orders-create/ASK-19-W2-sell-PT-USDC-15B-at-10pct-pool-B2.mp4) | Wallet 2 lists 15,000,000,000 PT USDC (150 USDC at maturity, pool B2) at 10%. |
| ASK-20 | Wallet 2 | [`ASK-20-W2-sell-PT-DJED-150M-at-11-5pct-pool-B3.mp4`](videos/03-sell-orders-create/ASK-20-W2-sell-PT-DJED-150M-at-11-5pct-pool-B3.mp4) | Wallet 2 lists 150,000,000 PT DJED (150 DJED at maturity, pool B3) at 11.5%. |
| ASK-21 | Wallet 2 | [`ASK-21-W2-sell-PT-SNEK-40000-at-10pct-pool-B4.mp4`](videos/03-sell-orders-create/ASK-21-W2-sell-PT-SNEK-40000-at-10pct-pool-B4.mp4) | Wallet 2 lists 40,000 PT SNEK (40,000 SNEK at maturity, pool B4) at 10%. |
| ASK-22 | Wallet 2 | [`ASK-22-W2-sell-PT-USDC-10B-at-10pct-pool-B5.mp4`](videos/03-sell-orders-create/ASK-22-W2-sell-PT-USDC-10B-at-10pct-pool-B5.mp4) | Wallet 2 lists 10,000,000,000 PT USDC (100 USDC at maturity, pool B5) at 10%. |

### 04 · Update or cancel sell orders

| Case | Wallet | Recording | What it shows |
|---|---|---|---|
| CHG-ASK-01 | Wallet 1 | [`CHG-ASK-01-W1-update-ASK-03-yield-8-to-13pct-re-ranks-the-book.mp4`](videos/04-sell-orders-update-cancel/CHG-ASK-01-W1-update-ASK-03-yield-8-to-13pct-re-ranks-the-book.mp4) | Wallet 1 updates sell order ASK-03 (pool A1) from 8% to 13%, so it becomes the best offer on the book. |
| CHG-ASK-02 | Wallet 1 | [`CHG-ASK-02-W1-cancel-ASK-08-DJED-200M-untouched.mp4`](videos/04-sell-orders-update-cancel/CHG-ASK-02-W1-cancel-ASK-08-DJED-200M-untouched.mp4) | Wallet 1 cancels sell order ASK-08 (200,000,000 PT DJED, pool A3) before anyone bought from it. |
| CHG-ASK-03 | Wallet 1 | [`CHG-ASK-03-W1-update-ASK-16-amount-200M-to-150M-keeps-9pct.mp4`](videos/04-sell-orders-update-cancel/CHG-ASK-03-W1-update-ASK-16-amount-200M-to-150M-keeps-9pct.mp4) | Wallet 1 updates sell order ASK-16 (pool A5) from 200,000,000 to 150,000,000 PT ADA, same 9%. |
| CHG-ASK-04 | Wallet 1 | [`CHG-ASK-04-W1-cancel-ASK-02-after-it-was-part-bought.mp4`](videos/04-sell-orders-update-cancel/CHG-ASK-04-W1-cancel-ASK-02-after-it-was-part-bought.mp4) | Wallet 1 cancels what is left of sell order ASK-02 (pool A1) after BUY-03 bought part of it. |

### 05 · Place bids

| Case | Wallet | Recording | What it shows |
|---|---|---|---|
| BID-01 | Wallet 2 | [`BID-01-W2-bid-PT-ADA-200M-at-15pct-pool-A1.mp4`](videos/05-bids-place/BID-01-W2-bid-PT-ADA-200M-at-15pct-pool-A1.mp4) | Wallet 2 places a bid of 200,000,000 lovelace (200 ADA) on PT ADA (pool A1) at 15%. |
| BID-02 | Wallet 2 | [`BID-02-W2-bid-PT-ADA-200M-at-18pct-pool-A1.mp4`](videos/05-bids-place/BID-02-W2-bid-PT-ADA-200M-at-18pct-pool-A1.mp4) | Wallet 2 places a bid of 200,000,000 lovelace (200 ADA) on PT ADA (pool A1) at 18%. |
| BID-03 | Wallet 2 | [`BID-03-W2-bid-PT-USDC-20B-at-14pct-pool-A2.mp4`](videos/05-bids-place/BID-03-W2-bid-PT-USDC-20B-at-14pct-pool-A2.mp4) | Wallet 2 places a bid of 20,000,000,000 USDC units (200 USDC) on PT USDC (pool A2) at 14%. |
| BID-04 | Wallet 2 | [`BID-04-W2-bid-PT-USDC-20B-at-14pct-pool-A2.mp4`](videos/05-bids-place/BID-04-W2-bid-PT-USDC-20B-at-14pct-pool-A2.mp4) | Wallet 2 places a bid of 20,000,000,000 USDC units (200 USDC) on PT USDC (pool A2) at 14%. |
| BID-05 | Wallet 2 | [`BID-05-W2-bid-PT-DJED-200M-at-16pct-pool-A3.mp4`](videos/05-bids-place/BID-05-W2-bid-PT-DJED-200M-at-16pct-pool-A3.mp4) | Wallet 2 places a bid of 200,000,000 DJED units (200 DJED) on PT DJED (pool A3) at 16%. |
| BID-06 | Wallet 2 | [`BID-06-W2-bid-PT-SNEK-100000-at-15pct-pool-A4.mp4`](videos/05-bids-place/BID-06-W2-bid-PT-SNEK-100000-at-15pct-pool-A4.mp4) | Wallet 2 places a bid of 100,000 SNEK on PT SNEK (pool A4) at 15%. |
| BID-07 | Wallet 2 | [`BID-07-W2-bid-PT-ADA-100M-at-12pct-pool-A5.mp4`](videos/05-bids-place/BID-07-W2-bid-PT-ADA-100M-at-12pct-pool-A5.mp4) | Wallet 2 places a bid of 100,000,000 lovelace (100 ADA) on PT ADA (pool A5) at 12%. |
| BID-08 | Wallet 1 | [`BID-08-W1-bid-PT-ADA-150M-at-14pct-pool-B1.mp4`](videos/05-bids-place/BID-08-W1-bid-PT-ADA-150M-at-14pct-pool-B1.mp4) | Wallet 1 places a bid of 150,000,000 lovelace (150 ADA) on PT ADA (pool B1) at 14%. |
| BID-09 | Wallet 1 | [`BID-09-W1-bid-PT-ADA-250M-at-17pct-pool-B1.mp4`](videos/05-bids-place/BID-09-W1-bid-PT-ADA-250M-at-17pct-pool-B1.mp4) | Wallet 1 places a bid of 250,000,000 lovelace (250 ADA) on PT ADA (pool B1) at 17%. |
| BID-10 | Wallet 1 | [`BID-10-W1-bid-PT-USDC-15B-at-13pct-pool-B2.mp4`](videos/05-bids-place/BID-10-W1-bid-PT-USDC-15B-at-13pct-pool-B2.mp4) | Wallet 1 places a bid of 15,000,000,000 USDC units (150 USDC) on PT USDC (pool B2) at 13%. |
| BID-11 | Wallet 1 | [`BID-11-W1-bid-PT-DJED-150M-at-15pct-pool-B3.mp4`](videos/05-bids-place/BID-11-W1-bid-PT-DJED-150M-at-15pct-pool-B3.mp4) | Wallet 1 places a bid of 150,000,000 DJED units (150 DJED) on PT DJED (pool B3) at 15%. |
| BID-12 | Wallet 1 | [`BID-12-W1-bid-PT-ADA-100M-at-20pct-pool-B1.mp4`](videos/05-bids-place/BID-12-W1-bid-PT-ADA-100M-at-20pct-pool-B1.mp4) | Wallet 1 places a bid of 100,000,000 lovelace (100 ADA) on PT ADA (pool B1) at 20%. |
| BID-13 | Wallet 1 | [`BID-13-W1-bid-PT-USDC-10B-at-12pct-pool-B5.mp4`](videos/05-bids-place/BID-13-W1-bid-PT-USDC-10B-at-12pct-pool-B5.mp4) | Wallet 1 places a bid of 10,000,000,000 USDC units (100 USDC) on PT USDC (pool B5) at 12%. |
| BID-14 | Wallet 1 | [`BID-14-W1-bid-PT-DJED-50M-at-25pct-pool-B3.mp4`](videos/05-bids-place/BID-14-W1-bid-PT-DJED-50M-at-25pct-pool-B3.mp4) | Wallet 1 places a bid of 50,000,000 DJED units (50 DJED) on PT DJED (pool B3) at 25%. |
| BID-15 | Wallet 1 | [`BID-15-W1-bid-PT-DJED-40M-at-16pct-pool-B3.mp4`](videos/05-bids-place/BID-15-W1-bid-PT-DJED-40M-at-16pct-pool-B3.mp4) | Wallet 1 places a bid of 40,000,000 DJED units (40 DJED) on PT DJED (pool B3) at 16%. |
| BID-16 | Wallet 1 | [`BID-16-W1-bid-PT-DJED-40M-at-17pct-pool-B3.mp4`](videos/05-bids-place/BID-16-W1-bid-PT-DJED-40M-at-17pct-pool-B3.mp4) | Wallet 1 places a bid of 40,000,000 DJED units (40 DJED) on PT DJED (pool B3) at 17%. |
| BID-17 | Wallet 1 | [`BID-17-W1-bid-PT-DJED-40M-at-18pct-pool-B3.mp4`](videos/05-bids-place/BID-17-W1-bid-PT-DJED-40M-at-18pct-pool-B3.mp4) | Wallet 1 places a bid of 40,000,000 DJED units (40 DJED) on PT DJED (pool B3) at 18%. |
| BID-18 | Wallet 1 | [`BID-18-W1-bid-PT-DJED-40M-at-19pct-pool-B3.mp4`](videos/05-bids-place/BID-18-W1-bid-PT-DJED-40M-at-19pct-pool-B3.mp4) | Wallet 1 places a bid of 40,000,000 DJED units (40 DJED) on PT DJED (pool B3) at 19%. |

### 06 · Update or cancel bids

| Case | Wallet | Recording | What it shows |
|---|---|---|---|
| CHG-BID-01 | Wallet 1 | [`CHG-BID-01-W1-update-BID-09-amount-250M-to-200M-and-yield-17-to-16pct.mp4`](videos/06-bids-update-cancel/CHG-BID-01-W1-update-BID-09-amount-250M-to-200M-and-yield-17-to-16pct.mp4) | Wallet 1 updates bid BID-09 (pool B1) from 250,000,000 lovelace at 17% to 200,000,000 lovelace at 16%. |
| CHG-BID-02 | Wallet 1 | [`CHG-BID-02-W1-update-BID-10-yield-only-13-to-15pct.mp4`](videos/06-bids-update-cancel/CHG-BID-02-W1-update-BID-10-yield-only-13-to-15pct.mp4) | Wallet 1 updates bid BID-10 (pool B2) from 13% to 15%, the amount stays 15,000,000,000 USDC units. |
| CHG-BID-03 | Wallet 1 | [`CHG-BID-03-W1-update-BID-11-amount-only-150M-to-200M.mp4`](videos/06-bids-update-cancel/CHG-BID-03-W1-update-BID-11-amount-only-150M-to-200M.mp4) | Wallet 1 updates bid BID-11 (pool B3) from 150,000,000 to 200,000,000 DJED units, the yield stays 15%. |
| CHG-BID-04 | Wallet 1 | [`CHG-BID-04-W1-cancel-BID-12-ADA-bid-100M.mp4`](videos/06-bids-update-cancel/CHG-BID-04-W1-cancel-BID-12-ADA-bid-100M.mp4) | Wallet 1 cancels bid BID-12 (pool B1, 100,000,000 lovelace); the 100 ADA and the ADA held beside it come back. |
| CHG-BID-05 | Wallet 1 | [`CHG-BID-05-W1-cancel-BID-14-token-bid-50M-DJED.mp4`](videos/06-bids-update-cancel/CHG-BID-05-W1-cancel-BID-14-token-bid-50M-DJED.mp4) | Wallet 1 cancels bid BID-14 (pool B3, 50,000,000 DJED units), a bid in a token; the 50 DJED and the 2 ADA held beside it come back, less the network fee. |
| CHG-BID-07 | Wallet 2 | [`CHG-BID-07-W2-cancel-the-tie-bid-that-SELL-02-part-filled.mp4`](videos/06-bids-update-cancel/CHG-BID-07-W2-cancel-the-tie-bid-that-SELL-02-part-filled.mp4) | Wallet 2 cancels what is left of bid BID-03 (pool A2) after SELL-02 filled part of it: 109.48 USDC and the ADA held beside it return. |

### 07 · Buy: market orders against the sell orders

| Case | Wallet | Recording | What it shows |
|---|---|---|---|
| BUY-01 | Wallet 2 | [`BUY-01-W2-max-buy-6-orders-in-one-tx-PT-DJED-450M-pool-A3.mp4`](videos/07-buy-market-orders/BUY-01-W2-max-buy-6-orders-in-one-tx-PT-DJED-450M-pool-A3.mp4) | Wallet 2 buys 450,000,000 PT DJED with Max: one transaction fills six sell orders. Matched: ASK-07 (10.5%, the relisted order), ASK-09 (9%), ASK-10 (8%), ASK-11 (7%), ASK-12 (6%) and ASK-13 (5%), all whole. |
| BUY-02 | Wallet 2 | [`BUY-02-W2-part-of-order-ASK-04-PT-USDC-10B-pool-A2.mp4`](videos/07-buy-market-orders/BUY-02-W2-part-of-order-ASK-04-PT-USDC-10B-pool-A2.mp4) | Wallet 2 buys 10,000,000,000 PT USDC, part of ASK-04 at 11%. Matched: ASK-04 (11%) part. |
| BUY-03 | Wallet 2 | [`BUY-03-W2-sweep-3-orders-best-yield-first-PT-ADA-550M-pool-A1.mp4`](videos/07-buy-market-orders/BUY-03-W2-sweep-3-orders-best-yield-first-PT-ADA-550M-pool-A1.mp4) | Wallet 2 buys 550,000,000 PT ADA in one transaction: ASK-03 (13%) and ASK-01 (12%) whole, ASK-02 (10%) part. Matched: ASK-03 (13%) whole, ASK-01 (12%) whole, ASK-02 (10%) part. |
| BUY-04 | Wallet 2 | [`BUY-04-W2-part-of-order-SNEK-keeps-more-than-minimum-PT-SNEK-5000-pool-A4.mp4`](videos/07-buy-market-orders/BUY-04-W2-part-of-order-SNEK-keeps-more-than-minimum-PT-SNEK-5000-pool-A4.mp4) | Wallet 2 buys 5,000 PT SNEK, part of ASK-14 at 12%. Matched: ASK-14 (12%) part. |
| BUY-05 | Wallet 2 | [`BUY-05-W2-sweep-3-orders-with-a-yield-tie-PT-USDC-45B-pool-A2.mp4`](videos/07-buy-market-orders/BUY-05-W2-sweep-3-orders-with-a-yield-tie-PT-USDC-45B-pool-A2.mp4) | Wallet 2 buys 45,000,000,000 PT USDC in one transaction: the remaining 20,000,000,000 of ASK-04 (11%), then 25,000,000,000 from the two 9% orders. Matched: rest of ASK-04 (11%), ASK-05 (9%) whole, ASK-06 (9%) part. |
| BUY-06 | Wallet 2 | [`BUY-06-W2-whole-order-exactly-the-minimum-short-pool-PT-ADA-90M-pool-A5.mp4`](videos/07-buy-market-orders/BUY-06-W2-whole-order-exactly-the-minimum-short-pool-PT-ADA-90M-pool-A5.mp4) | Wallet 2 buys 90,000,000 PT ADA, the whole of ASK-15 (exactly the pool minimum) at 10%. Matched: ASK-15 (10%) whole. |
| BUY-07 | Wallet 1 | [`BUY-07-W1-sweep-2-orders-the-book-is-emptied-PT-ADA-250M-pool-B1.mp4`](videos/07-buy-market-orders/BUY-07-W1-sweep-2-orders-the-book-is-emptied-PT-ADA-250M-pool-B1.mp4) | Wallet 1 buys 250,000,000 PT ADA in one transaction: all of ASK-17 (11%) and all of ASK-18 (9%). Matched: ASK-17 (11%) whole, ASK-18 (9%) whole. |
| BUY-08 | Wallet 1 | [`BUY-08-W1-part-of-order-ASK-19-PT-USDC-5B-pool-B2.mp4`](videos/07-buy-market-orders/BUY-08-W1-part-of-order-ASK-19-PT-USDC-5B-pool-B2.mp4) | Wallet 1 buys 5,000,000,000 PT USDC, part of ASK-19 at 10%. Matched: ASK-19 (10%) part. |
| BUY-09 | Wallet 1 | [`BUY-09-W1-whole-order-ASK-20-PT-DJED-150M-pool-B3.mp4`](videos/07-buy-market-orders/BUY-09-W1-whole-order-ASK-20-PT-DJED-150M-pool-B3.mp4) | Wallet 1 buys 150,000,000 PT DJED, the whole of ASK-20 at 11.5%. Matched: ASK-20 (11.5%) whole. |
| BUY-10 | Wallet 1 | [`BUY-10-W1-whole-order-token-short-pool-PT-USDC-10B-pool-B5.mp4`](videos/07-buy-market-orders/BUY-10-W1-whole-order-token-short-pool-PT-USDC-10B-pool-B5.mp4) | Wallet 1 buys 10,000,000,000 PT USDC, the whole of ASK-22 (short pool B5) at 10%. Matched: ASK-22 (10%) whole. |
| BUY-12 | Wallet 2 | [`BUY-12-W2-last-USDC-order-after-the-tie-PT-USDC-5B-pool-A2.mp4`](videos/07-buy-market-orders/BUY-12-W2-last-USDC-order-after-the-tie-PT-USDC-5B-pool-A2.mp4) | Wallet 2 buys the 5,000,000,000 PT USDC left on ASK-06 (9%) after BUY-05. Matched: rest of ASK-06 (9%). |

### 08 · Sell to bids: market orders against the bids

| Case | Wallet | Recording | What it shows |
|---|---|---|---|
| SELL-01 | Wallet 1 | [`SELL-01-W1-max-sweeps-2-bids-first-bid-filled-out-PT-ADA-pool-A1.mp4`](videos/08-sell-to-bids-market-orders/SELL-01-W1-max-sweeps-2-bids-first-bid-filled-out-PT-ADA-pool-A1.mp4) | Wallet 1 sells all its free PT ADA of pool A1 (349,999,999) to the bids with Max: BID-01 (15%) is filled out, then BID-02 (18%) takes the rest. The 88 ADA left on BID-02 is below the 90 ADA minimum, so BID-02 closes too and the 88 ADA returns to wallet 2 in the same transaction. |
| SELL-02 | Wallet 1 | [`SELL-02-W1-part-of-a-bid-with-a-yield-tie-PT-USDC-pool-A2.mp4`](videos/08-sell-to-bids-market-orders/SELL-02-W1-part-of-a-bid-with-a-yield-tie-PT-USDC-pool-A2.mp4) | Wallet 1 sells 10,000,000,000 PT USDC on pool A2, where two bids tie at 14%: it fills part of BID-03, the older one; BID-04 is untouched. |
| SELL-03 | Wallet 1 | [`SELL-03-W1-leaves-less-than-minimum-so-the-bid-closes-PT-DJED-pool-A3.mp4`](videos/08-sell-to-bids-market-orders/SELL-03-W1-leaves-less-than-minimum-so-the-bid-closes-PT-DJED-pool-A3.mp4) | Wallet 1 sells 210,000,000 PT DJED to BID-05 (16%). The 12.49 DJED left on BID-05 is below the 30 DJED minimum, so BID-05 closes and that amount returns to wallet 2 in the same transaction. |
| SELL-04 | Wallet 1 | [`SELL-04-W1-part-of-a-bid-SNEK-PT-SNEK-pool-A4.mp4`](videos/08-sell-to-bids-market-orders/SELL-04-W1-part-of-a-bid-SNEK-PT-SNEK-pool-A4.mp4) | Wallet 1 sells 40,000 PT SNEK to BID-06 (15%). |
| SELL-05 | Wallet 2 | [`SELL-05-W2-max-sweeps-2-bids-first-bid-filled-out-PT-ADA-pool-B1.mp4`](videos/08-sell-to-bids-market-orders/SELL-05-W2-max-sweeps-2-bids-first-bid-filled-out-PT-ADA-pool-B1.mp4) | Wallet 2 sells all its free PT ADA of pool B1 (249,999,999) to the bids with Max: BID-08 (14%) is filled out, then BID-09 (16%) is part-filled and keeps 106 ADA. Wallet 2 receives 240.57 ADA, net of fees. |
| SELL-06 | Wallet 2 | [`SELL-06-W2-sells-to-4-bids-max-per-transaction-PT-DJED-pool-B3.mp4`](videos/08-sell-to-bids-market-orders/SELL-06-W2-sells-to-4-bids-max-per-transaction-PT-DJED-pool-B3.mp4) | Wallet 2 sells 329,000,000 PT DJED to the five bids on pool B3. One transaction fills four bids out (15%, 16%, 17% and 18%) and the 19% bid stays on the book. |
| SELL-07 | Wallet 2 | [`SELL-07-W2-part-of-a-bid-USDC-PT-USDC-pool-B2.mp4`](videos/08-sell-to-bids-market-orders/SELL-07-W2-part-of-a-bid-USDC-PT-USDC-pool-B2.mp4) | Wallet 2 sells 10,000,000,000 PT USDC to BID-10 (15%), part of the bid; 52.59 USDC stay on it. |

### 11 · Trade history

| Case | Wallet | Recording | What it shows |
|---|---|---|---|
| HIST-08 | Wallet 1 | [`HIST-08-W1-history-updates-by-itself.mp4`](videos/11-trade-history/HIST-08-W1-history-updates-by-itself.mp4) | Wallet 1 keeps its History page (Buy orders, All) open in one tab and, in another, sells 10,000,000,000 PT USDC of pool A2 to BID-04 (14%). About 30 seconds after it returns to the History tab, the new row appears without a reload: 05 Nov 2026 08:54:41 (UTC+7; 01:54:41 UTC), pUSDC, 100 PT, 14.00%, 94.71 USDC paid by the bid, seller *You*. |

### 12 · Matured pools and redeem

| Case | Wallet | Recording | What it shows |
|---|---|---|---|
| MAT-01 | Wallet 2 | [`MAT-01-W2-cancel-BID-07-on-a-matured-pool-A5.mp4`](videos/12-matured-pools-and-redeem/MAT-01-W2-cancel-BID-07-on-a-matured-pool-A5.mp4) | Wallet 2 cancels bid BID-07 (100 ADA at 12%) on pool A5 after the pool matured. The dialog says *This market has matured, so the bid can no longer fill*; the 100 ADA and the 2 ADA held beside it return, less the network fee. |
| MAT-02 | Wallet 2 | [`MAT-02-W2-redeem-PT-ADA-pool-A5-bought-earlier.mp4`](videos/12-matured-pools-and-redeem/MAT-02-W2-redeem-PT-ADA-pool-A5-bought-earlier.mp4) | Wallet 2 redeems the 90,000,000 PT ADA of pool A5 bought in BUY-06. The popup shows *Total redeem 90 ADA*; the wallet receives 3,878.492574 qAda, the form in which pool A5 holds its ADA. |
| MAT-03 | Wallet 2 | [`MAT-03-W2-redeem-PT-USDC-pool-B5-own-pool.mp4`](videos/12-matured-pools-and-redeem/MAT-03-W2-redeem-PT-USDC-pool-B5-own-pool.mp4) | Wallet 2 redeems the 19,999,999,999 PT USDC it still holds of its own pool B5 and receives 200 USDC. |
| MAT-04 | Wallet 1 | [`MAT-04-W1-cancel-BID-13-USDC-bid-on-a-matured-pool-B5.mp4`](videos/12-matured-pools-and-redeem/MAT-04-W1-cancel-BID-13-USDC-bid-on-a-matured-pool-B5.mp4) | Wallet 1 cancels bid BID-13 (100 USDC at 12%) on pool B5 after the pool matured; the 100 USDC and the ADA held beside it return. |
| MAT-05 | Wallet 1 | [`MAT-05-W1-redeem-PT-ADA-pool-A5-with-the-order-still-listed.mp4`](videos/12-matured-pools-and-redeem/MAT-05-W1-redeem-PT-ADA-pool-A5-with-the-order-still-listed.mp4) | Wallet 1 redeems all its PT ADA of pool A5 while ASK-16 (150,000,000 PT at 9%) is still listed. The popup says *Withdrawn from your order in this transaction*; the order leaves My Account in the same transaction, and wallet 1 receives 413.31 ADA, net of the network fee. |
| MAT-06 | Wallet 1 | [`MAT-06-W1-redeem-PT-USDC-pool-B5-bought-earlier.mp4`](videos/12-matured-pools-and-redeem/MAT-06-W1-redeem-PT-USDC-pool-B5-bought-earlier.mp4) | Wallet 1 redeems the 10,000,000,000 PT USDC of pool B5 bought in BUY-10 and receives 100 USDC. |

---

## Contents

```
README.md               this page
USER_GUIDE.md           step-by-step guide, with screenshots
CASES.md                every case, grouped (122 cases)
TRANSACTIONS.md         every transaction, with its Cardanoscan link
MATCHING.md             how orders are matched, with the trades worked through
TEST_WALLETS.md         the two public test wallets, ready to restore in Eternl
screenshots/            one folder per case, in numbered groups
videos/                 screen recordings of the transactions, in the same groups
```

## What the cases cover

| What | Cases |
|---|---|
| A sell order in each token | ASK-01 (ADA), ASK-04 (USDC), ASK-07 (DJED), ASK-14 (SNEK) |
| Several sell orders at different yields on one PT | ASK-01 to ASK-03, ASK-04 to ASK-06, ASK-07 to ASK-13 |
| A sell order of exactly the pool minimum | ASK-15, ASK-09 to ASK-13 |
| Two orders at the same yield | ASK-05 and ASK-06, BID-03 and BID-04 |
| A bid in ADA and a bid in a token | BID-01, BID-03 |
| Buy a whole order / part of an order | BUY-06, BUY-09, BUY-10 / BUY-02, BUY-04, BUY-08 (the rest of a part-bought order: BUY-12) |
| Buy sweeping several orders in one transaction | BUY-01, BUY-03, BUY-05, BUY-07 |
| Buy with Max sweeping six orders in one transaction | BUY-01 |
| Sell to a bid, part of the bid | SELL-02, SELL-04, SELL-07, HIST-08 |
| Sell to bids, bid filled out, or closed because what was left fell below the minimum | SELL-01, SELL-03, SELL-05, SELL-06 |
| Sell sweeping several bids | SELL-01, SELL-05, SELL-06 (four bids, the most one sale takes in one transaction) |
| Update a sell order / cancel one | CHG-ASK-01, CHG-ASK-03 / CHG-ASK-02, CHG-ASK-04 |
| Update a bid (amount and yield, yield only, amount only) | CHG-BID-01, CHG-BID-02, CHG-BID-03 |
| Cancel a bid (ADA, token, part-filled) | CHG-BID-04, CHG-BID-05, CHG-BID-07 |
| A pool that matured: cancel a bid, redeem, redeem with an order still listed | MAT-01, MAT-04 / MAT-02, MAT-03, MAT-06 / MAT-05 |
| Price changes with the time left and the yield; the fees | PRICE-01, PRICE-02, PRICE-03 |
| The order book display | BOOK-01 to BOOK-09 |
| The trade history | HIST-01 to HIST-10 |
| Actions the app blocks | BLOCK-01 to BLOCK-13 |

---

## Notes

- **Orders are matched when a trader takes them.** A buy fills against the sell orders on the book, best yield first; a sale to bids fills against the bids, lowest yield first. See [MATCHING.md](MATCHING.md).
- **Maturity.** On Preview a protocol day is 6 minutes and a year counts as 36.5 hours. The maturity of each pool is in the table above. The two short pools, A5 and B5, mature during the test, so that matured pools can be shown. PT can be listed and bought until maturity; after that it is redeemed for the underlying token.
- **Fees.** The buyer pays 0.2% of the price and the seller 0.1%. A transaction also costs a small ADA network fee.
- **Times.** The pool table and [TRANSACTIONS.md](TRANSACTIONS.md) give times in UTC. The app screenshots show UTC+7: *05-Nov-26 05:00* in a screenshot is 2026-11-04 22:00 UTC.
