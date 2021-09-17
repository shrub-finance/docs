# Orders

An order is an offer to buy or sell a certain option contract for a certain price within a certain time window.

Example Order: `Sell 20 $2.00 USDC strike MATIC Call options with expration of October 31, 2021 for $0.25 USDC each (valid until September 15, 2021 3:00p)`

* `size`: Total number of option contracts to be bought or sold each representing the right to 1 of the `quoteAsset`. This can be fractional with a minimum precision of 1 millionth. \(20\)
* `isBuy`: Whether the order is an offer to BUY or SELL the options \(SELL\)
* `nonce`: parameter unique to an address/option combination. Must be 1 greater than the previous `nonce` for that user/option. Used to enforce the order of operations and allow canceling of orders
* `price`: price in terms of `baseAsset` per contract that an offer is made \($0.25\)
* `offerExpire`: date after which an order is no longer valid \(September 15, 2021 3:00p\)
* `fee`: fee in terms of the blockchain's gas token \(MATIC\) to be collected by the matcher for matching order. 

On the shrub platform a user who wishes to make an offer to buy or sell a particular number of options at a particular price combines an `Option` and an `Order`, signs it, and calls `OrderAnnounce` to emit this order to the blockchain as an event. As long as the `nonce` and `offerExpire` are valid, this order will be available to match.

