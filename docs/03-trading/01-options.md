# Options

> An option is a contract which conveys its owner the right, but not the obligation, to buy or sell an underlying asset at a specified strike price prior to a specified date.
>
> [https://en.wikipedia.org/wiki/Option\_\(finance\)](https://en.wikipedia.org/wiki/Option_%28finance%29)

An options contract is defined by a combination of parameters. As an example, someone may write 20  $2.00 strike MATIC/USDC Call contracts with an expiration of October 31, 2021, for $0.25 each. The following parameters define an option contract on Shrub \(example in parenthesis\):

Example Order: `Sell 20 $2.00 USDC strike MATIC Call options with expration of October 31, 2021 for $0.25 USDC each.`

* `baseAsset`: Asset on which `price` is based \(USDC\)
* `quoteAsset`: Underlying asset of the option and what is ultimately settled on exercise \(MATIC\)
* `optionType`: Either
  * CALL: Right to buy at the `strike` price \(CALL\)
  * PUT: Right to sell at the `strike` price
* `expiry`: Date after which the contract can no longer be exercised \(October 31, 2021 12:00p\)
* `strike`: Price in terms of the `baseAsset` for which either
  * CALL - The `quoteAsset` can be purchased \($2.00\)
  * PUT - The `quoteAsset` can be sold

