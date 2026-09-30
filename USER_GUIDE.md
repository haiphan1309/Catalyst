# Zero Coupon — User Guide

**Create sell and buy orders for zero-coupon bonds on the Cardano Preview testnet.**

| | |
|---|---|
| App | https://app.zerocoupon.site |
| Network | Cardano **Preview** (testnet) |
| Wallet | Eternl |
| Explorer | https://preview.cardanoscan.io |

![The Market: the order book and the Trade panel](screenshots/01-app-overview/03-app-market-with-orders.png)

---

## What you are trading

- A **zero-coupon bond** pays nothing until it matures, then pays its full face value.
- On Zero Coupon the bond is a **Principal Token (PT)**. Each PT comes from a pool of one token (ADA, USDC, DJED or SNEK). At maturity, PT is redeemed for that token one for one.
- A **seller** lists PT at the yield they ask. They are paid as soon as someone buys.
- A **buyer** pays less than face value today and receives the full value at maturity. The difference is the buyer's yield.

**Amounts are counted in PT units.** One PT unit is worth one smallest unit of its token:

| PT | At maturity |
|---|---|
| PT ADA | 1,000,000 PT = 1 ADA |
| PT USDC | 100,000,000 PT = 1 USDC |
| PT DJED | 1,000,000 PT = 1 DJED |
| PT SNEK | 1 PT = 1 SNEK |

Under every amount you type, the app shows what it is worth in the token, for example *~ 100 ADA*.

---

## Before you start

