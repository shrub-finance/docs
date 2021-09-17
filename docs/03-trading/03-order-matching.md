# Order Matching

If there are 2 orders in the order book for the same `Option` and with compatible prices \(the price per contract on the BUY order is at least the price per contract of the SELL order\), valid `nonce`, valid `offerExpire`, and each party has sufficient collateral then they can be matched.

Example Orders to be matched: 

`User A: Sell 20 $2.00 USDC strike MATIC Call options with expration of October 31, 2021 for $0.25 USDC each (valid until September 15, 2021 3:00p)`

`User B: Buy 10 $2.00 USDC strike MATIC Call options with expration of October 31, 2021 for $0.27 USDC each (valid until September 15, 2021 1:00p)`

Matching is the mechanism by which users are entered into a contract. When the match occurs, the `pricePerContract * size` is paid from the buyer to the seller in the `baseAsset` \(USDC\), and the seller's `quoteAsset` \(MATIC\) collateral is locked.

Matching can be done either as one of the users participating in a trade \(as a market order\) or by a third party who observes the compatible orders in the order book and performs the match to collect the `fee` that the orders included.

Effects of a match in the example:

* 10 contracts would be sold as this is the minimum of the sizes in the orders. 
* The price would be $0.26 as this is the average of the 2 offer `pricePerContract` 
* 10 MATIC would be locked from User A

#### Before

|  | User A | User B |
| :--- | :--- | :--- |
| USDC | 0 | 10 |
| MATIC unlocked | 20 | 0 |
| MATIC locked | 0 | 0 |

#### After

|  | User A | User B |
| :--- | :--- | :--- |
| USDC | 2.60 | 7.40 |
| MATIC unlocked | 10 | 0 |
| MATIC locked | 10 | 0 |

The asset that is locked \(MATIC\) is transferred to a pool of all of the locked `quoteAsset` for a particular contract and the seller will own a percentage of that pool based on the relative number of options that they sold. If the options are exercised, the exchange of funds will occur in the pool. The seller can reclaim funds from the pool once the contract has expired.

