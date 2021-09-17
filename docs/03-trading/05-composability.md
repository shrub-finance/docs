# Composability

When options are purchased on shrub the record of this remains stored within the shrub contract. In order to maintain compatibility and composability with other platforms, Shrub facilitates converting option positions to ERC-20 tokens. This will allow users to interact with other DeFi platforms with their Shrub options.

Both long and short option positions can be tokenized. The ShrubExchange contract will be a Contract Factory and there will be a method for creating an ERC-20 token contract for any long or short option position. Once the ERC-20 contract is created, option tokens can be minted by exchanging the options on the ShrubExchange contract for tokenized options on the ERC-20 contract. These tokens can then be burned in exchange for Shrub options or directly to exercise \(long\) or recover collateral \(short\).

There will be a specific ERC-20 contract for all of the option parameters including long or short:

* `baseAsset`
* `quoteAsset`
* `optionType`
* `expiry`
* `strike`
* `Long/Short` 

