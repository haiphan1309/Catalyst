# How orders are matched

On the Zero Coupon order book, matching happens on-chain when a trader takes the book: a **buy** is matched against the sell orders and **Sell to bids** against the bids, best price for the trader first, in one transaction.

- A buy takes the sell orders of one maturity, highest yield first. A sale to bids takes the bids of one maturity, lowest yield first.
- One transaction can take several orders or bids. A buy took six sell orders in one transaction (BUY-01). A sale to bids takes up to four bids in one transaction (SELL-06).
- What stays on a sell order after a partial buy must be at least the pool's minimum. If it would be less, the app lowers the buy so that exactly the minimum stays (BLOCK-04).
- What stays on a bid after a partial sale must also be at least the pool's minimum. If it would be less, the bid closes in the same transaction and the rest returns to the bidder (SELL-01, SELL-03).
- The buyer pays a fee of 0.2% of the price, the seller 0.1%.
- Nothing is matched after maturity. A matured pool is no longer in the Token list of *Place Bid* or *Create Sell Order* (BLOCK-11, BLOCK-12). A bid on it can only be cancelled (MAT-01, MAT-04), and its PT is redeemed. Redeeming PT that is still listed withdraws the sell order in the same transaction (MAT-05).

## Sell orders: the buyer takes the highest yield first

The Buy dialog matches the sell orders of the maturity from the highest yield down. BUY-03 shows it: the buy took ASK-03 (13%), then ASK-01 (12%), then part of ASK-02 (10%). The *Implied Yield* is the average over the orders matched.

- BUY-03: 550,000,000 PT ADA took ASK-03 (13%) and ASK-01 (12%) whole, then 100,000,000 of ASK-02 (10%).
- BUY-01: **Max** took all six DJED sell orders of pool A3 in one transaction, from 10.5% down to 5%: 450,000,000 PT, Implied Yield 9.33%.

If what would stay on an order is below the pool's minimum, the app lowers the buy. In BLOCK-04, wallet 2 typed 10,000 PT SNEK on ASK-14 (45,000 PT): the dialog matched 7,687 PT, so that 37,313, the minimum, stays on the order. The *Matched* line shows the amount that will be bought (PRICE-01: 10,000,000 PT matched on ASK-02, so that 90 ADA stays).

## Bids: the seller takes the lowest yield first

Sell to bids matches the bids of the maturity from the lowest yield up. In SELL-01, wallet 1 sold 349,999,999 PT ADA with **Max**: 222,534,612 PT went to BID-01 (15%) and 127,465,387 PT to BID-02 (18%), average yield 16.09%. The dialog showed *Receive* 311 ADA.

One sale takes up to four bids. In SELL-06, five bids waited on pool B3, at 15%, 16%, 17%, 18% and 19%. Selling 329,000,000 PT filled the four lowest bids out and left the 19% bid on the book. A buy is not limited to four: BUY-01 took six sell orders.

## Two orders at the same yield

When two orders have the same yield, the one placed earlier was filled first in both tests below.

- BUY-05: ASK-05 and ASK-06 are both at 9%. After the rest of ASK-04 (11%), the buy took ASK-05 (20,000,000,000 PT, placed before ASK-06) whole, then 5,000,000,000 of ASK-06.
- SELL-02: BID-03 and BID-04 are both 20,000,000,000 USDC units at 14%. The sale filled part of BID-03, placed first; BID-04 was not touched.

## When the rest of a bid is too small

If what would be left on a bid is below the pool's minimum, the bid closes in the same transaction and what is left returns to the bidder.

- SELL-01: after the sale, 88 ADA would have been left on BID-02, below the 90 ADA minimum. BID-02 closed and the 88 ADA returned to wallet 2 in the same transaction.
- SELL-03: wallet 1 sold 210,000,000 PT DJED to BID-05 (200 DJED) for about 187 DJED. What was left was below the 30 DJED minimum, so BID-05 closed.

In the history, a filled-out ADA bid shows what it paid as *≤ X* (HIST-06: *≤ 150 ADA* for BID-08 in SELL-05). The bid's change returns to the bidder in the same transaction and cannot be told apart on-chain, so the figure is the most the bid could have spent.

## Worked trades

