We are submitting the evidence for Milestone 2, *Implement Sell/Buy Order Creation screen*. In the app the product is called **Zero Coupon**. It runs on the Cardano **Preview** testnet.

- Testnet app: https://app.zerocoupon.site
- Evidence folder: https://github.com/haiphan1309/Catalyst/tree/main/milestone-2

A. Output: Deployed Testnet DEX interface with Sell/Buy Order Creation functionality.
Acceptance criteria: Users can connect a Testnet Eternl wallet to the DEX interface and submit buy/sell orders of Zero-Coupon Bonds successfully.
Evidence:
- Testnet URL: https://app.zerocoupon.site
- Screen recordings of every action, from the first click to the confirmed transaction, with the Eternl signing window visible: https://github.com/haiphan1309/Catalyst/tree/main/milestone-2/videos
- Screenshots of every step: https://github.com/haiphan1309/Catalyst/tree/main/milestone-2/screenshots
- All recordings, screenshots and transactions were made by our team.
- A buy is filled straight away against the sell orders on the book. The order book's *Buy order* column is part of Milestone 3.

B. Output: Smart contract logic enabling creation of Zero-Coupon Bond orders on-chain.
Acceptance criteria: At least 10 Sell/Buy orders are successfully created and visible on-chain with transaction hashes viewable in a Cardano Testnet explorer.
Evidence:
- 17 orders created from the app on 29 September 2026 with two Eternl wallets: 9 sell orders and 8 buy orders, plus 4 updates and 2 cancels. Full table with the time, block, amounts and screenshots of each: https://github.com/haiphan1309/Catalyst/blob/main/milestone-2/TRANSACTIONS.md
- All 23 transactions carry the app's message under Cardano metadata label 674: "Bond DEX: Create Ask Order", "Bond DEX: Buy Ask Orders", "Bond DEX: Update Ask Order" or "Bond DEX: Cancel Ask Order".
- Each sell order locks its PT at the order contract. Each buy, update and cancel spends the order there, and the chain accepted every one of these contract runs (valid_contract = true).
- For every buy, the price paid equals the order's asking yield applied to the time left to maturity, to the smallest unit, and the fees are exactly 0.2% (buyer) and 0.1% (seller) of that price.

Sell orders:
- S1: wallet 1 lists 200,000,000 PT ADA (200 ADA at maturity) at 12%: https://preview.cardanoscan.io/transaction/6a6a404c835b67847b0557f9c76534c6a4ff035a2d2c80e47987caa0e4a20844
- S2: wallet 1 lists 50,000,000 PT DJED (50 DJED at maturity) at 14%: https://preview.cardanoscan.io/transaction/3592818b837234a4184a7b8f9a832e3075d927e80e5437386cc6fd798e0fe344
- S3: wallet 1 lists 10,000,000,000 PT USDC (100 USDC at maturity) at 10%: https://preview.cardanoscan.io/transaction/2d4ac0fcd654a8bce457f564a6d4057e1816ae4e29a043aba2980f975e9b3492
- S4: wallet 1 lists 40,000 PT SNEK (40,000 SNEK at maturity) at 10%: https://preview.cardanoscan.io/transaction/80f03c37aabf868ed98568cbe097c7336a3dda56919c9514bff124b56353ad33
- S5: wallet 1 lists 200,000,000 PT ADA (200 ADA at maturity) at 12%: https://preview.cardanoscan.io/transaction/782343150a817427bf938bcf12c8a60ea16898e357295f2603dba3afac6186eb
- S6: wallet 2 lists 200,000,000 PT ADA (200 ADA at maturity) at 14%: https://preview.cardanoscan.io/transaction/8b354c59668abce1ba0fcd5b570765ad03170f82061ed71f0d8417b7b3ca5ca6
- S7: wallet 2 lists 10,000,000,000 PT USDC (100 USDC at maturity) at 14%: https://preview.cardanoscan.io/transaction/399f7c42717cfe91b2055738e21f7cb8bfd1089a4a93a610d81ccd34542e6ab8
- S8: wallet 2 lists 45,000 PT SNEK (45,000 SNEK at maturity) at 14%: https://preview.cardanoscan.io/transaction/40e0da55654eb77ede34c28a17bfebee5ab78a425ac51a56299a83f25876956e
- S9: wallet 2 lists 100,000,000 PT DJED (100 DJED at maturity) at 14%: https://preview.cardanoscan.io/transaction/40c26d5ccf2946d1af9a198c6217649f69e3e131b9e8c8d6849ecc162dbeb860

