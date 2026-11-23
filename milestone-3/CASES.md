# Cases

Every case of Milestone 3, grouped by what it shows. The folder names in `screenshots/` and `videos/` start with the case ID.

## How to read a name

`BUY-03-W2-sweep-3-orders-best-yield-first-PT-ADA-550M-pool-A1`

- `BUY` is the group: SETUP, ASK, CHG-ASK, BID, CHG-BID, BUY, SELL, BOOK, PRICE, HIST, MAT, BLOCK, ACC.
- `03` is the number inside the group.
- `W2` is the wallet that acts: W1 is wallet 1, W2 is wallet 2.
- The rest says what happens: the token, the amount in raw units and the pool. Pools A1–A5 are wallet 1's, pools B1–B5 wallet 2's.
- `SETUP` is not a feature of the app: it is the ten pools our team prepared before the test, with the transaction of each.


## 02 · Pools prepared by the team before the test

| ID | What it shows | Signature | Folder |
|---|---|---|---|
| SETUP-01 | Wallet 1 prepared pool A1: 1,000 ADA, minimum order 90 ADA; the pool's PT was minted to wallet 1 | yes | [SETUP-01-W1-prepared-pool-A1-ADA-1000-tx-66c430d9](screenshots/02-setup-pools-prepared-by-the-team/SETUP-01-W1-prepared-pool-A1-ADA-1000-tx-66c430d9) |
| SETUP-02 | Wallet 1 prepared pool A2: 1,000 USDC, minimum order 30 USDC; the pool's PT was minted to wallet 1 | yes | [SETUP-02-W1-prepared-pool-A2-USDC-1000-tx-d590f965](screenshots/02-setup-pools-prepared-by-the-team/SETUP-02-W1-prepared-pool-A2-USDC-1000-tx-d590f965) |
| SETUP-03 | Wallet 1 prepared pool A3: 1,000 DJED, minimum order 30 DJED; the pool's PT was minted to wallet 1 | yes | [SETUP-03-W1-prepared-pool-A3-DJED-1000-tx-a5430239](screenshots/02-setup-pools-prepared-by-the-team/SETUP-03-W1-prepared-pool-A3-DJED-1000-tx-a5430239) |
| SETUP-04 | Wallet 1 prepared pool A4: 100,000 SNEK, minimum order 37,313 SNEK; the pool's PT was minted to wallet 1 | yes | [SETUP-04-W1-prepared-pool-A4-SNEK-100000-tx-049aeb08](screenshots/02-setup-pools-prepared-by-the-team/SETUP-04-W1-prepared-pool-A4-SNEK-100000-tx-049aeb08) |
| SETUP-05 | Wallet 1 prepared pool A5: 500 ADA, minimum order 90 ADA; the pool's PT was minted to wallet 1 (used later to show a matured pool) | yes | [SETUP-05-W1-prepared-pool-A5-ADA-500-tx-89ff0a78](screenshots/02-setup-pools-prepared-by-the-team/SETUP-05-W1-prepared-pool-A5-ADA-500-tx-89ff0a78) |
| SETUP-06 | Wallet 2 prepared pool B1: 500 ADA, minimum order 90 ADA; the pool's PT was minted to wallet 2 | yes | [SETUP-06-W2-prepared-pool-B1-ADA-500-tx-7bd23a27](screenshots/02-setup-pools-prepared-by-the-team/SETUP-06-W2-prepared-pool-B1-ADA-500-tx-7bd23a27) |
| SETUP-07 | Wallet 2 prepared pool B2: 500 USDC, minimum order 30 USDC; the pool's PT was minted to wallet 2 | yes | [SETUP-07-W2-prepared-pool-B2-USDC-500-tx-b6fd048a](screenshots/02-setup-pools-prepared-by-the-team/SETUP-07-W2-prepared-pool-B2-USDC-500-tx-b6fd048a) |
| SETUP-08 | Wallet 2 prepared pool B3: 500 DJED, minimum order 30 DJED; the pool's PT was minted to wallet 2 | yes | [SETUP-08-W2-prepared-pool-B3-DJED-500-tx-546000be](screenshots/02-setup-pools-prepared-by-the-team/SETUP-08-W2-prepared-pool-B3-DJED-500-tx-546000be) |
| SETUP-09 | Wallet 2 prepared pool B4: 50,000 SNEK, minimum order 37,313 SNEK; the pool's PT was minted to wallet 2 | yes | [SETUP-09-W2-prepared-pool-B4-SNEK-50000-tx-b675dcf3](screenshots/02-setup-pools-prepared-by-the-team/SETUP-09-W2-prepared-pool-B4-SNEK-50000-tx-b675dcf3) |
| SETUP-10 | Wallet 2 prepared pool B5: 300 USDC, minimum order 30 USDC; the pool's PT was minted to wallet 2 (used later to show a matured pool) | yes | [SETUP-10-W2-prepared-pool-B5-USDC-300-tx-de81cc5f](screenshots/02-setup-pools-prepared-by-the-team/SETUP-10-W2-prepared-pool-B5-USDC-300-tx-de81cc5f) |

## 03 · Create sell orders