| Trade | Wallet | Action | Matched | Why |
|---|---|---|---|---|
| BUY-01 | Wallet 2 | buys 450,000,000 PT DJED with Max, in one transaction | ASK-07 (10.5%, the relisted order), ASK-09 (9%), ASK-10 (8%), ASK-11 (7%), ASK-12 (6%), ASK-13 (5%), all whole | Highest yield first; Max takes every sell order of the maturity |
| BUY-02 | Wallet 2 | buys 10,000,000,000 PT USDC, part of ASK-04 at 11% | ASK-04 (11%) part | 20,000,000,000 PT (200 USDC) stays on ASK-04, above the 30 USDC minimum |
| BUY-03 | Wallet 2 | buys 550,000,000 PT ADA in one transaction: ASK-03 (13%) and ASK-01 (12%) whole, ASK-02 (10%) part | ASK-03 (13%) whole, ASK-01 (12%) whole, ASK-02 (10%) part | Highest yield first: 13%, 12%, then 10%; 100,000,000 PT stays on ASK-02, above the 90 ADA minimum |
| BUY-04 | Wallet 2 | buys 5,000 PT SNEK, part of ASK-14 at 12% | ASK-14 (12%) part | 40,000 PT stays on ASK-14, above the 37,313 SNEK minimum |
| BUY-05 | Wallet 2 | buys 45,000,000,000 PT USDC in one transaction: the remaining 20,000,000,000 of ASK-04 (11%), then 25,000,000,000 from the two 9% orders | rest of ASK-04 (11%), ASK-05 (9%) whole, ASK-06 (9%) part | 11% first, then the two 9% orders: ASK-05, placed earlier, before ASK-06 |
| BUY-06 | Wallet 2 | buys 90,000,000 PT ADA, the whole of ASK-15 (exactly the pool minimum) at 10% | ASK-15 (10%) whole | ASK-15 is exactly the 90 ADA minimum, so it can only be bought whole |
| BUY-07 | Wallet 1 | buys 250,000,000 PT ADA in one transaction: all of ASK-17 (11%) and all of ASK-18 (9%) | ASK-17 (11%) whole, ASK-18 (9%) whole | 11% first, then 9%; nothing is left on the book of pool B1 |
| BUY-08 | Wallet 1 | buys 5,000,000,000 PT USDC, part of ASK-19 at 10% | ASK-19 (10%) part | 10,000,000,000 PT (100 USDC) stays on ASK-19, above the 30 USDC minimum |
| BUY-09 | Wallet 1 | buys 150,000,000 PT DJED, the whole of ASK-20 at 11.5% | ASK-20 (11.5%) whole | The only sell order of pool B3, bought whole |
| BUY-10 | Wallet 1 | buys 10,000,000,000 PT USDC, the whole of ASK-22 (short pool B5) at 10% | ASK-22 (10%) whole | The only sell order of pool B5, bought whole |
| BUY-12 | Wallet 2 | buys the 5,000,000,000 PT USDC left on ASK-06 (9%) after BUY-05 | rest of ASK-06 (9%) | The 5,000,000,000 PT left on ASK-06 after BUY-05, bought whole |
| SELL-01 | Wallet 1 | sells all its free PT ADA of pool A1 (349,999,999) to the bids with Max | BID-01 (15%) whole: 222,534,612 PT; BID-02 (18%): 127,465,387 PT, then closed with 88 ADA returned | Lowest yield first; the 88 ADA left on BID-02 is below the 90 ADA minimum, so BID-02 closes |
| SELL-02 | Wallet 1 | sells 10,000,000,000 PT USDC on pool A2, where two bids tie at 14% | BID-03 (14%) part; BID-04 (14%) untouched | Same yield and size: the older bid first; 10,948,334,003 USDC units stay on BID-03 |
| SELL-03 | Wallet 1 | sells 210,000,000 PT DJED to BID-05 (16%) | BID-05 (16%) part, then closed | What was left of BID-05 is below the 30 DJED minimum, so the bid closes |
| SELL-04 | Wallet 1 | sells 40,000 PT SNEK to BID-06 (15%) | BID-06 (15%) part | 64,035 SNEK stays on BID-06, above the 37,313 SNEK minimum |
| SELL-05 | Wallet 2 | sells all its free PT ADA of pool B1 to the bids: BID-08 (14%) is filled out, BID-09 (16%) is part-filled | BID-08 (14%) whole: 153,765,415 PT for 150 ADA; BID-09 (16%) part: 96,234,584 PT for 93.52 ADA | Lowest yield first; 106 ADA stays on BID-09, above the 90 ADA minimum |
| SELL-06 | Wallet 2 | sells 329,000,000 PT DJED on pool B3, where five bids wait | BID-11 (15%): 205,343,880 PT for 200 DJED; BID-15 (16%), BID-16 (17%) and BID-17 (18%): 41,145,351, 41,221,925 and 41,288,844 PT for about 40 DJED each; all four filled out. BID-18 (19%) untouched | Lowest yield first; one sale takes up to four bids, so the 19% bid stays |
| SELL-07 | Wallet 2 | sells 10,000,000,000 PT USDC to BID-10 (15%) | BID-10 (15%) part | 5,258,878,523 USDC units (52.59 USDC) stay on BID-10, above the 30 USDC minimum |
| HIST-08 | Wallet 1 | sells 10,000,000,000 PT USDC of pool A2 to BID-04 (14%) | BID-04 (14%) part | 10,529,280,131 USDC units (105.29 USDC) stay on BID-04, above the 30 USDC minimum |