Buy orders:
- B1: wallet 2 buys the whole S5 order, 200,000,000 PT ADA, for 190.204353 ADA: https://preview.cardanoscan.io/transaction/769fe7c5f0a2363ec5f10f482ead7c9ef2da7f5f6dd6bbd2c6cd05d5ce66c9c5
- B2: wallet 2 buys 4,000,000,000 PT USDC from S3 for 38.37290231 USDC; 6,000,000,000 stay on the book: https://preview.cardanoscan.io/transaction/b8e756296c278877f1004a17aadd36b2bea761fbf02264ef942bf62b13147cdd
- B3: wallet 2 buys the whole S4 order, 40,000 PT SNEK, for 38,381 SNEK: https://preview.cardanoscan.io/transaction/13cef99c6bdb4c35537238a2c5256e336f26f00bdbe5fab02e443cb582bbcdc8
- B4: wallet 2 buys 15,000,000 PT DJED from S2 for 14.154353 DJED; 35,000,000 stay on the book: https://preview.cardanoscan.io/transaction/aa406828a52dab4cc03f31118a6b8fccf6e1e8b0b2f5bbcfa86e08c2d75fdf5b
- B5: wallet 1 buys the whole S6 order, 200,000,000 PT ADA, for 189.147917 ADA: https://preview.cardanoscan.io/transaction/a7f72029a1c328011b51d0f5b086ba3a2ac314a09d9297592b9bbd1b5e456fcd
- B6: wallet 1 buys 3,000,000,000 PT USDC from S7 for 28.37444158 USDC; 7,000,000,000 stay on the book: https://preview.cardanoscan.io/transaction/ea6793f62a413745c427461a50ca5aaf3ec5b25ff3d123ec8962b10525b76169
- B7: wallet 1 buys 5,000 PT SNEK from S8 for 4,731 SNEK; 40,000 stay on the book: https://preview.cardanoscan.io/transaction/83075bfa750b32e0a736b3209c6430a028cf25e9094ed6d8d683c6cb9cd8991d
- B8: wallet 1 buys the whole S9 order, 100,000,000 PT DJED, for 94.610779 DJED: https://preview.cardanoscan.io/transaction/0a37987ae86d04ca2808df71aa370570c0470b96768c6c8301cf7316c6c661cf

Updates and cancels:
- U1: wallet 1 changes S1 from 200,000,000 PT ADA at 12% to 100,000,000 PT ADA at 9%: https://preview.cardanoscan.io/transaction/88022256f626a8e10bb0b99611a3303eeed4e09eb9325e1b242fbc3fd9f36c8a
- U2: wallet 1 changes the same order to 11%: https://preview.cardanoscan.io/transaction/dfd489a21c16ace3d52f4c4875810485dd335cd01feedd9fe01cb38e2ba8e138
- C1: wallet 1 cancels it; the PT goes back to wallet 1: https://preview.cardanoscan.io/transaction/b399a2038d01e80654a6f8d146cabf49ab6009b63058addc4af6d50cfc75ef46
- U3: wallet 2 changes S7 — 7,000,000,000 PT USDC left after the partial buy B6 — to 5,000,000,000 PT USDC at 12%: https://preview.cardanoscan.io/transaction/d3befd558aa413c5f2760f0b5e44b7b4e154bb9bfb8a9c36bf7eae55344705f2
- U4: wallet 2 changes the same order to 13%: https://preview.cardanoscan.io/transaction/d46bcffb9a8909bafcb6d6bdf471e712823660490c48fff2f10a6d862824f900
- C2: wallet 2 cancels it; the PT goes back to wallet 2: https://preview.cardanoscan.io/transaction/f47f6a5de6d4200b61270cde6fb1a40ab00c56c29fd06774fc31cc3e635c2574

C. Output: Public user guide for Sell/Buy workflow.
Acceptance criteria: User guide enables any community tester to complete the workflow without developer assistance.
Evidence:
- User guide, with a screenshot for every step: https://github.com/haiphan1309/Catalyst/blob/main/milestone-2/USER_GUIDE.md
- The guide covers:
  - setting up Eternl on Preview, with test ADA and collateral;
  - connecting the wallet;
  - seeing the PT held;
  - creating, updating and cancelling a sell order;
  - buying a whole order or part of one;
  - checking each transaction on Cardanoscan.
- Two public test wallets, already holding PT and test tokens: https://github.com/haiphan1309/Catalyst/blob/main/milestone-2/TEST_WALLETS.md
- On Preview, bonds mature one day after their pool is created, and a year counts as 36.5 hours, so even a one-day bond trades at a clear discount.
