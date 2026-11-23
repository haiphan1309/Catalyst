# Zero Coupon — User Guide

**Trade zero-coupon bonds on the Cardano Preview testnet: sell orders, bids, buying, selling to bids, price matching and the trade history.**

| | |
|---|---|
| App | https://app.zerocoupon.site |
| Network | Cardano **Preview** (testnet) |
| Wallet | Eternl |
| Explorer | https://preview.cardanoscan.io |

![The Market: the order book and the Trade panel](screenshots/09-order-book-display/BOOK-02-W1-ADA-tab-three-maturities/01-app-ada-tab-a5-b1-a1.png)

---

## What you are trading

- A **zero-coupon bond** pays nothing until it matures, then pays its full face value.
- On Zero Coupon the bond is a **Principal Token (PT)**. Each PT comes from a pool of one token (ADA, USDC, DJED or SNEK). At maturity, PT is redeemed for that token one for one (a pool of ADA may pay out qAda, the form in which it holds its ADA; see MAT-02).
- A **seller** lists PT at the yield they ask. They are paid as soon as someone buys.
- A **buyer** pays less than face value today and receives the full value at maturity. The difference is the buyer's yield.
- A **bidder** puts money on the book at the yield they want and waits. A seller can sell PT to the best bid at once.

**Amounts are counted in PT units.** One PT unit is worth one smallest unit of its token:

| PT | At maturity |
|---|---|
| PT ADA | 1,000,000 PT = 1 ADA |
| PT USDC | 100,000,000 PT = 1 USDC |
| PT DJED | 1,000,000 PT = 1 DJED |
| PT SNEK | 1 PT = 1 SNEK |

Under every amount you type, the app shows what it is worth in the token, for example *~ 100 ADA*. In dialogs, *My bids* and the history, the app writes PT ADA as *pADA* (likewise pUSDC, pDJED, pSNEK).

---

## Before you start

