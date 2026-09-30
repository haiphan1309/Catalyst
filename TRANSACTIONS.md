# On-chain orders — Cardano Preview

This page lists every transaction made for this milestone on 29 September 2026: **9 sell orders**, **8 buy orders**, **4 updates** and **2 cancels**. All were built by https://app.zerocoupon.site and signed in Eternl by one of the two test wallets. Every figure below is read from the chain; open any hash on Cardanoscan (Preview) to check it.

| Wallet | Address |
|---|---|
| Wallet 1 | `addr_test1qq5d0puzqsp70uut68m9kj7djwfhq2gy88gxj5g6mke8f7qudwk64wkcpnsyu9mcg2nu3kxkuyspwrh5x5ghj0u94ucsvz7r3n` |
| Wallet 2 | `addr_test1qz8r8mdqunhr5cl0d0936274upx2qwuhhcnrfurxudxuxlj62s4ndurtq2k8pf8laeqzpgnn9rcgrp8wpae58wnsa3dqgkwfy0` |

Each *Evidence* folder holds the app screenshots of that transaction, the wallet's own record in Eternl, and its Cardanoscan page. Times are UTC.

## What holds for all 23 transactions

- Each carries the app's message under Cardano metadata label 674: *Bond DEX: Create Ask Order*, *Bond DEX: Buy Ask Orders*, *Bond DEX: Update Ask Order* or *Bond DEX: Cancel Ask Order*.
- Every sell order locks its PT, with 2 ADA, at the order contract. The contract address starts with `addr_test1zq4qng…` and ends with the seller's own staking credential, so each wallet's open orders sit at one address — open [wallet 1's orders](https://preview.cardanoscan.io/address/addr_test1zq4qngypk7czqwtf23jpe4ucukrtm72z4jjrv9rty0tewucudwk64wkcpnsyu9mcg2nu3kxkuyspwrh5x5ghj0u94ucs7uvhup) or [wallet 2's orders](https://preview.cardanoscan.io/address/addr_test1zq4qngypk7czqwtf23jpe4ucukrtm72z4jjrv9rty0tewu662s4ndurtq2k8pf8laeqzpgnn9rcgrp8wpae58wnsa3dq4k6kna) on Cardanoscan. The asking yield is stored on chain with the order.
- Every buy, update and cancel spends that order at the contract, and the chain accepted every one of these contract runs (`valid_contract = true`).
- For every buy, the price equals the order's asking yield applied to the time left to maturity, to the smallest unit. The buyer fee is 0.2% and the seller fee 0.1% of that price.

## Sell orders — 9

| # | Time (UTC) | Block | Wallet | PT | Amount (PT) | Worth at maturity | Asking yield | Transaction | Evidence |
|---|---|---|---|---|---|---|---|---|---|
| S1 | 04:15:30 | 4,707,229 | 1 | PT ADA | 200,000,000 | 200 ADA | 12% | [6a6a404c…a20844](https://preview.cardanoscan.io/transaction/6a6a404c835b67847b0557f9c76534c6a4ff035a2d2c80e47987caa0e4a20844) | [screenshots](screenshots/02-wallet-1-addr_test1qq5d0/03-create-sell-orders/S1-sell-PT-ADA-200M-at-12pct-tx-6a6a404c/) |
| S2 | 04:19:53 | 4,707,238 | 1 | PT DJED | 50,000,000 | 50 DJED | 14% | [3592818b…0fe344](https://preview.cardanoscan.io/transaction/3592818b837234a4184a7b8f9a832e3075d927e80e5437386cc6fd798e0fe344) | [screenshots](screenshots/02-wallet-1-addr_test1qq5d0/03-create-sell-orders/S2-sell-PT-DJED-50M-at-14pct-tx-3592818b/) |
| S3 | 04:32:05 | 4,707,259 | 1 | PT USDC | 10,000,000,000 | 100 USDC | 10% | [2d4ac0fc…9b3492](https://preview.cardanoscan.io/transaction/2d4ac0fcd654a8bce457f564a6d4057e1816ae4e29a043aba2980f975e9b3492) | [screenshots](screenshots/02-wallet-1-addr_test1qq5d0/03-create-sell-orders/S3-sell-PT-USDC-10B-at-10pct-tx-2d4ac0fc/) |
| S4 | 04:33:46 | 4,707,265 | 1 | PT SNEK | 40,000 | 40,000 SNEK | 10% | [80f03c37…53ad33](https://preview.cardanoscan.io/transaction/80f03c37aabf868ed98568cbe097c7336a3dda56919c9514bff124b56353ad33) | [screenshots](screenshots/02-wallet-1-addr_test1qq5d0/03-create-sell-orders/S4-sell-PT-SNEK-40000-at-10pct-tx-80f03c37/) |
| S5 | 07:25:07 | 4,707,608 | 1 | PT ADA | 200,000,000 | 200 ADA | 12% | [78234315…6186eb](https://preview.cardanoscan.io/transaction/782343150a817427bf938bcf12c8a60ea16898e357295f2603dba3afac6186eb) | [screenshots](screenshots/02-wallet-1-addr_test1qq5d0/03-create-sell-orders/S5-sell-PT-ADA-200M-at-12pct-tx-78234315/) |
| S6 | 07:59:55 | 4,707,675 | 2 | PT ADA | 200,000,000 | 200 ADA | 14% | [8b354c59…ca5ca6](https://preview.cardanoscan.io/transaction/8b354c59668abce1ba0fcd5b570765ad03170f82061ed71f0d8417b7b3ca5ca6) | [screenshots](screenshots/03-wallet-2-addr_test1qz8r8/03-create-sell-orders/S6-sell-PT-ADA-200M-at-14pct-tx-8b354c59/) |
| S7 | 08:01:40 | 4,707,677 | 2 | PT USDC | 10,000,000,000 | 100 USDC | 14% | [399f7c42…2e6ab8](https://preview.cardanoscan.io/transaction/399f7c42717cfe91b2055738e21f7cb8bfd1089a4a93a610d81ccd34542e6ab8) | [screenshots](screenshots/03-wallet-2-addr_test1qz8r8/03-create-sell-orders/S7-sell-PT-USDC-10B-at-14pct-tx-399f7c42/) |
| S8 | 08:04:12 | 4,707,684 | 2 | PT SNEK | 45,000 | 45,000 SNEK | 14% | [40e0da55…76956e](https://preview.cardanoscan.io/transaction/40e0da55654eb77ede34c28a17bfebee5ab78a425ac51a56299a83f25876956e) | [screenshots](screenshots/03-wallet-2-addr_test1qz8r8/03-create-sell-orders/S8-sell-PT-SNEK-45000-at-14pct-tx-40e0da55/) |
| S9 | 08:05:41 | 4,707,687 | 2 | PT DJED | 100,000,000 | 100 DJED | 14% | [40c26d5c…beb860](https://preview.cardanoscan.io/transaction/40c26d5ccf2946d1af9a198c6217649f69e3e131b9e8c8d6849ecc162dbeb860) | [screenshots](screenshots/03-wallet-2-addr_test1qz8r8/03-create-sell-orders/S9-sell-PT-DJED-100M-at-14pct-tx-40c26d5c/) |

S1 and S7 were each later updated twice and then cancelled (see [Updates and cancels](#updates-and-cancels)). S6 resells the 200,000,000 PT ADA that wallet 2 bought in B1.

## Buy orders — 8

| # | Time (UTC) | Block | Buyer | Bought from | PT bought | Left on the order | Buyer paid | Seller received | Transaction | Evidence |
|---|---|---|---|---|---|---|---|---|---|---|
| B1 | 07:37:56 | 4,707,629 | 2 | S5 | 200,000,000 PT ADA | none (whole order) | 190.204353 ADA | 189.634879 ADA | [769fe7c5…66c9c5](https://preview.cardanoscan.io/transaction/769fe7c5f0a2363ec5f10f482ead7c9ef2da7f5f6dd6bbd2c6cd05d5ce66c9c5) | [screenshots](screenshots/03-wallet-2-addr_test1qz8r8/02-buy-orders/B1-buy-PT-ADA-200M-whole-order-tx-769fe7c5/) |
| B2 | 07:41:04 | 4,707,634 | 2 | S3 | 4,000,000,000 PT USDC | 6,000,000,000 | 38.37290231 USDC | 38.25801339 USDC | [b8e75629…147cdd](https://preview.cardanoscan.io/transaction/b8e756296c278877f1004a17aadd36b2bea761fbf02264ef942bf62b13147cdd) | [screenshots](screenshots/03-wallet-2-addr_test1qz8r8/02-buy-orders/B2-buy-PT-USDC-4B-part-of-order-tx-b8e75629/) |
| B3 | 07:45:18 | 4,707,645 | 2 | S4 | 40,000 PT SNEK | none (whole order) | 38,381 SNEK | 38,266 SNEK | [13cef99c…bbcdc8](https://preview.cardanoscan.io/transaction/13cef99c6bdb4c35537238a2c5256e336f26f00bdbe5fab02e443cb582bbcdc8) | [screenshots](screenshots/03-wallet-2-addr_test1qz8r8/02-buy-orders/B3-buy-PT-SNEK-40000-whole-order-tx-13cef99c/) |
| B4 | 07:47:32 | 4,707,652 | 2 | S2 | 15,000,000 PT DJED | 35,000,000 | 14.154353 DJED | 14.111974 DJED | [aa406828…5fdf5b](https://preview.cardanoscan.io/transaction/aa406828a52dab4cc03f31118a6b8fccf6e1e8b0b2f5bbcfa86e08c2d75fdf5b) | [screenshots](screenshots/03-wallet-2-addr_test1qz8r8/02-buy-orders/B4-buy-PT-DJED-15M-part-of-order-tx-aa406828/) |
| B5 | 08:24:38 | 4,707,726 | 1 | S6 | 200,000,000 PT ADA | none (whole order) | 189.147917 ADA | 188.581606 ADA | [a7f72029…456fcd](https://preview.cardanoscan.io/transaction/a7f72029a1c328011b51d0f5b086ba3a2ac314a09d9297592b9bbd1b5e456fcd) | [screenshots](screenshots/02-wallet-1-addr_test1qq5d0/05-buy-orders/B5-buy-PT-ADA-200M-whole-order-tx-a7f72029/) |
| B6 | 08:25:59 | 4,707,732 | 1 | S7 | 3,000,000,000 PT USDC | 7,000,000,000 | 28.37444158 USDC | 28.28948816 USDC | [ea6793f6…b76169](https://preview.cardanoscan.io/transaction/ea6793f62a413745c427461a50ca5aaf3ec5b25ff3d123ec8962b10525b76169) | [screenshots](screenshots/02-wallet-1-addr_test1qq5d0/05-buy-orders/B6-buy-PT-USDC-3B-part-of-order-tx-ea6793f6/) |
| B7 | 08:29:57 | 4,707,739 | 1 | S8 | 5,000 PT SNEK | 40,000 | 4,731 SNEK | 4,717 SNEK | [83075bfa…d8991d](https://preview.cardanoscan.io/transaction/83075bfa750b32e0a736b3209c6430a028cf25e9094ed6d8d683c6cb9cd8991d) | [screenshots](screenshots/02-wallet-1-addr_test1qq5d0/05-buy-orders/B7-buy-PT-SNEK-5000-part-of-order-tx-83075bfa/) |
| B8 | 08:31:33 | 4,707,744 | 1 | S9 | 100,000,000 PT DJED | none (whole order) | 94.610779 DJED | 94.327514 DJED | [0a37987a…c661cf](https://preview.cardanoscan.io/transaction/0a37987ae86d04ca2808df71aa370570c0470b96768c6c8301cf7316c6c661cf) | [screenshots](screenshots/02-wallet-1-addr_test1qq5d0/05-buy-orders/B8-buy-PT-DJED-100M-whole-order-tx-0a37987a/) |

*Buyer paid* is the price plus the 0.2% buyer fee. *Seller received* is the price minus the 0.1% seller fee; when a whole order is bought, the seller also gets back the 2 ADA the order held.

## Updates and cancels

| # | Time (UTC) | Block | Wallet | Order | Change | Transaction | Evidence |
|---|---|---|---|---|---|---|---|
| U1 | 04:51:34 | 4,707,313 | 1 | S1 | 200,000,000 → 100,000,000 PT (100,000,000 PT back to wallet 1); asking yield 12% → 9% | [88022256…f36c8a](https://preview.cardanoscan.io/transaction/88022256f626a8e10bb0b99611a3303eeed4e09eb9325e1b242fbc3fd9f36c8a) | [screenshots](screenshots/02-wallet-1-addr_test1qq5d0/04-update-and-cancel-sell-orders/U1-update-PT-ADA-to-100M-at-9pct-tx-88022256/) |
| U2 | 04:53:35 | 4,707,318 | 1 | S1, as updated by U1 | asking yield 9% → 11% | [dfd489a2…a8e138](https://preview.cardanoscan.io/transaction/dfd489a21c16ace3d52f4c4875810485dd335cd01feedd9fe01cb38e2ba8e138) | [screenshots](screenshots/02-wallet-1-addr_test1qq5d0/04-update-and-cancel-sell-orders/U2-update-PT-ADA-to-11pct-tx-dfd489a2/) |
| C1 | 04:54:52 | 4,707,322 | 1 | S1, as updated by U2 | cancelled; the 100,000,000 PT and the 2 ADA the order held back to wallet 1 | [b399a203…75ef46](https://preview.cardanoscan.io/transaction/b399a2038d01e80654a6f8d146cabf49ab6009b63058addc4af6d50cfc75ef46) | [screenshots](screenshots/02-wallet-1-addr_test1qq5d0/04-update-and-cancel-sell-orders/C1-cancel-PT-ADA-100M-tx-b399a203/) |
| U3 | 10:20:53 | 4,708,001 | 2 | S7, as left after B6 | 7,000,000,000 → 5,000,000,000 PT (2,000,000,000 PT back to wallet 2); asking yield 14% → 12% | [d3befd55…4705f2](https://preview.cardanoscan.io/transaction/d3befd558aa413c5f2760f0b5e44b7b4e154bb9bfb8a9c36bf7eae55344705f2) | [screenshots](screenshots/03-wallet-2-addr_test1qz8r8/04-update-and-cancel-sell-orders/U3-update-PT-USDC-to-5B-at-12pct-tx-d3befd55/) |
| U4 | 10:22:38 | 4,708,007 | 2 | S7, as updated by U3 | asking yield 12% → 13% | [d46bcffb…24f900](https://preview.cardanoscan.io/transaction/d46bcffb9a8909bafcb6d6bdf471e712823660490c48fff2f10a6d862824f900) | [screenshots](screenshots/03-wallet-2-addr_test1qz8r8/04-update-and-cancel-sell-orders/U4-update-PT-USDC-to-13pct-tx-d46bcffb/) |
| C2 | 10:24:22 | 4,708,011 | 2 | S7, as updated by U4 | cancelled; the 5,000,000,000 PT and the 2 ADA the order held back to wallet 2 | [f47f6a5d…5c2574](https://preview.cardanoscan.io/transaction/f47f6a5de6d4200b61270cde6fb1a40ab00c56c29fd06774fc31cc3e635c2574) | [screenshots](screenshots/03-wallet-2-addr_test1qz8r8/04-update-and-cancel-sell-orders/C2-cancel-PT-USDC-5B-tx-f47f6a5d/) |

## What the 23 transactions cover

| Dimension | Values exercised |
|---|---|
| Signing wallets | 2 — and each wallet sells, buys from the other, updates and cancels |
| PT assets | ADA · USDC · DJED · SNEK |
| Asking yields | 10% · 12% · 13% · 14% |
| Whole-order buys | 4 — B1, B3, B5, B8 |
| Partial buys, with the rest staying on the book | 4 — B2, B4, B6, B7 |
| Updates | amount and yield together (U1, U3) · yield alone (U2, U4) |
| Cancels, with the PT and the 2 ADA returned | 2 — C1, C2, one from each wallet |

## How to check a transaction

1. Open the link, or paste the hash at https://preview.cardanoscan.io.
2. The **Metadata** tab names the action. *Ask order* means sell order.
3. What each action shows on chain:
   - **Sell order:** the PT and 2 ADA move from the seller's wallet to the order contract.
   - **Buy:** the order is spent; the PT goes to the buyer and the seller is paid in the same transaction, with the fees sent to the protocol fee address. After a partial buy, the rest of the order goes back to the order contract with the same asking yield.
   - **Update:** the order is spent and replaced, in the same transaction, by an order with the new amount or yield. PT taken off the order goes back to the seller.
   - **Cancel:** the order is spent and its PT and 2 ADA go back to the seller's wallet.
