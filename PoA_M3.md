We are submitting the evidence for Milestone 3, *Implement Bond Dex and Price matching*. In the app the product is called **Zero Coupon**. It runs on the Cardano **Preview** testnet.

- Testnet app: https://app.zerocoupon.site
- Evidence folder: https://github.com/haiphan1309/Catalyst/tree/main/milestone-3
- Github Repo SC: https://github.com/haiphan1309/zero-coupon-aiken-contracts

A. Output: Testnet DEX page showing active open orders (order book).
Acceptance criteria: Users can view all active orders and execute matching trades on Cardano Testnet.
Evidence:
- Testnet URL: https://app.zerocoupon.site
- Screen recordings of the order book and of every trade in the test cases, from the first click to the confirmed transaction, with the Eternl signing window visible: https://github.com/haiphan1309/Catalyst/tree/main/milestone-3/videos
- Screenshots of each case: https://github.com/haiphan1309/Catalyst/tree/main/milestone-3/screenshots
- All recordings, screenshots and transactions were made by our team.
- The order book shows the bids in its *Buy order* column and the sell orders in its *Sell order* column.

B. Output: Price-matching functionality allowing trades to be executed.
Acceptance criteria: At least 10 successful trades executed and verified on-chain (with transaction hashes).
Evidence:
- 19 trades in the test cases, made from the app on 04 and 05 Nov 2026 with two Eternl wallets: 11 buys against sell orders and 8 sells to bids. The test wallets made two more buys, listed under Other transactions: 21 trades in all. Full table with the time, block, amounts and screenshots of each: https://github.com/haiphan1309/Catalyst/blob/main/milestone-3/TRANSACTIONS.md
- A buy takes the sell orders with the highest yield first. Sell to bids takes the bids with the lowest yield first. One transaction can take several orders: BUY-01 took six sell orders. A sale to bids takes up to four bids in one transaction (SELL-06). How the matching works, trade by trade: https://github.com/haiphan1309/Catalyst/blob/main/milestone-3/MATCHING.md
- The ten pools the trades are made on were prepared by our team before the test, five for each wallet: https://github.com/haiphan1309/Catalyst/blob/main/milestone-3/TRANSACTIONS.md#pools-prepared-before-the-test
- All trades carry the app's message under Cardano metadata label 674, "Bond DEX: Buy Ask Orders" or "Bond DEX: Sell To Bid Orders".
- Each trade spends the orders at the contract, and the chain accepted every one of these contract runs (valid_contract = true).
- In every trade paid in USDC, DJED or SNEK, the protocol fee address receives 0.2% of the price from the buyer and 0.1% from the seller, each rounded to the smallest unit.

Buys:
- BUY-01: wallet 2 buys 450,000,000 PT DJED with Max: one transaction fills six sell orders, ASK-07 and ASK-09 to ASK-13, all whole: https://preview.cardanoscan.io/transaction/216926e346ba0eca30b171b9a950bb0059e538e4534047708757d5b37727ab4f
- BUY-02: wallet 2 buys 10,000,000,000 PT USDC, part of ASK-04 at 11%: https://preview.cardanoscan.io/transaction/0e8008af55c2be2bc1dd81bf74eb05f14705b1d00cae2ea869216e6df5742c10
- BUY-03: wallet 2 buys 550,000,000 PT ADA in one transaction: ASK-03 (13%) and ASK-01 (12%) whole, ASK-02 (10%) part: https://preview.cardanoscan.io/transaction/1fd54c2f72176d30e4346d74d546113e66c527a9554131844a9eb441eef497d9
- BUY-04: wallet 2 buys 5,000 PT SNEK, part of ASK-14 at 12%: https://preview.cardanoscan.io/transaction/fd9fa7f1373d21bdb5bd4daadd729e8351918a50dfc1178d0268021053b9b285
- BUY-05: wallet 2 buys 45,000,000,000 PT USDC in one transaction: the remaining 20,000,000,000 of ASK-04 (11%), then 25,000,000,000 from the two 9% orders: https://preview.cardanoscan.io/transaction/4c9eb83ed00972ec568e3e451689151c292a910bbf71f08d44a8ce01d857125d
- BUY-06: wallet 2 buys 90,000,000 PT ADA, the whole of ASK-15 (exactly the pool minimum) at 10%: https://preview.cardanoscan.io/transaction/0fbabab2dd170cbfbe9e5325776d7cb90371e27f3ea53db0abf4a62196dd0c4f
- BUY-07: wallet 1 buys 250,000,000 PT ADA in one transaction: all of ASK-17 (11%) and all of ASK-18 (9%): https://preview.cardanoscan.io/transaction/d9efcf5341edfe23974d263c828031eec80f1cca7019155be06c65d77e7d2c1b
- BUY-08: wallet 1 buys 5,000,000,000 PT USDC, part of ASK-19 at 10%: https://preview.cardanoscan.io/transaction/22e90659128b455b5a39bea4b12935f2477c6b901685c01623bfa8ae293a7fde
- BUY-09: wallet 1 buys 150,000,000 PT DJED, the whole of ASK-20 at 11.5%: https://preview.cardanoscan.io/transaction/55559488fd8411a59a8f51e7c48d076d092fe3bbc2c0e2829bb38c20c973b1d1
- BUY-10: wallet 1 buys 10,000,000,000 PT USDC, the whole of ASK-22 (short pool B5) at 10%: https://preview.cardanoscan.io/transaction/310bfd683803b9563fc7e5b055d80bd11f3a462412a97dc8120e3eab7b70b074
- BUY-12: wallet 2 buys the last 5,000,000,000 PT USDC order left at 9% after BUY-05: https://preview.cardanoscan.io/transaction/7374c5352c167eff0e642d59888dc48d0ea3445e53eb888da80ee388fce7c65d