1. **Eternl.** Install the Eternl browser extension (https://eternl.io), then create or restore a wallet.
2. **Preview network.** Switch Eternl to **Preview**. The app runs on Preview only.
3. **Test ADA.** Request test ADA for your Preview address from the Cardano testnet faucet: https://docs.cardano.org/cardano-testnets/tools/faucet
4. **Collateral.** Set up collateral in Eternl's settings. Buying, updating and cancelling an order run the order contract, and Cardano requires collateral for that.

With test ADA alone you can trade **PT ADA**, which is paid for in ADA.

**Shortcut:** restore one of the two public test wallets in [TEST_WALLETS.md](TEST_WALLETS.md). They already hold PT and test tokens, so you can skip the faucet.

---

## 1. Connect your wallet

1. Open https://app.zerocoupon.site. The **Preview** badge in the header shows the network.
2. Click **Connect Wallet** and choose **Eternl**.
3. If Eternl asks, approve the connection.

Your wallet now appears in the header.

![Connect Wallet: choose Eternl](screenshots/02-wallet-1-addr_test1qq5d0/02-connect-eternl-wallet/01-app-wallet-list.png)

![Connecting to Eternl](screenshots/02-wallet-1-addr_test1qq5d0/02-connect-eternl-wallet/02-app-connecting-eternl.png)

![Connected: the wallet in the header, on Preview](screenshots/02-wallet-1-addr_test1qq5d0/02-connect-eternl-wallet/03-app-connected.png)

---

## 2. See the PT in your wallet

Open **My Account**. It lists every PT your wallet holds, by token and maturity. The **Listed for sale** column shows how much of each PT is on sale.

![My Account: the PT this wallet holds](screenshots/02-wallet-1-addr_test1qq5d0/01-before-any-order/11-app-my-account.png)

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
   | **Number of PT to list for sale** | **Max** fills in all you hold. The amount must be at least the pool's minimum. If it is lower, the dialog tells you the minimum, for example *Minimum value to sell is 90 ADA*. |
   | **Effective Fixed APY for Buyer** | The yield you offer the buyer. |

   **Expected Receive (≈ now)** shows what you would receive if the order were bought right now, after the seller fee. Your order keeps the yield you set, so its price rises as maturity approaches.
3. Click **List** and sign in Eternl.
4. A progress window follows the transaction and ends with **Transaction confirmed**.

Your order is now in the Market order book under **Sell order**. **My Account** shows it under **Listed for sale**.

![Token: every PT in the wallet, with its maturity and balance](screenshots/02-wallet-1-addr_test1qq5d0/01-before-any-order/02-app-sell-dialog-all-pt.png)

![Below the pool's minimum, the dialog says so](screenshots/02-wallet-1-addr_test1qq5d0/03-create-sell-orders/S1-sell-PT-ADA-200M-at-12pct-tx-6a6a404c/01-app-below-minimum-error.png)

![Create Sell Order: amount, APY and Expected Receive](screenshots/02-wallet-1-addr_test1qq5d0/03-create-sell-orders/S1-sell-PT-ADA-200M-at-12pct-tx-6a6a404c/02-app-sell-dialog-filled.png)

![Sign in Eternl](screenshots/02-wallet-1-addr_test1qq5d0/03-create-sell-orders/S1-sell-PT-ADA-200M-at-12pct-tx-6a6a404c/03-eternl-sign-transaction.png)

![Transaction confirmed](screenshots/02-wallet-1-addr_test1qq5d0/03-create-sell-orders/S1-sell-PT-ADA-200M-at-12pct-tx-6a6a404c/04-app-transaction-confirmed.png)

![The order in the order book](screenshots/02-wallet-1-addr_test1qq5d0/03-create-sell-orders/S1-sell-PT-ADA-200M-at-12pct-tx-6a6a404c/05-app-order-on-market.png)

![My Account: the PT listed for sale](screenshots/02-wallet-1-addr_test1qq5d0/03-create-sell-orders/S1-sell-PT-ADA-200M-at-12pct-tx-6a6a404c/06-app-my-account-listed.png)

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

![Update is disabled until something changes](screenshots/02-wallet-1-addr_test1qq5d0/04-update-and-cancel-sell-orders/U1-update-PT-ADA-to-100M-at-9pct-tx-88022256/02-app-update-dialog-unchanged.png)

![Update Sell Order: a new APY](screenshots/02-wallet-1-addr_test1qq5d0/04-update-and-cancel-sell-orders/U2-update-PT-ADA-to-11pct-tx-dfd489a2/03-app-update-dialog-new-apy.png)

![Sign the update in Eternl](screenshots/02-wallet-1-addr_test1qq5d0/04-update-and-cancel-sell-orders/U2-update-PT-ADA-to-11pct-tx-dfd489a2/04-eternl-sign-transaction.png)

![The order at its new APY](screenshots/02-wallet-1-addr_test1qq5d0/04-update-and-cancel-sell-orders/U2-update-PT-ADA-to-11pct-tx-dfd489a2/06-app-my-account-new-apy.png)

![Cancel Sell Order: what returns to your wallet](screenshots/02-wallet-1-addr_test1qq5d0/04-update-and-cancel-sell-orders/C1-cancel-PT-ADA-100M-tx-b399a203/02-app-cancel-dialog.png)

![Sign the cancel in Eternl](screenshots/02-wallet-1-addr_test1qq5d0/04-update-and-cancel-sell-orders/C1-cancel-PT-ADA-100M-tx-b399a203/03-eternl-sign-transaction.png)

![The PT is back in the wallet, no longer listed](screenshots/02-wallet-1-addr_test1qq5d0/04-update-and-cancel-sell-orders/C1-cancel-PT-ADA-100M-tx-b399a203/05-app-my-account-pt-back.png)

---

## 5. Create a buy order

1. On **Market**, choose a token or **All**. Offers are grouped by maturity, with the highest yield first. The arrow under the maturity date shows every offer.
2. Click the **yield** of the sell order you want to buy from. **Buy PT** in the Trade panel opens the best offer.
3. Read **Market Order**:

   | Field | What it shows |
   |---|---|
   | **Number of PT tokens to buy** | Starts at the whole order. Enter less to buy part of it, as long as what stays on the order is at least the pool's minimum. **Max** is the most one transaction can buy. |
   | **ADA Receive Maturity** (named after the token) | What you receive at maturity, and the days until then. |
   | **Implied Yield** | Your yield if you hold to maturity. It is shown with the order(s) the buy is matched with. |
   | **Fee** | The buyer fee. |
   | **Pay** | The total you pay. |

4. Click **Buy** and sign in Eternl.
5. The progress window ends with **Transaction confirmed**.

After a whole-order buy the order leaves the book. After a partial buy, the book shows what is left. The PT you bought is in **My Account**.

On the Market your own orders open *Update*, not *Buy*. You cannot buy from yourself.

![The order book with every offer shown](screenshots/01-app-overview/04-app-market-with-orders-expanded.png)

![Market: click the yield of an order to buy from it](screenshots/03-wallet-2-addr_test1qz8r8/02-buy-orders/B1-buy-PT-ADA-200M-whole-order-tx-769fe7c5/01-app-market-before-buy.png)

![Market Order: buying a whole order](screenshots/03-wallet-2-addr_test1qz8r8/02-buy-orders/B1-buy-PT-ADA-200M-whole-order-tx-769fe7c5/02-app-buy-dialog-whole-order.png)

![Sign in Eternl](screenshots/03-wallet-2-addr_test1qz8r8/02-buy-orders/B1-buy-PT-ADA-200M-whole-order-tx-769fe7c5/03-eternl-sign-transaction.png)

![Transaction confirmed](screenshots/03-wallet-2-addr_test1qz8r8/02-buy-orders/B1-buy-PT-ADA-200M-whole-order-tx-769fe7c5/04-app-transaction-confirmed.png)

![The order has left the book](screenshots/03-wallet-2-addr_test1qz8r8/02-buy-orders/B1-buy-PT-ADA-200M-whole-order-tx-769fe7c5/05-app-market-after-buy.png)

![Market Order: buying part of an order](screenshots/03-wallet-2-addr_test1qz8r8/02-buy-orders/B2-buy-PT-USDC-4B-part-of-order-tx-b8e75629/02-app-buy-dialog-part-of-order.png)

![The rest of the order stays on the book](screenshots/03-wallet-2-addr_test1qz8r8/02-buy-orders/B2-buy-PT-USDC-4B-part-of-order-tx-b8e75629/05-app-market-after-buy.png)

![My Account: the PT bought](screenshots/03-wallet-2-addr_test1qz8r8/02-buy-orders/B1-buy-PT-ADA-200M-whole-order-tx-769fe7c5/06-app-my-account-bought-pt.png)

---

## 6. Check your transaction on the explorer

The confirmation shows the transaction hash. Click it to open Cardanoscan, or paste it at https://preview.cardanoscan.io.

- The **Metadata** tab names the action. *Ask* is the market term for an offer to sell.

  | Action | Metadata |
  |---|---|
  | Create a sell order | *Bond DEX: Create Ask Order* |
  | Buy | *Bond DEX: Buy Ask Orders* |
  | Update an order | *Bond DEX: Update Ask Order* |
  | Cancel an order | *Bond DEX: Cancel Ask Order* |

- A **sell order** moves your PT to the order contract, an address that starts with `addr_test1z…`. The PT waits there for a buyer.
- A **buy** sends the PT to the buyer and pays the seller in the same transaction.

Your wallet keeps the same record: in Eternl, the transaction's outputs show the PT going to the order contract (*Plutus V3*).

![Eternl: the sell order's transaction details](screenshots/02-wallet-1-addr_test1qq5d0/03-create-sell-orders/S1-sell-PT-ADA-200M-at-12pct-tx-6a6a404c/07-eternl-transaction-details.png)

![A sell order on Cardanoscan: the PT sent to the order contract](screenshots/02-wallet-1-addr_test1qq5d0/03-create-sell-orders/S1-sell-PT-ADA-200M-at-12pct-tx-6a6a404c/08-cardanoscan-transaction.png)

![A buy on Cardanoscan: PT to the buyer, payment to the seller](screenshots/03-wallet-2-addr_test1qz8r8/02-buy-orders/B1-buy-PT-ADA-200M-whole-order-tx-769fe7c5/08-cardanoscan-transaction.png)

---

## Good to know

- **Maturity.** On Preview, a pool's bonds mature one day after the pool is created, and a year counts as 36.5 hours, so even a one-day bond trades at a clear discount. Orders can be bought until maturity; after that, PT is redeemed in My Account rather than traded.
- **Fees.**
  - The buyer pays 0.2% of the price, shown as *Fee* before signing.
  - The seller pays 0.1%, already taken out of *Expected Receive*.
  - Every transaction also costs a small ADA network fee. Eternl shows it before you sign.
- **Script wallets** (multi-signature or smart-contract wallets) can buy but cannot create a sell order. The app tells you when this applies.