1. **Eternl.** Install the Eternl browser extension (https://eternl.io), then create or restore a wallet.
2. **Preview network.** Switch Eternl to **Preview**. The app runs on Preview only.
3. **Test ADA.** Request test ADA for your Preview address from the Cardano testnet faucet: https://docs.cardano.org/cardano-testnets/tools/faucet
4. **Collateral.** Set up collateral in Eternl's settings. Buying, selling to bids, updating, cancelling and redeeming run a contract, and Cardano requires collateral for that.

With test ADA alone you can trade **PT ADA**, which is paid for in ADA.

**Shortcut:** restore one of the two public test wallets in [TEST_WALLETS.md](TEST_WALLETS.md). They already hold PT and test tokens, so you can skip the faucet.

---

## 1. Connect your wallet

1. Open https://app.zerocoupon.site. The **Preview** badge in the header shows the network.
2. Click **Connect Wallet** and choose **Eternl**.
3. If Eternl asks, approve the connection.

Your wallet now appears in the header.

![Connected: the wallet in the header, on Preview](screenshots/00-wallets-before-any-order/wallet-1-addr_test1qq5d0/04-app-market-all-tab.png)

---

## 2. See the PT in your wallet

Open **My Account**. It lists every PT your wallet holds, by token and maturity. The **Listed for sale** column shows how much of each PT is on sale. A page holds 10 rows.

![My Account: the PT this wallet holds](screenshots/00-wallets-before-any-order/wallet-1-addr_test1qq5d0/01-app-my-account-positions-page-1.png)

No PT yet? Buy some on the Market first (step 5). You can then sell it here.

---

## 3. Create a sell order

1. Open the sell dialog in either of two ways:
   - on **Market**, click **Sell PT** in the Trade panel;
   - in **My Account**, click **+** (*List for sale*) on the PT's row.
2. Fill in **Create Sell Order**:

   | Field | What to enter |
   |---|---|
   | **Token** | The PT to sell. |
   | **Number of PT to list for sale** | **Max** fills in all you hold. If you enter more than you hold, the amount is set back to the Max. The amount must be at least the pool's minimum. If it is lower, the dialog tells you the minimum, for example *Minimum value to sell is 90 ADA*. |
   | **Effective Fixed APY for Buyer** | The yield you offer the buyer. |

   **Expected Receive (≈ now)** shows what you would receive if the order were bought right now, after the seller fee. Your order keeps the yield you set, so its price rises as maturity approaches.
3. Click **List** and sign in Eternl.
4. A progress window follows the transaction and ends with **Transaction confirmed**. You can also open the transaction on Cardanoscan (section 12).

Your order is now in the Market order book under **Sell order**. **My Account** shows it under **Listed for sale**.

![Token: the PT in the wallet, with its maturity and balance](screenshots/13-blocked-actions/BLOCK-08-W1-sell-with-no-PT-of-that-pool/02-app-blocked-message-or-disabled-button.png)

![Below the pool's minimum, the dialog says so](screenshots/13-blocked-actions/BLOCK-02-W2-list-more-PT-than-held/02a-app-typed-20000-minimum-value-message.png)

![Create Sell Order: amount, APY and Expected Receive](screenshots/03-sell-orders-create/ASK-04-W1-sell-PT-USDC-30B-at-11pct-pool-A2-tx-78311866/02-app-sell-dialog-filled.png)

![Sign in Eternl](screenshots/03-sell-orders-create/ASK-04-W1-sell-PT-USDC-30B-at-11pct-pool-A2-tx-78311866/03-eternl-sign-transaction.png)

![Transaction confirmed](screenshots/03-sell-orders-create/ASK-04-W1-sell-PT-USDC-30B-at-11pct-pool-A2-tx-78311866/04-app-transaction-confirmed.png)

![The order in the order book](screenshots/03-sell-orders-create/ASK-04-W1-sell-PT-USDC-30B-at-11pct-pool-A2-tx-78311866/05-app-order-on-market.png)

![My Account: the PT listed for sale](screenshots/03-sell-orders-create/ASK-04-W1-sell-PT-USDC-30B-at-11pct-pool-A2-tx-78311866/06-app-my-account-listed-end-of-phase-1.png)

---

## 4. Update or cancel your sell order

**Update**

1. In **My Account**, click the pencil (*Edit order*) on the order's row. Or, on **Market**, click the yield of your own order.
2. Change the amount or the APY. **Update** stays disabled until something has changed.
3. Click **Update** and sign in Eternl.

**Cancel**

1. In **My Account**, click **×** (*Cancel order*).
2. **Cancel Sell Order** shows what returns to your wallet: the PT, plus the ADA the order held.
3. Click **Cancel order** and sign in Eternl. To keep the order, click **Keep order** instead.

![Update Sell Order: a new amount, the same APY](screenshots/04-sell-orders-update-cancel/CHG-ASK-03-W1-update-ASK-16-amount-200M-to-150M-keeps-9pct-tx-d1ebfe0d/02-app-update-dialog-filled.png)

![Sign the update in Eternl](screenshots/04-sell-orders-update-cancel/CHG-ASK-03-W1-update-ASK-16-amount-200M-to-150M-keeps-9pct-tx-d1ebfe0d/03-eternl-sign-transaction.png)

![The order with its new amount](screenshots/04-sell-orders-update-cancel/CHG-ASK-03-W1-update-ASK-16-amount-200M-to-150M-keeps-9pct-tx-d1ebfe0d/05-app-order-after.png)

![Sign the cancel in Eternl: the PT comes back](screenshots/04-sell-orders-update-cancel/CHG-ASK-02-W1-cancel-ASK-08-DJED-200M-untouched-tx-ca202e63/03-eternl-sign-transaction.png)

---

## 5. Buy: a market order against the sell orders

1. On **Market**, choose a token or **All**. Offers are grouped by maturity, with the highest yield first. The arrow under the maturity date shows every offer.
2. Click the **yield** in the row of the maturity you want to buy, with the row closed. The dialog matches the sell orders of that maturity from the highest yield down. **Buy PT** in the Trade panel opens the nearest maturity.
3. Read **Market Order**:

   | Field | What it shows |
   |---|---|
   | **Number of p… tokens to buy** (named after the token) | Starts at the whole order. Enter less to buy part of it. If what would stay on an order is below the pool's minimum, the app lowers your buy so that the minimum stays; the *Matched* line shows the amount bought. **Max** takes every sell order of that maturity. |
   | **ADA Receive Maturity** (named after the token) | What you receive at maturity, and the days until then. |
   | **Implied Yield** | Your yield if you hold to maturity. It is shown with the order(s) the buy is matched with. |
   | **Fee** | The buyer fee. |
   | **Pay** | The total you pay. |

4. Click **Buy** and sign in Eternl.
5. The progress window ends with **Transaction confirmed**.

After a whole-order buy the order leaves the book. After a partial buy, the book shows what is left. The PT you bought is in **My Account**.

On the Market your own orders open *Update*, not *Buy*. You cannot buy from yourself.

![The order book with every offer shown](screenshots/09-order-book-display/BOOK-09-W2-book-before-and-after-a-sweep/01-app-before-buy.png)

![Market: click the yield of an order to buy from it](screenshots/09-order-book-display/BOOK-09-W2-book-before-and-after-a-sweep/01a-app-before-buy-market-ada-collapsed.png)

![Market Order: buying a whole order](screenshots/07-buy-market-orders/BUY-09-W1-whole-order-ASK-20-PT-DJED-150M-pool-B3-tx-55559488/02-app-buy-dialog.png)

![Sign in Eternl](screenshots/07-buy-market-orders/BUY-09-W1-whole-order-ASK-20-PT-DJED-150M-pool-B3-tx-55559488/03-eternl-sign-transaction.png)

![Transaction confirmed](screenshots/07-buy-market-orders/BUY-09-W1-whole-order-ASK-20-PT-DJED-150M-pool-B3-tx-55559488/04-app-transaction-confirmed.png)

![The order has left the book](screenshots/07-buy-market-orders/BUY-09-W1-whole-order-ASK-20-PT-DJED-150M-pool-B3-tx-55559488/05-app-market-after-buy.png)

![Market Order: buying part of an order](screenshots/07-buy-market-orders/BUY-02-W2-part-of-order-ASK-04-PT-USDC-10B-pool-A2-tx-0e8008af/02-app-buy-dialog.png)

![The rest of the order stays on the book](screenshots/07-buy-market-orders/BUY-02-W2-part-of-order-ASK-04-PT-USDC-10B-pool-A2-tx-0e8008af/05-app-market-after-buy.png)

![My Account: PT bought on the Market](screenshots/07-buy-market-orders/BUY-09-W1-whole-order-ASK-20-PT-DJED-150M-pool-B3-tx-55559488/06-app-my-account-bought-pt.png)

---

## 6. Place a bid: a limit order

A bid is money waiting at the yield you choose. It stays on the book until a seller takes it, or until you update or cancel it.

1. On **Market**, click **Place a bid** under *Limit order* in the Trade panel.
2. Fill in **Place Bid**:

   | Field | What to enter |
   |---|---|
   | **Token** | The PT you want to buy. Read the *Matures …* line under it: one token can have several pools. |
   | **Amount to bid (raw … units)** | How much of the pool's token you put in. **Max** fills in the most you can bid. |
   | **Effective Fixed APY for You** | The yield you want. A higher yield means a lower price. |

   Under the form, the dialog shows what the bid locks and what it buys: **Bid**, **Held in addition** (an ADA bid also holds 2 ADA, which comes back when the bid closes; a bid in a token also holds 2 ADA, which comes back the same way), **You get if filled now** and **You get if filled at maturity**.
3. Click **Place bid** and sign in Eternl.
4. The bid is on the order book. **My Account** lists it under **My bids**.

![Place Bid dialog, filled in (BID-01)](screenshots/05-bids-place/BID-01-W2-bid-PT-ADA-200M-at-15pct-pool-A1-tx-d56b543e/02-app-bid-dialog-filled.png)

![The bid in My bids (BID-08)](screenshots/05-bids-place/BID-08-W1-bid-PT-ADA-150M-at-14pct-pool-B1-tx-aec75a1a/06-app-my-account-my-bids.png)

---

## 7. Sell to bids: a market order against the bids

Sell to bids is the opposite of buying: you sell PT you hold to the bids that wait on the book, and you are paid straight away.

1. On **Market**, choose the token, then click the **yield** of a bid in the row of the maturity you want to sell. You can also click **Sell to bids** under *Market order* in the Trade panel; the *Token* line shows the pool.
2. Read the **Market Order** dialog (*Sell pADA*, *Sell pUSDC*…):

   | Field | What it shows |
   |---|---|
   | **Number of p… tokens to sell** (named after the token) | What you sell. **Max** fills in the most this wallet can sell. |
   | **Receive** | What you are paid now. |
   | **Maturity** and **Days to maturity** | When the PT matures. |

3. Click **Sell** and sign in Eternl.

One sale takes up to four bids (SELL-06). A bid that your sale fills completely leaves the book. A bid that is only partly filled stays with what is left, unless that is below the pool's minimum: then the bid closes and the rest goes back to the bidder in the same transaction.

![Sell PT dialog (SELL-01)](screenshots/08-sell-to-bids-market-orders/SELL-01-W1-max-sweeps-2-bids-first-bid-filled-out-PT-ADA-pool-A1-tx-9b7d9969/02-app-sell-to-bids-dialog.png)

![The bids after the sale (SELL-01)](screenshots/08-sell-to-bids-market-orders/SELL-01-W1-max-sweeps-2-bids-first-bid-filled-out-PT-ADA-pool-A1-tx-9b7d9969/05-app-market-bids-after.png)

![One sale fills four bids; the fifth stays on the book (SELL-06)](screenshots/08-sell-to-bids-market-orders/SELL-06-W2-sells-to-4-bids-max-per-transaction-PT-DJED-pool-B3-tx-91189258/05-app-market-bids-after.png)

---

## 8. Update or cancel your bid

**Update**
1. In **My Account**, under **My bids**, click the *Update bid* icon on the bid's row.
2. Change **Amount to bid** or **Effective Fixed APY for You**. **Update** stays disabled until something has changed.
3. Click **Update** and sign in Eternl.

**Cancel**
1. In **My bids**, click the *Cancel bid* icon.
2. **Cancel Bid** shows what comes back to your wallet.
3. Click **Cancel bid** and sign in Eternl.

![Update Bid dialog (CHG-BID-01)](screenshots/06-bids-update-cancel/CHG-BID-01-W1-update-BID-09-amount-250M-to-200M-and-yield-17-to-16pct-tx-2e2729d8/02-app-update-bid-dialog-filled.png)

![Cancel Bid dialog (CHG-BID-04)](screenshots/06-bids-update-cancel/CHG-BID-04-W1-cancel-BID-12-ADA-bid-100M-tx-77309b0c/02-app-cancel-bid-dialog.png)

---

## 9. Read the order book and how orders are matched

On **Market**, the order book groups offers by maturity. In each row, **Buy order** shows the bids (*Volume* and *Yield*) and **Sell order** shows the sell orders (*Yield* and *Volume (PT)*).

- The arrow under the maturity date shows every offer of that maturity.
- Sell orders come with the highest yield first. Bids come with the lowest yield first.
- When two offers have the same yield, the one placed earlier was filled first in our tests (BUY-05, SELL-02).
- The Trade panel names the best offer and the best bid of the token you chose.
- A **buy** takes the sell order with the highest yield first, then the next, in one transaction.
- **Sell to bids** takes the bid with the lowest yield first, then the next.
- What stays on a sell order after a partial buy must be at least the pool's minimum. If it would be less, the app lowers your buy so that the minimum stays on the order.
- If what stays on a bid after a partial sale would be less than the pool's minimum, the bid closes in the same transaction and what is left returns to the bidder.
- An order keeps its yield, so its price rises as maturity gets closer.

The rules, trade by trade, are in [MATCHING.md](MATCHING.md).

![The Market with sell orders and bids (BOOK-01)](screenshots/09-order-book-display/BOOK-01-W1-market-all-tokens/01-app-market-all-tab.png)

![A maturity row opened: pool A2 with its two 14% bids (BOOK-03)](screenshots/09-order-book-display/BOOK-03-W1-USDC-tab/01-app-usdc-tab-a2-row-expanded.png)

---

## 10. The trade history

The history lists the trades of your wallet, newest first. One row is one order filled, so a single transaction can appear more than once.

1. Open **History** in the menu. Without a wallet it asks you to connect one: the history is your wallet's own.
2. Pick the book with **Sell orders** or **Buy orders**. **Sell orders** lists the fills of sell orders; **Buy orders** lists the fills of bids.
3. Narrow the list down: **All PT** picks a token, and **All**, **I sold** and **I bought** pick the side. **All** lists both of your sides together.
4. Each row shows the **Time** of the trade, the **Asset** and its pool, the **Maturity** of the pool (date and hour), the **Amount**, the **Yield**, what the seller received (for a bid: what the bid paid), the seller, the buyer (for a bid: the bidder), and a link to the transaction on Cardanoscan. Your own side reads *You*. Point at the link to see the fee of that transaction. A page holds 20 rows.
5. The page reads the trades again every 30 seconds while it is open, so a trade that settles shows up without a reload (HIST-08).
6. An ADA bid that was filled out shows its figure as *≤ X*. The tooltip explains why: the bid's change cannot be told apart on-chain, so the figure is the most the bid could have spent (HIST-06).

![The history of wallet 1, Sell orders, All (HIST-01)](screenshots/11-trade-history/HIST-01-W1-W2-sell-orders-history-all-of-the-wallet/w1-01-app-sell-orders-all.png)

![The history before SELL-01 (HIST-09)](screenshots/11-trade-history/HIST-09-W1-history-before-and-after-one-trade/01-app-buy-orders-before-sell-01.png)

![The history after SELL-01 (HIST-09)](screenshots/11-trade-history/HIST-09-W1-history-before-and-after-one-trade/02-app-buy-orders-after-sell-01.png)

---

## 11. A pool that has matured: cancel and redeem

1. In **My Account**, the PT of a matured pool carries the *redeemable* tag.
2. Click the **Redeem** icon on its row (tooltip *Redeem for the underlying token*). **Redeem …** opens and shows what you receive.
3. Click **Redeem** and sign in Eternl. Click **Close** to leave without redeeming.

If some of the PT is still listed for sale, the icon's tooltip reads *Redeem — the PT on sale is withdrawn in the same transaction*. The **Redeem** dialog then marks that PT *Withdrawn from your order in this transaction* (MAT-05). A redeem of PT ADA can pay out qAda, the form in which the pool holds its ADA (MAT-02). A bid on a matured pool can no longer fill: in **My bids** it carries the *matured* tag and offers only the *Cancel bid* icon. **Cancel Bid** then says *This market has matured, so the bid can no longer fill*; cancel it to get its money back. A matured pool is no longer in the **Token** list of *Place Bid* or *Create Sell Order*: it can no longer be bid on or listed (BLOCK-11, BLOCK-12).

![The Redeem dialog: the PT on sale is withdrawn in the same transaction (MAT-05)](screenshots/12-matured-pools-and-redeem/MAT-05-W1-redeem-PT-ADA-pool-A5-with-the-order-still-listed-tx-85eb6f9a/02-app-redeem-popup.png)

![Cancelling a bid on a matured pool (MAT-04)](screenshots/12-matured-pools-and-redeem/MAT-04-W1-cancel-BID-13-USDC-bid-on-a-matured-pool-B5-tx-42e6bb0b/02-app-cancel-bid-dialog.png)

---

## 12. Check your transaction on the explorer

The confirmation shows the transaction hash. Click it to open Cardanoscan, or paste it at https://preview.cardanoscan.io.

- The **Metadata** tab names the action. *Ask* is the market term for an offer to sell.

  | Action | Metadata |
  |---|---|
  | Create a sell order | *Bond DEX: Create Ask Order* |
  | Buy | *Bond DEX: Buy Ask Orders* |
  | Update an order | *Bond DEX: Update Ask Order* |
  | Cancel an order | *Bond DEX: Cancel Ask Order* |
  | Place a bid | *Bond DEX: Create Bid Order* |
  | Sell to bids | *Bond DEX: Sell To Bid Orders* |
  | Update a bid | *Bond DEX: Update Bid Order* |
  | Cancel a bid | *Bond DEX: Cancel Bid Order* |
  | Redeem | *Fixed-Rate Lending: Redeem Pool* |

- A **sell order** moves your PT to the order contract, an address that starts with `addr_test1z…`. The PT waits there for a buyer.
- A **buy** sends the PT to the buyer and pays the seller in the same transaction.

Your wallet keeps the same record: in Eternl, the transaction's outputs show the PT going to the order contract (*Plutus V3*).

![Eternl: the sell order's transaction details](screenshots/03-sell-orders-create/ASK-04-W1-sell-PT-USDC-30B-at-11pct-pool-A2-tx-78311866/07-eternl-transaction-details.png)

![A sell order on Cardanoscan: the PT sent to the order contract](screenshots/03-sell-orders-create/ASK-04-W1-sell-PT-USDC-30B-at-11pct-pool-A2-tx-78311866/08-cardanoscan-transaction.png)

![A buy on Cardanoscan: PT to the buyer, payment to the seller](screenshots/07-buy-market-orders/BUY-09-W1-whole-order-ASK-20-PT-DJED-150M-pool-B3-tx-55559488/08-cardanoscan-transaction.png)

---

## Good to know

- **Maturity.** On Preview a protocol day is 6 minutes and a year counts as 36.5 hours, so even a bond that matures tomorrow trades at a clear discount. Orders can be bought until maturity; after that, PT is redeemed in My Account rather than traded.
- **Fees.**
  - The buyer pays 0.2% of the price, shown as *Fee* before signing.
  - The seller pays 0.1%, already taken out of *Expected Receive*.
  - Every transaction also costs a small ADA network fee. Eternl shows it before you sign.
- **Script wallets** (multi-signature or smart-contract wallets) can buy but cannot create a sell order. The app tells you when this applies.
- **More than one order per transaction.** One buy or one sale to bids can take several orders or bids at once. BUY-01 took six sell orders; a sale to bids takes up to four bids (SELL-06).
- **Bids.** The bidder is the buyer: it pays 0.2% of the price when the bid fills, as the bid dialog shows. Every bid also holds 2 ADA beside it, which comes back when the bid closes.
- **Own orders.** A wallet cannot buy from its own sell order or sell to its own bid: clicking your own order opens *Update* instead.