| ID | What it shows | Signature | Folder |
|---|---|---|---|
| ASK-01 | Wallet 1 lists 300,000,000 PT ADA (300 ADA at maturity, pool A1) at 12% | yes | [ASK-01-W1-sell-PT-ADA-300M-at-12pct-pool-A1-tx-f3e476d5](screenshots/03-sell-orders-create/ASK-01-W1-sell-PT-ADA-300M-at-12pct-pool-A1-tx-f3e476d5) |
| ASK-02 | Wallet 1 lists 200,000,000 PT ADA (200 ADA at maturity, pool A1) at 10% | yes | [ASK-02-W1-sell-PT-ADA-200M-at-10pct-pool-A1-tx-5390db87](screenshots/03-sell-orders-create/ASK-02-W1-sell-PT-ADA-200M-at-10pct-pool-A1-tx-5390db87) |
| ASK-03 | Wallet 1 lists 150,000,000 PT ADA (150 ADA at maturity, pool A1) at 8% | yes | [ASK-03-W1-sell-PT-ADA-150M-at-8pct-pool-A1-tx-f312fc70](screenshots/03-sell-orders-create/ASK-03-W1-sell-PT-ADA-150M-at-8pct-pool-A1-tx-f312fc70) |
| ASK-04 | Wallet 1 lists 30,000,000,000 PT USDC (300 USDC at maturity, pool A2) at 11% | yes | [ASK-04-W1-sell-PT-USDC-30B-at-11pct-pool-A2-tx-78311866](screenshots/03-sell-orders-create/ASK-04-W1-sell-PT-USDC-30B-at-11pct-pool-A2-tx-78311866) |
| ASK-05 | Wallet 1 lists 20,000,000,000 PT USDC (200 USDC at maturity, pool A2) at 9% | yes | [ASK-05-W1-sell-PT-USDC-20B-at-9pct-pool-A2-tx-918d2fb1](screenshots/03-sell-orders-create/ASK-05-W1-sell-PT-USDC-20B-at-9pct-pool-A2-tx-918d2fb1) |
| ASK-06 | Wallet 1 lists 10,000,000,000 PT USDC (100 USDC at maturity, pool A2) at 9% | yes | [ASK-06-W1-sell-PT-USDC-10B-at-9pct-pool-A2-tx-5dc9b9fa](screenshots/03-sell-orders-create/ASK-06-W1-sell-PT-USDC-10B-at-9pct-pool-A2-tx-5dc9b9fa) |
| ASK-07 | Wallet 1 lists 300,000,000 PT DJED (300 DJED at maturity, pool A3) at 10.5%. This order was cancelled and listed again with the same amount and yield; BUY-01 bought the relisted order. The relist is in screenshots 09 to 24 of the folder and in [TRANSACTIONS.md](TRANSACTIONS.md#other-transactions-of-the-test-wallets) | yes | [ASK-07-W1-sell-PT-DJED-300M-at-10-5pct-pool-A3-tx-63661e56](screenshots/03-sell-orders-create/ASK-07-W1-sell-PT-DJED-300M-at-10-5pct-pool-A3-tx-63661e56) |
| ASK-08 | Wallet 1 lists 200,000,000 PT DJED (200 DJED at maturity, pool A3) at 8.5% | yes | [ASK-08-W1-sell-PT-DJED-200M-at-8-5pct-pool-A3-tx-9700d58b](screenshots/03-sell-orders-create/ASK-08-W1-sell-PT-DJED-200M-at-8-5pct-pool-A3-tx-9700d58b) |
| ASK-09 | Wallet 1 lists 30,000,000 PT DJED (30 DJED at maturity, pool A3) at 9% | yes | [ASK-09-W1-sell-PT-DJED-30M-at-9pct-pool-A3-tx-c81deba3](screenshots/03-sell-orders-create/ASK-09-W1-sell-PT-DJED-30M-at-9pct-pool-A3-tx-c81deba3) |
| ASK-10 | Wallet 1 lists 30,000,000 PT DJED (30 DJED at maturity, pool A3) at 8% | yes | [ASK-10-W1-sell-PT-DJED-30M-at-8pct-pool-A3-tx-2144ce2b](screenshots/03-sell-orders-create/ASK-10-W1-sell-PT-DJED-30M-at-8pct-pool-A3-tx-2144ce2b) |
| ASK-11 | Wallet 1 lists 30,000,000 PT DJED (30 DJED at maturity, pool A3) at 7% | yes | [ASK-11-W1-sell-PT-DJED-30M-at-7pct-pool-A3-tx-0a7e8719](screenshots/03-sell-orders-create/ASK-11-W1-sell-PT-DJED-30M-at-7pct-pool-A3-tx-0a7e8719) |
| ASK-12 | Wallet 1 lists 30,000,000 PT DJED (30 DJED at maturity, pool A3) at 6% | yes | [ASK-12-W1-sell-PT-DJED-30M-at-6pct-pool-A3-tx-63cb585f](screenshots/03-sell-orders-create/ASK-12-W1-sell-PT-DJED-30M-at-6pct-pool-A3-tx-63cb585f) |
| ASK-13 | Wallet 1 lists 30,000,000 PT DJED (30 DJED at maturity, pool A3) at 5% | yes | [ASK-13-W1-sell-PT-DJED-30M-at-5pct-pool-A3-tx-f170c84e](screenshots/03-sell-orders-create/ASK-13-W1-sell-PT-DJED-30M-at-5pct-pool-A3-tx-f170c84e) |
| ASK-14 | Wallet 1 lists 45,000 PT SNEK (45,000 SNEK at maturity, pool A4) at 12% | yes | [ASK-14-W1-sell-PT-SNEK-45000-at-12pct-pool-A4-tx-60822ea2](screenshots/03-sell-orders-create/ASK-14-W1-sell-PT-SNEK-45000-at-12pct-pool-A4-tx-60822ea2) |
| ASK-15 | Wallet 1 lists 90,000,000 PT ADA (90 ADA at maturity, pool A5) at 10% | yes | [ASK-15-W1-sell-PT-ADA-90M-at-10pct-pool-A5-tx-ea174bcf](screenshots/03-sell-orders-create/ASK-15-W1-sell-PT-ADA-90M-at-10pct-pool-A5-tx-ea174bcf) |
| ASK-16 | Wallet 1 lists 200,000,000 PT ADA (200 ADA at maturity, pool A5) at 9% | yes | [ASK-16-W1-sell-PT-ADA-200M-at-9pct-pool-A5-tx-276247e9](screenshots/03-sell-orders-create/ASK-16-W1-sell-PT-ADA-200M-at-9pct-pool-A5-tx-276247e9) |
| ASK-17 | Wallet 2 lists 150,000,000 PT ADA (150 ADA at maturity, pool B1) at 11% | yes | [ASK-17-W2-sell-PT-ADA-150M-at-11pct-pool-B1-tx-bb2faf8b](screenshots/03-sell-orders-create/ASK-17-W2-sell-PT-ADA-150M-at-11pct-pool-B1-tx-bb2faf8b) |
| ASK-18 | Wallet 2 lists 100,000,000 PT ADA (100 ADA at maturity, pool B1) at 9% | yes | [ASK-18-W2-sell-PT-ADA-100M-at-9pct-pool-B1-tx-95a15dcc](screenshots/03-sell-orders-create/ASK-18-W2-sell-PT-ADA-100M-at-9pct-pool-B1-tx-95a15dcc) |
| ASK-19 | Wallet 2 lists 15,000,000,000 PT USDC (150 USDC at maturity, pool B2) at 10% | yes | [ASK-19-W2-sell-PT-USDC-15B-at-10pct-pool-B2-tx-2ff5a646](screenshots/03-sell-orders-create/ASK-19-W2-sell-PT-USDC-15B-at-10pct-pool-B2-tx-2ff5a646) |
| ASK-20 | Wallet 2 lists 150,000,000 PT DJED (150 DJED at maturity, pool B3) at 11.5% | yes | [ASK-20-W2-sell-PT-DJED-150M-at-11-5pct-pool-B3-tx-54fc0d0a](screenshots/03-sell-orders-create/ASK-20-W2-sell-PT-DJED-150M-at-11-5pct-pool-B3-tx-54fc0d0a) |
| ASK-21 | Wallet 2 lists 40,000 PT SNEK (40,000 SNEK at maturity, pool B4) at 10% | yes | [ASK-21-W2-sell-PT-SNEK-40000-at-10pct-pool-B4-tx-3d21a585](screenshots/03-sell-orders-create/ASK-21-W2-sell-PT-SNEK-40000-at-10pct-pool-B4-tx-3d21a585) |
| ASK-22 | Wallet 2 lists 10,000,000,000 PT USDC (100 USDC at maturity, pool B5) at 10% | yes | [ASK-22-W2-sell-PT-USDC-10B-at-10pct-pool-B5-tx-89018ece](screenshots/03-sell-orders-create/ASK-22-W2-sell-PT-USDC-10B-at-10pct-pool-B5-tx-89018ece) |

## 04 · Update or cancel sell orders

| ID | What it shows | Signature | Folder |
|---|---|---|---|
| CHG-ASK-01 | Wallet 1 updates sell order ASK-03 (pool A1) from 8% to 13%, so it becomes the best offer on the book | yes | [CHG-ASK-01-W1-update-ASK-03-yield-8-to-13pct-re-ranks-the-book-tx-441c71d2](screenshots/04-sell-orders-update-cancel/CHG-ASK-01-W1-update-ASK-03-yield-8-to-13pct-re-ranks-the-book-tx-441c71d2) |
| CHG-ASK-02 | Wallet 1 cancels sell order ASK-08 (200,000,000 PT DJED, pool A3) before anyone bought from it | yes | [CHG-ASK-02-W1-cancel-ASK-08-DJED-200M-untouched-tx-ca202e63](screenshots/04-sell-orders-update-cancel/CHG-ASK-02-W1-cancel-ASK-08-DJED-200M-untouched-tx-ca202e63) |
| CHG-ASK-03 | Wallet 1 updates sell order ASK-16 (pool A5) from 200,000,000 to 150,000,000 PT ADA, same 9% | yes | [CHG-ASK-03-W1-update-ASK-16-amount-200M-to-150M-keeps-9pct-tx-d1ebfe0d](screenshots/04-sell-orders-update-cancel/CHG-ASK-03-W1-update-ASK-16-amount-200M-to-150M-keeps-9pct-tx-d1ebfe0d) |
| CHG-ASK-04 | Wallet 1 cancels what is left of sell order ASK-02 (pool A1) after BUY-03 bought part of it | yes | [CHG-ASK-04-W1-cancel-ASK-02-after-it-was-part-bought-tx-46ec059a](screenshots/04-sell-orders-update-cancel/CHG-ASK-04-W1-cancel-ASK-02-after-it-was-part-bought-tx-46ec059a) |

## 05 · Place bids (limit orders)

| ID | What it shows | Signature | Folder |
|---|---|---|---|
| BID-01 | Wallet 2 places a bid of 200,000,000 lovelace (200 ADA) on PT ADA (pool A1) at 15% | yes | [BID-01-W2-bid-PT-ADA-200M-at-15pct-pool-A1-tx-d56b543e](screenshots/05-bids-place/BID-01-W2-bid-PT-ADA-200M-at-15pct-pool-A1-tx-d56b543e) |
| BID-02 | Wallet 2 places a bid of 200,000,000 lovelace (200 ADA) on PT ADA (pool A1) at 18% | yes | [BID-02-W2-bid-PT-ADA-200M-at-18pct-pool-A1-tx-bd081a75](screenshots/05-bids-place/BID-02-W2-bid-PT-ADA-200M-at-18pct-pool-A1-tx-bd081a75) |
| BID-03 | Wallet 2 places a bid of 20,000,000,000 USDC units (200 USDC) on PT USDC (pool A2) at 14% | yes | [BID-03-W2-bid-PT-USDC-20B-at-14pct-pool-A2-tx-6bc58069](screenshots/05-bids-place/BID-03-W2-bid-PT-USDC-20B-at-14pct-pool-A2-tx-6bc58069) |
| BID-04 | Wallet 2 places a bid of 20,000,000,000 USDC units (200 USDC) on PT USDC (pool A2) at 14% | yes | [BID-04-W2-bid-PT-USDC-20B-at-14pct-pool-A2-tx-b388b07d](screenshots/05-bids-place/BID-04-W2-bid-PT-USDC-20B-at-14pct-pool-A2-tx-b388b07d) |
| BID-05 | Wallet 2 places a bid of 200,000,000 DJED units (200 DJED) on PT DJED (pool A3) at 16% | yes | [BID-05-W2-bid-PT-DJED-200M-at-16pct-pool-A3-tx-ae9d8cc2](screenshots/05-bids-place/BID-05-W2-bid-PT-DJED-200M-at-16pct-pool-A3-tx-ae9d8cc2) |
| BID-06 | Wallet 2 places a bid of 100,000 SNEK on PT SNEK (pool A4) at 15% | yes | [BID-06-W2-bid-PT-SNEK-100000-at-15pct-pool-A4-tx-651bbd51](screenshots/05-bids-place/BID-06-W2-bid-PT-SNEK-100000-at-15pct-pool-A4-tx-651bbd51) |
| BID-07 | Wallet 2 places a bid of 100,000,000 lovelace (100 ADA) on PT ADA (pool A5) at 12% | yes | [BID-07-W2-bid-PT-ADA-100M-at-12pct-pool-A5-tx-0c50ce8e](screenshots/05-bids-place/BID-07-W2-bid-PT-ADA-100M-at-12pct-pool-A5-tx-0c50ce8e) |
| BID-08 | Wallet 1 places a bid of 150,000,000 lovelace (150 ADA) on PT ADA (pool B1) at 14% | yes | [BID-08-W1-bid-PT-ADA-150M-at-14pct-pool-B1-tx-aec75a1a](screenshots/05-bids-place/BID-08-W1-bid-PT-ADA-150M-at-14pct-pool-B1-tx-aec75a1a) |
| BID-09 | Wallet 1 places a bid of 250,000,000 lovelace (250 ADA) on PT ADA (pool B1) at 17% | yes | [BID-09-W1-bid-PT-ADA-250M-at-17pct-pool-B1-tx-b57ae67b](screenshots/05-bids-place/BID-09-W1-bid-PT-ADA-250M-at-17pct-pool-B1-tx-b57ae67b) |
| BID-10 | Wallet 1 places a bid of 15,000,000,000 USDC units (150 USDC) on PT USDC (pool B2) at 13% | yes | [BID-10-W1-bid-PT-USDC-15B-at-13pct-pool-B2-tx-700c924e](screenshots/05-bids-place/BID-10-W1-bid-PT-USDC-15B-at-13pct-pool-B2-tx-700c924e) |
| BID-11 | Wallet 1 places a bid of 150,000,000 DJED units (150 DJED) on PT DJED (pool B3) at 15% | yes | [BID-11-W1-bid-PT-DJED-150M-at-15pct-pool-B3-tx-6ecbbaff](screenshots/05-bids-place/BID-11-W1-bid-PT-DJED-150M-at-15pct-pool-B3-tx-6ecbbaff) |
| BID-12 | Wallet 1 places a bid of 100,000,000 lovelace (100 ADA) on PT ADA (pool B1) at 20% | yes | [BID-12-W1-bid-PT-ADA-100M-at-20pct-pool-B1-tx-7cea3e50](screenshots/05-bids-place/BID-12-W1-bid-PT-ADA-100M-at-20pct-pool-B1-tx-7cea3e50) |
| BID-13 | Wallet 1 places a bid of 10,000,000,000 USDC units (100 USDC) on PT USDC (pool B5) at 12% | yes | [BID-13-W1-bid-PT-USDC-10B-at-12pct-pool-B5-tx-3e57e4a8](screenshots/05-bids-place/BID-13-W1-bid-PT-USDC-10B-at-12pct-pool-B5-tx-3e57e4a8) |
| BID-14 | Wallet 1 places a bid of 50,000,000 DJED units (50 DJED) on PT DJED (pool B3) at 25% | yes | [BID-14-W1-bid-PT-DJED-50M-at-25pct-pool-B3-tx-7c7e4a8f](screenshots/05-bids-place/BID-14-W1-bid-PT-DJED-50M-at-25pct-pool-B3-tx-7c7e4a8f) |
| BID-15 | Wallet 1 places a bid of 40,000,000 DJED units (40 DJED) on PT DJED (pool B3) at 16% | yes | [BID-15-W1-bid-PT-DJED-40M-at-16pct-pool-B3-tx-b6bf4be0](screenshots/05-bids-place/BID-15-W1-bid-PT-DJED-40M-at-16pct-pool-B3-tx-b6bf4be0) |
| BID-16 | Wallet 1 places a bid of 40,000,000 DJED units (40 DJED) on PT DJED (pool B3) at 17% | yes | [BID-16-W1-bid-PT-DJED-40M-at-17pct-pool-B3-tx-010bc8af](screenshots/05-bids-place/BID-16-W1-bid-PT-DJED-40M-at-17pct-pool-B3-tx-010bc8af) |
| BID-17 | Wallet 1 places a bid of 40,000,000 DJED units (40 DJED) on PT DJED (pool B3) at 18% | yes | [BID-17-W1-bid-PT-DJED-40M-at-18pct-pool-B3-tx-cd624b60](screenshots/05-bids-place/BID-17-W1-bid-PT-DJED-40M-at-18pct-pool-B3-tx-cd624b60) |
| BID-18 | Wallet 1 places a bid of 40,000,000 DJED units (40 DJED) on PT DJED (pool B3) at 19% | yes | [BID-18-W1-bid-PT-DJED-40M-at-19pct-pool-B3-tx-159ee4d4](screenshots/05-bids-place/BID-18-W1-bid-PT-DJED-40M-at-19pct-pool-B3-tx-159ee4d4) |

## 06 · Update or cancel bids

| ID | What it shows | Signature | Folder |
|---|---|---|---|
| CHG-BID-01 | Wallet 1 updates bid BID-09 (pool B1) from 250,000,000 lovelace at 17% to 200,000,000 lovelace at 16% | yes | [CHG-BID-01-W1-update-BID-09-amount-250M-to-200M-and-yield-17-to-16pct-tx-2e2729d8](screenshots/06-bids-update-cancel/CHG-BID-01-W1-update-BID-09-amount-250M-to-200M-and-yield-17-to-16pct-tx-2e2729d8) |
| CHG-BID-02 | Wallet 1 updates bid BID-10 (pool B2) from 13% to 15%, the amount stays 15,000,000,000 USDC units | yes | [CHG-BID-02-W1-update-BID-10-yield-only-13-to-15pct-tx-81abed40](screenshots/06-bids-update-cancel/CHG-BID-02-W1-update-BID-10-yield-only-13-to-15pct-tx-81abed40) |
| CHG-BID-03 | Wallet 1 updates bid BID-11 (pool B3) from 150,000,000 to 200,000,000 DJED units, the yield stays 15% | yes | [CHG-BID-03-W1-update-BID-11-amount-only-150M-to-200M-tx-b8bcd42d](screenshots/06-bids-update-cancel/CHG-BID-03-W1-update-BID-11-amount-only-150M-to-200M-tx-b8bcd42d) |
| CHG-BID-04 | Wallet 1 cancels bid BID-12 (pool B1, 100,000,000 lovelace); the 100 ADA and the ADA held beside it come back | yes | [CHG-BID-04-W1-cancel-BID-12-ADA-bid-100M-tx-77309b0c](screenshots/06-bids-update-cancel/CHG-BID-04-W1-cancel-BID-12-ADA-bid-100M-tx-77309b0c) |
| CHG-BID-05 | Wallet 1 cancels bid BID-14 (pool B3, 50,000,000 DJED units), a bid in a token; the 50 DJED and the 2 ADA held beside it come back, less the network fee | yes | [CHG-BID-05-W1-cancel-BID-14-token-bid-50M-DJED-tx-917a26ad](screenshots/06-bids-update-cancel/CHG-BID-05-W1-cancel-BID-14-token-bid-50M-DJED-tx-917a26ad) |
| CHG-BID-07 | Wallet 2 cancels what is left of bid BID-03 (pool A2) after SELL-02 filled part of it: the 10,948,334,003 USDC units (109.48 USDC) and the ADA held beside it return | yes | [CHG-BID-07-W2-cancel-the-tie-bid-that-SELL-02-part-filled-tx-ec79230a](screenshots/06-bids-update-cancel/CHG-BID-07-W2-cancel-the-tie-bid-that-SELL-02-part-filled-tx-ec79230a) |

## 07 · Buy: market orders against the sell orders

| ID | What it shows | Signature | Folder |
|---|---|---|---|
| BUY-01 | Wallet 2 buys 450,000,000 PT DJED with Max: one transaction fills six sell orders. Matched: ASK-07 (10.5%, the relisted order), ASK-09 (9%), ASK-10 (8%), ASK-11 (7%), ASK-12 (6%) and ASK-13 (5%), all whole | yes | [BUY-01-W2-max-buy-6-orders-in-one-tx-PT-DJED-450M-pool-A3-tx-216926e3](screenshots/07-buy-market-orders/BUY-01-W2-max-buy-6-orders-in-one-tx-PT-DJED-450M-pool-A3-tx-216926e3) |
| BUY-02 | Wallet 2 buys 10,000,000,000 PT USDC, part of ASK-04 at 11%. Matched: ASK-04 (11%) part | yes | [BUY-02-W2-part-of-order-ASK-04-PT-USDC-10B-pool-A2-tx-0e8008af](screenshots/07-buy-market-orders/BUY-02-W2-part-of-order-ASK-04-PT-USDC-10B-pool-A2-tx-0e8008af) |
| BUY-03 | Wallet 2 buys 550,000,000 PT ADA in one transaction: ASK-03 (13%) and ASK-01 (12%) whole, ASK-02 (10%) part. Matched: ASK-03 (13%) whole, ASK-01 (12%) whole, ASK-02 (10%) part | yes | [BUY-03-W2-sweep-3-orders-best-yield-first-PT-ADA-550M-pool-A1-tx-1fd54c2f](screenshots/07-buy-market-orders/BUY-03-W2-sweep-3-orders-best-yield-first-PT-ADA-550M-pool-A1-tx-1fd54c2f) |
| BUY-04 | Wallet 2 buys 5,000 PT SNEK, part of ASK-14 at 12%. Matched: ASK-14 (12%) part | yes | [BUY-04-W2-part-of-order-SNEK-keeps-more-than-minimum-PT-SNEK-5000-pool-A4-tx-fd9fa7f1](screenshots/07-buy-market-orders/BUY-04-W2-part-of-order-SNEK-keeps-more-than-minimum-PT-SNEK-5000-pool-A4-tx-fd9fa7f1) |
| BUY-05 | Wallet 2 buys 45,000,000,000 PT USDC in one transaction: the remaining 20,000,000,000 of ASK-04 (11%), then 25,000,000,000 from the two 9% orders. Matched: rest of ASK-04 (11%), ASK-05 (9%) whole, ASK-06 (9%) part | yes | [BUY-05-W2-sweep-3-orders-with-a-yield-tie-PT-USDC-45B-pool-A2-tx-4c9eb83e](screenshots/07-buy-market-orders/BUY-05-W2-sweep-3-orders-with-a-yield-tie-PT-USDC-45B-pool-A2-tx-4c9eb83e) |
| BUY-06 | Wallet 2 buys 90,000,000 PT ADA, the whole of ASK-15 (exactly the pool minimum) at 10%. Matched: ASK-15 (10%) whole | yes | [BUY-06-W2-whole-order-exactly-the-minimum-short-pool-PT-ADA-90M-pool-A5-tx-0fbabab2](screenshots/07-buy-market-orders/BUY-06-W2-whole-order-exactly-the-minimum-short-pool-PT-ADA-90M-pool-A5-tx-0fbabab2) |
| BUY-07 | Wallet 1 buys 250,000,000 PT ADA in one transaction: all of ASK-17 (11%) and all of ASK-18 (9%). Matched: ASK-17 (11%) whole, ASK-18 (9%) whole | yes | [BUY-07-W1-sweep-2-orders-the-book-is-emptied-PT-ADA-250M-pool-B1-tx-d9efcf53](screenshots/07-buy-market-orders/BUY-07-W1-sweep-2-orders-the-book-is-emptied-PT-ADA-250M-pool-B1-tx-d9efcf53) |
| BUY-08 | Wallet 1 buys 5,000,000,000 PT USDC, part of ASK-19 at 10%. Matched: ASK-19 (10%) part | yes | [BUY-08-W1-part-of-order-ASK-19-PT-USDC-5B-pool-B2-tx-22e90659](screenshots/07-buy-market-orders/BUY-08-W1-part-of-order-ASK-19-PT-USDC-5B-pool-B2-tx-22e90659) |
| BUY-09 | Wallet 1 buys 150,000,000 PT DJED, the whole of ASK-20 at 11.5%. Matched: ASK-20 (11.5%) whole | yes | [BUY-09-W1-whole-order-ASK-20-PT-DJED-150M-pool-B3-tx-55559488](screenshots/07-buy-market-orders/BUY-09-W1-whole-order-ASK-20-PT-DJED-150M-pool-B3-tx-55559488) |
| BUY-10 | Wallet 1 buys 10,000,000,000 PT USDC, the whole of ASK-22 (short pool B5) at 10%. Matched: ASK-22 (10%) whole | yes | [BUY-10-W1-whole-order-token-short-pool-PT-USDC-10B-pool-B5-tx-310bfd68](screenshots/07-buy-market-orders/BUY-10-W1-whole-order-token-short-pool-PT-USDC-10B-pool-B5-tx-310bfd68) |
| BUY-12 | Wallet 2 buys the 5,000,000,000 PT USDC left on ASK-06 (9%) after BUY-05. Matched: rest of ASK-06 (9%) | yes | [BUY-12-W2-last-USDC-order-after-the-tie-PT-USDC-5B-pool-A2-tx-7374c535](screenshots/07-buy-market-orders/BUY-12-W2-last-USDC-order-after-the-tie-PT-USDC-5B-pool-A2-tx-7374c535) |

## 08 · Sell to bids: market orders against the bids

| ID | What it shows | Signature | Folder |
|---|---|---|---|
| SELL-01 | Wallet 1 sells all its free PT ADA of pool A1 (349,999,999) to the bids with Max: BID-01 (15%) is filled out, then BID-02 (18%) takes the rest. The 88 ADA left on BID-02 is below the 90 ADA minimum, so BID-02 closes too and the 88 ADA returns to wallet 2 in the same transaction | yes | [SELL-01-W1-max-sweeps-2-bids-first-bid-filled-out-PT-ADA-pool-A1-tx-9b7d9969](screenshots/08-sell-to-bids-market-orders/SELL-01-W1-max-sweeps-2-bids-first-bid-filled-out-PT-ADA-pool-A1-tx-9b7d9969) |
| SELL-02 | Wallet 1 sells 10,000,000,000 PT USDC on pool A2, where two bids tie at 14%: it fills part of BID-03, the older one; BID-04 is untouched | yes | [SELL-02-W1-part-of-a-bid-with-a-yield-tie-PT-USDC-pool-A2-tx-e5f1e145](screenshots/08-sell-to-bids-market-orders/SELL-02-W1-part-of-a-bid-with-a-yield-tie-PT-USDC-pool-A2-tx-e5f1e145) |
| SELL-03 | Wallet 1 sells 210,000,000 PT DJED to BID-05 (16%). The 12.49 DJED left on BID-05 is below the 30 DJED minimum, so BID-05 closes and that amount returns to wallet 2 in the same transaction | yes | [SELL-03-W1-leaves-less-than-minimum-so-the-bid-closes-PT-DJED-pool-A3-tx-fb2d538f](screenshots/08-sell-to-bids-market-orders/SELL-03-W1-leaves-less-than-minimum-so-the-bid-closes-PT-DJED-pool-A3-tx-fb2d538f) |
| SELL-04 | Wallet 1 sells 40,000 PT SNEK to BID-06 (15%); 64,035 SNEK stay on BID-06 | yes | [SELL-04-W1-part-of-a-bid-SNEK-PT-SNEK-pool-A4-tx-62c81101](screenshots/08-sell-to-bids-market-orders/SELL-04-W1-part-of-a-bid-SNEK-PT-SNEK-pool-A4-tx-62c81101) |
| SELL-05 | Wallet 2 sells all its free PT ADA of pool B1 (249,999,999) to the bids with Max. Matched: BID-08 (14%) filled out, then BID-09 (16%) part-filled with 93.52 ADA; 106 ADA stays on BID-09. Wallet 2 receives 240.57 ADA, net of fees | yes | [SELL-05-W2-max-sweeps-2-bids-first-bid-filled-out-PT-ADA-pool-B1-tx-edf5844d](screenshots/08-sell-to-bids-market-orders/SELL-05-W2-max-sweeps-2-bids-first-bid-filled-out-PT-ADA-pool-B1-tx-edf5844d) |
| SELL-06 | Wallet 2 sells 329,000,000 PT DJED on pool B3, where five bids wait (15% to 19%). A sale to bids fills up to four bids in one transaction. Matched: BID-11 (15%), BID-15 (16%), BID-16 (17%) and BID-17 (18%), all filled out; BID-18 (19%) stays on the book. Wallet 2 receives 319.03 DJED | yes | [SELL-06-W2-sells-to-4-bids-max-per-transaction-PT-DJED-pool-B3-tx-91189258](screenshots/08-sell-to-bids-market-orders/SELL-06-W2-sells-to-4-bids-max-per-transaction-PT-DJED-pool-B3-tx-91189258) |
| SELL-07 | Wallet 2 sells 10,000,000,000 PT USDC to BID-10 (15%). Matched: BID-10 part; 52.59 USDC stay on the bid. Wallet 2 receives 97.12 USDC | yes | [SELL-07-W2-part-of-a-bid-USDC-PT-USDC-pool-B2-tx-61d3a50d](screenshots/08-sell-to-bids-market-orders/SELL-07-W2-part-of-a-bid-USDC-PT-USDC-pool-B2-tx-61d3a50d) |

## 09 · Order book display

| ID | What it shows | Signature | Folder |
|---|---|---|---|
| BOOK-01 | Wallet 1 shows the Market with every token | no | [BOOK-01-W1-market-all-tokens](screenshots/09-order-book-display/BOOK-01-W1-market-all-tokens) |
| BOOK-02 | Wallet 1 shows the ADA tab with three maturities: pools A1, B1 and A5 | no | [BOOK-02-W1-ADA-tab-three-maturities](screenshots/09-order-book-display/BOOK-02-W1-ADA-tab-three-maturities) |
| BOOK-03 | Wallet 1 shows the USDC tab | no | [BOOK-03-W1-USDC-tab](screenshots/09-order-book-display/BOOK-03-W1-USDC-tab) |
| BOOK-04 | Wallet 1 shows the DJED tab after CHG-BID-05, with five bids on pool B3 at five different yields: 15%, 16%, 17%, 18% and 19% | no | [BOOK-04-W1-DJED-tab-with-five-bids-on-pool-B3](screenshots/09-order-book-display/BOOK-04-W1-DJED-tab-with-five-bids-on-pool-B3) |
| BOOK-05 | Wallet 1 shows the SNEK tab | no | [BOOK-05-W1-SNEK-tab](screenshots/09-order-book-display/BOOK-05-W1-SNEK-tab) |
| BOOK-06 | Wallet 1 shows a maturity row with a sell order and a bid side by side: pool B2, a 10% sell order and a 13% bid. The arrow under the date opens a row; BOOK-03 (screenshot 01) shows the row of pool A2 opened, with its two 14% bids | no | [BOOK-06-W1-expanded-row-sell-orders-and-bids](screenshots/09-order-book-display/BOOK-06-W1-expanded-row-sell-orders-and-bids) |
| BOOK-07 | Wallet 1 shows what the Trade panel says about the best offer and the best bid | no | [BOOK-07-W1-trade-card-best-offer-and-best-bid](screenshots/09-order-book-display/BOOK-07-W1-trade-card-best-offer-and-best-bid) |
| BOOK-08 | Wallet 1 shows pool A1 before and after ASK-03 was updated from 8% to 13% | no | [BOOK-08-W1-sell-order-re-ranks-after-an-update](screenshots/09-order-book-display/BOOK-08-W1-sell-order-re-ranks-after-an-update) |
| BOOK-09 | Wallet 2 shows pool A1 before and after BUY-03 swept three orders | no | [BOOK-09-W2-book-before-and-after-a-sweep](screenshots/09-order-book-display/BOOK-09-W2-book-before-and-after-a-sweep) |

## 10 · Price and fees

| ID | What it shows | Signature | Folder |
|---|---|---|---|
| PRICE-01 | Wallet 2 compares the price of PT ADA at the same 10% yield on pool A1 (2 days left: 100,000,000 PT for 92.92 ADA) and on pool A5 (matures the same day: 90,000,000 PT for 89.36 ADA). On pool A1 a buy of 90,000,000 PT is lowered to 10,000,000 PT, so that 90 ADA, the minimum, stays on ASK-02 | no | [PRICE-01-W2-same-yield-different-time-to-maturity](screenshots/10-price-and-fees/PRICE-01-W2-same-yield-different-time-to-maturity) |
| PRICE-02 | Wallet 2 quotes ASK-14 (12%) twice. First: 5,000 PT SNEK for 4,556 SNEK (0.9112 SNEK per PT). Later the same day: the 40,000 PT left for 36,950 SNEK (0.9238 SNEK per PT). Same yield, closer to maturity, higher price. Wallet 1 cannot quote it: ASK-14 is its own order | no | [PRICE-02-W1-W2-same-order-quoted-twice](screenshots/10-price-and-fees/PRICE-02-W1-W2-same-order-quoted-twice) |
| PRICE-03 | The Buy dialog of BUY-01 (wallet 2) shows a Fee of 0.8393 DJED on a payment of about 420 DJED: 0.2% of the price. A Sell dialog of wallet 1 (349,999,999 PT ADA to two bids) shows a Fee of 0.3114 ADA: 0.1% of the price, about 311 ADA | no | [PRICE-03-W1-W2-fees-0-2-percent-buyer-0-1-percent-seller](screenshots/10-price-and-fees/PRICE-03-W1-W2-fees-0-2-percent-buyer-0-1-percent-seller) |

## 11 · Trade history

| ID | What it shows | Signature | Folder |
|---|---|---|---|
| HIST-01 | Each wallet shows its own history of sell orders, role All: what it sold and what it bought, newest first (30 trades for each wallet, including earlier trades these wallets made before this milestone) | no | [HIST-01-W1-W2-sell-orders-history-all-of-the-wallet](screenshots/11-trade-history/HIST-01-W1-W2-sell-orders-history-all-of-the-wallet) |
| HIST-02 | Each wallet filters the sell-order history by I sold and I bought: wallet 1 shows 20 and 10 trades, wallet 2 shows 10 and 20, including earlier trades made before this milestone | no | [HIST-02-W1-W2-sell-orders-history-i-sold-and-i-bought](screenshots/11-trade-history/HIST-02-W1-W2-sell-orders-history-i-sold-and-i-bought) |
| HIST-03 | Each wallet shows its own history of bid fills, role All: what it sold into bids and what its bids bought (12 trades for each wallet: the 12 bid fills of SELL-01 to SELL-07) | no | [HIST-03-W1-W2-bid-fills-history-all-of-the-wallet](screenshots/11-trade-history/HIST-03-W1-W2-bid-fills-history-all-of-the-wallet) |
| HIST-04 | Each wallet filters the bid-fill history by role: wallet 1 shows 5 sold and 7 bought, wallet 2 shows 7 sold and 5 bought | no | [HIST-04-W1-W2-bid-fills-history-i-sold-and-i-bought](screenshots/11-trade-history/HIST-04-W1-W2-bid-fills-history-i-sold-and-i-bought) |
| HIST-05 | Each wallet shows the time and the maturity (date and hour) of each fill | no | [HIST-05-W1-W2-time-and-maturity-of-each-fill](screenshots/11-trade-history/HIST-05-W1-W2-time-and-maturity-of-each-fill) |
| HIST-06 | Each wallet shows a filled-out ADA bid as “≤ 150 ADA” (BID-08 in SELL-05); the tooltip says the bid’s change cannot be told apart on-chain, so this is the most it could have spent | no | [HIST-06-W1-W2-filled-out-bid-shows-at-most-and-its-note](screenshots/11-trade-history/HIST-06-W1-W2-filled-out-bid-shows-at-most-and-its-note) |
| HIST-07 | Each wallet points at a fill’s explorer link: the tooltip gives the fee (0.2917 USDC for SELL-07) and the transaction hash it opens | no | [HIST-07-W1-W2-explorer-link-and-fee-tooltip](screenshots/11-trade-history/HIST-07-W1-W2-explorer-link-and-fee-tooltip) |
| HIST-08 | Wallet 1 keeps its History page (Buy orders, All) open in one tab and sells 10,000,000,000 PT USDC of pool A2 to BID-04 (14%) in another. About 30 seconds after it returns to the History tab, the new row appears without a reload and the count goes from 12 to 13 trades. Matched: BID-04 (14%) part; 105.29 USDC stay on the bid | yes | [HIST-08-W1-history-updates-by-itself-tx-241211ad](screenshots/11-trade-history/HIST-08-W1-history-updates-by-itself-tx-241211ad) |
| HIST-09 | Wallet 1 shows the history before and after SELL-01 | no | [HIST-09-W1-history-before-and-after-one-trade](screenshots/11-trade-history/HIST-09-W1-history-before-and-after-one-trade) |
| HIST-10 | Each wallet shows the second page of the history: a page holds 20 rows, page 2 reads *Showing 21–30 of 30 trades*, including earlier trades made before this milestone | no | [HIST-10-W1-W2-second-page-of-the-history](screenshots/11-trade-history/HIST-10-W1-W2-second-page-of-the-history) |

## 12 · Matured pools and redeem

| ID | What it shows | Signature | Folder |
|---|---|---|---|
| MAT-01 | Wallet 2 cancels bid BID-07 (100 ADA at 12%) on pool A5 after the pool matured; the dialog says *This market has matured, so the bid can no longer fill*. A matured bid shows only the cancel icon. Wallet 2 receives 101.68 ADA, net of the network fee | yes | [MAT-01-W2-cancel-BID-07-on-a-matured-pool-A5-tx-3dd70ae4](screenshots/12-matured-pools-and-redeem/MAT-01-W2-cancel-BID-07-on-a-matured-pool-A5-tx-3dd70ae4) |
| MAT-02 | Wallet 2 redeems the 90,000,000 PT ADA of the matured pool A5 that it bought in BUY-06. The popup shows *Total redeem 90 ADA*; the wallet receives 3,878.492574 qAda, the form in which pool A5 holds its ADA | yes | [MAT-02-W2-redeem-PT-ADA-pool-A5-bought-earlier-tx-b3566a49](screenshots/12-matured-pools-and-redeem/MAT-02-W2-redeem-PT-ADA-pool-A5-bought-earlier-tx-b3566a49) |
| MAT-03 | Wallet 2 redeems the 19,999,999,999 PT USDC it still holds of its own matured pool B5 and receives 200 USDC | yes | [MAT-03-W2-redeem-PT-USDC-pool-B5-own-pool-tx-a13edc09](screenshots/12-matured-pools-and-redeem/MAT-03-W2-redeem-PT-USDC-pool-B5-own-pool-tx-a13edc09) |
| MAT-04 | Wallet 1 cancels bid BID-13 (100 USDC at 12%) on pool B5 after the pool matured; a bid in a token. The 100 USDC and the ADA held beside it return | yes | [MAT-04-W1-cancel-BID-13-USDC-bid-on-a-matured-pool-B5-tx-42e6bb0b](screenshots/12-matured-pools-and-redeem/MAT-04-W1-cancel-BID-13-USDC-bid-on-a-matured-pool-B5-tx-42e6bb0b) |
| MAT-05 | Wallet 1 redeems all its PT ADA of the matured pool A5 while ASK-16 (150,000,000 PT at 9%) is still listed. The popup says *Withdrawn from your order in this transaction*: the order is withdrawn and redeemed in the same transaction, 410 ADA in total. Wallet 1 receives 413.31 ADA, net of the network fee | yes | [MAT-05-W1-redeem-PT-ADA-pool-A5-with-the-order-still-listed-tx-85eb6f9a](screenshots/12-matured-pools-and-redeem/MAT-05-W1-redeem-PT-ADA-pool-A5-with-the-order-still-listed-tx-85eb6f9a) |
| MAT-06 | Wallet 1 redeems the 10,000,000,000 PT USDC of the matured pool B5 that it bought in BUY-10 and receives 100 USDC | yes | [MAT-06-W1-redeem-PT-USDC-pool-B5-bought-earlier-tx-cd6868b7](screenshots/12-matured-pools-and-redeem/MAT-06-W1-redeem-PT-USDC-pool-B5-bought-earlier-tx-cd6868b7) |

## 13 · Blocked actions (no transaction)

| ID | What it shows | Signature | Folder |
|---|---|---|---|
| BLOCK-01 | Wallet 1 tries to list 50,000,000 PT ADA on pool A1, below the 90 ADA minimum | no | [BLOCK-01-W1-list-below-pool-minimum](screenshots/13-blocked-actions/BLOCK-01-W1-list-below-pool-minimum) |
| BLOCK-02 | Wallet 2 tries to list 20,000 PT SNEK on pool B4 while only 9,999 are free: the amount is set back to the Max of 9,999, the dialog says *Minimum value to sell is 37,313 SNEK* and **List** stays disabled | no | [BLOCK-02-W2-list-more-PT-than-held](screenshots/13-blocked-actions/BLOCK-02-W2-list-more-PT-than-held) |
| BLOCK-03 | Wallet 2 tries to bid 10,000,000 lovelace (10 ADA) at 15% on pool A1, which would buy less than the 90 ADA minimum | no | [BLOCK-03-W2-bid-below-pool-minimum](screenshots/13-blocked-actions/BLOCK-03-W2-bid-below-pool-minimum) |
| BLOCK-04 | Wallet 2 types 10,000 PT SNEK on ASK-14, which would leave 35,000, below the 37,313 minimum: the app does not block, it lowers the buy to 7,687 PT so that exactly 37,313 stays on the order | no | [BLOCK-04-W2-buy-that-would-leave-less-than-the-minimum](screenshots/13-blocked-actions/BLOCK-04-W2-buy-that-would-leave-less-than-the-minimum) |
| BLOCK-05 | Wallet 1 opens Update on BID-08 and changes nothing: **Update** stays disabled | no | [BLOCK-05-W1-update-bid-with-nothing-changed](screenshots/13-blocked-actions/BLOCK-05-W1-update-bid-with-nothing-changed) |
| BLOCK-06 | Wallet 1 looks at pool A1 where the only sell order left is its own ASK-02: **Buy PT** is disabled, and clicking the order opens *Update Sell Order*, not a buy | no | [BLOCK-06-W1-buy-from-your-own-sell-order](screenshots/13-blocked-actions/BLOCK-06-W1-buy-from-your-own-sell-order) |
| BLOCK-07 | Wallet 1 looks at pool B1 where all the bids are its own: clicking a bid opens *Update Bid*, not a sale | no | [BLOCK-07-W1-sell-to-bids-when-every-bid-is-your-own](screenshots/13-blocked-actions/BLOCK-07-W1-sell-to-bids-when-every-bid-is-your-own) |
| BLOCK-08 | Wallet 1 opens Sell PT SNEK while holding no PT of pool B4: the Token list only offers pools whose PT the wallet holds, so pool B4 cannot be chosen (no message) | no | [BLOCK-08-W1-sell-with-no-PT-of-that-pool](screenshots/13-blocked-actions/BLOCK-08-W1-sell-with-no-PT-of-that-pool) |
| BLOCK-09 | Wallet 1 tries to sell 500 USDC of PT on pool A2 while holding about 400: the dialog says *More than the 39.99B pUSDC this wallet has free to sell* and **Sell** stays disabled | no | [BLOCK-09-W1-sell-to-bids-more-than-held](screenshots/13-blocked-actions/BLOCK-09-W1-sell-to-bids-more-than-held) |
| BLOCK-10 | Wallet 1 tries to place a bid with a 0% yield: the dialog says *Enter an APY above 0%* and **Place bid** stays disabled | no | [BLOCK-10-W1-bid-with-zero-yield](screenshots/13-blocked-actions/BLOCK-10-W1-bid-with-zero-yield) |
| BLOCK-11 | Wallet 2 opens **Place a bid** after pool A5 matured: pool A5 is no longer in the Token list, so no bid can be placed on it | no | [BLOCK-11-W2-bid-on-a-matured-pool](screenshots/13-blocked-actions/BLOCK-11-W2-bid-on-a-matured-pool) |
| BLOCK-12 | Wallet 1 opens **Sell PT ADA** after pool A5 matured: pool A5 is no longer in the Token list, so its PT cannot be listed. In My Account its row carries the *redeemable* tag and offers Redeem instead | no | [BLOCK-12-W1-list-a-matured-PT](screenshots/13-blocked-actions/BLOCK-12-W1-list-a-matured-PT) |
| BLOCK-13 | Wallet 1 tries to sell 1,000 PT ADA to the bids: the dialog says *This sale is worth less than the ADA its outputs must carry and the network fee* and **Sell** stays disabled | no | [BLOCK-13-W1-sell-to-bids-a-tiny-amount](screenshots/13-blocked-actions/BLOCK-13-W1-sell-to-bids-a-tiny-amount) |

## 14 · My Account

| ID | What it shows | Signature | Folder |
|---|---|---|---|
| ACC-01 | Each wallet shows the PT it holds and the PT it has listed for sale (wallet 1: 19 positions; wallet 2: 15 positions, with ASK-21 and the rest of ASK-19 on sale) | no | [ACC-01-W1-W2-holdings-and-listed-for-sale](screenshots/14-my-account/ACC-01-W1-W2-holdings-and-listed-for-sale) |
| ACC-02 | Each wallet shows its My bids list: wallet 1 has 5 bids, wallet 2 has 3; a bid on a matured pool carries the *matured* tag and only the cancel icon | no | [ACC-02-W1-W2-my-bids-list](screenshots/14-my-account/ACC-02-W1-W2-my-bids-list) |
| ACC-03 | Each wallet shows its matured pools with the *redeemable* tag and the Redeem icon before redeeming. With PT still on sale, the tooltip reads *Redeem — the PT on sale is withdrawn in the same transaction* | no | [ACC-03-W1-W2-matured-rows-with-the-redeem-icon](screenshots/14-my-account/ACC-03-W1-W2-matured-rows-with-the-redeem-icon) |

## Notes

- The folder of a case with a transaction ends with `-tx-` and the first 8 characters of its hash.