Sells to bids:
- SELL-01: wallet 1 sells all its free PT ADA of pool A1 to the bids with Max: BID-01 (15%) is filled out, then BID-02 (18%) takes the rest and closes, because the 88 ADA left is below the 90 ADA minimum: https://preview.cardanoscan.io/transaction/9b7d9969ac7c9ce0355b9f0e46c8d10cc4a723939f98a5318b1724e433208345
- SELL-02: wallet 1 sells 10,000,000,000 PT USDC on pool A2, where two bids tie at 14%: it fills part of BID-03, the older one: https://preview.cardanoscan.io/transaction/e5f1e14558400ec7be64b91ee0697e2cebf98d3a3e8a44b9ecd8c084d75bd85e
- SELL-03: wallet 1 sells 210,000,000 PT DJED to BID-05 (16%); the 12.49 DJED left is below the 30 DJED minimum, so BID-05 closes: https://preview.cardanoscan.io/transaction/fb2d538fe8222d7057bc1ea33dd53de3858f22ece4910622c3f07de3814d873d
- SELL-04: wallet 1 sells 40,000 PT SNEK to BID-06 (15%): https://preview.cardanoscan.io/transaction/62c8110159ae3df674bf0faed009ffa12463d8776284c609e841e78b4dd172cd
- SELL-05: wallet 2 sells all its free PT ADA of pool B1 to the bids with Max: BID-08 (14%) is filled out, BID-09 (16%) is part-filled: https://preview.cardanoscan.io/transaction/edf5844de27dc3f94e1e8fe1ffe3a95eefb7ae44b4db80a8afe2e2278a8ea78b
- SELL-06: wallet 2 sells 329,000,000 PT DJED on pool B3, where five bids wait: one transaction fills four of them out (15% to 18%), the 19% bid stays: https://preview.cardanoscan.io/transaction/91189258f70192761312bc18f6b17d70d096f88457a832f26ad31e10b16890c0
- SELL-07: wallet 2 sells 10,000,000,000 PT USDC to BID-10 (15%), part of the bid: https://preview.cardanoscan.io/transaction/61d3a50df9ec1c9ecc5df6cde6d5b468c33260cc44ab494da9b2c2eb6c978be4
- HIST-08: wallet 1 sells 10,000,000,000 PT USDC of pool A2 to BID-04 (14%), part of the bid, with its History page open in another tab: https://preview.cardanoscan.io/transaction/241211ad131aa4960fe1a81d39c4baf6d55c91c5a54203913bd49af7ac76a54b

C. Output: Trade history component showing executed trades with timestamps and maturity data.
Acceptance criteria: Trade history updates automatically based on on-chain data.
Evidence:
- The history lists the trades of the connected wallet, on both books, newest first. Its own side of each trade reads "You".
- Recording of the history page showing a new trade without a reload (HIST-08): the page reads the trades from on-chain data again every 30 seconds while it is open; wallet 1 sells to a bid in another tab, and when the History tab is shown again the new row appears within the next refresh (about 30 seconds), with its side reading "You": https://github.com/haiphan1309/Catalyst/tree/main/milestone-3/videos/11-trade-history
- Screenshots of the history before and after a trade (HIST-09): https://github.com/haiphan1309/Catalyst/tree/main/milestone-3/screenshots/11-trade-history/HIST-09-W1-history-before-and-after-one-trade
- Screenshots of the time and maturity (date and hour) of each trade of this milestone (HIST-05): https://github.com/haiphan1309/Catalyst/tree/main/milestone-3/screenshots/11-trade-history/HIST-05-W1-W2-time-and-maturity-of-each-fill
- All history screenshots: https://github.com/haiphan1309/Catalyst/tree/main/milestone-3/screenshots/11-trade-history
- Every row links to its transaction on Cardanoscan.

D. Output: Public user guide for matching and trade history.
Acceptance criteria: Public user guide enables community testers to replicate actions without developer support.
Evidence:
- User guide, with screenshots of the screens and dialogs it uses: https://github.com/haiphan1309/Catalyst/blob/main/milestone-3/USER_GUIDE.md
- The guide covers:
  - setting up Eternl on Preview, with test ADA and collateral;
  - connecting the wallet;
  - seeing the PT held;
  - creating, updating and cancelling a sell order;
  - buying a whole order or part of one;
  - placing, updating and cancelling a bid;
  - selling to bids;
  - reading the order book and how orders are matched;
  - the trade history;
  - a matured pool: cancelling a bid and redeeming;
  - checking each transaction on Cardanoscan.
- Two public test wallets, already holding PT and test tokens: https://github.com/haiphan1309/Catalyst/blob/main/milestone-3/TEST_WALLETS.md
- On Preview, a protocol day is 6 minutes and a year counts as 36.5 hours, so even a bond that matures tomorrow trades at a clear discount.
