# Natural Buyers/Sellers

The following use cases lend themselves to natural buying and selling of options:

## Buy Call

### Retail Bull

Investors looking to create a leveraged long position in an asset and creating more exposure with their capital that they could by owning the asset outright.

### Event-Driven Investor

With the thesis that an asset could either move significantly up in price or the price could collapse, an investor could make an asymmetric bet using out-of-the-money call options where the maximum downside is the capital spent on the options and a large potential upside.

## Buy Put

### Retail Bear

Purchasing a put is a straightforward way to make a time-based short bet on an asset. Unlike creating short positions via a borrowing platform there is no risk of a margin call, and the maximum loss is the capital deployed to buy the position

### Insurance

Users can use puts as a hedge - insurance against some amount of their assets going below a certain price.

### Lock in price for locked funds

If a user has assets that are locked either in a contract, agreement, or need to be held for longer for tax reasons and the price on the asset increases to a level where the user wishes to sell, they can lock in a price by purchasing a put with an expiration after the date their funds become unlocked. This allows them to remove the possibility of the value of their portfolio decreasing while they are locked while retaining any further upside.

### Uniswap V3 Insurance

For someone providing liquidity, puts can be purchased with a strike price at the bottom of the range to cap any losses at that amount

## Sell Call

### Limit Seller

Rather than placing a limit order to sell an asset, a call option can be sold which will also include the premium. When following this strategy the seller will either just collect the premium if the option expires below the strike price, or sell the asset for the price they were willing to anyway and also collect the premium

### Yield Seeker

By selling a covered call, holders of an asset can generate yield on their assets

## Sell Put

### Limit Buyer

A long-term bullish investor can "buy the dip" by selling an out-of-the-money put for a price that they would be willing to acquire the asset. The possible outcomes for this are acquiring the asset at a discount to the current market price or simply collecting the premium if the option expires worthless.

### Gaming Organizations

Tokens that have an underlying utility for gaming such as Smooth Love Potion \(SLP\) in Axie Infinity are strategically purchased by gaming organizations to further their interests in a game's ecosystem. For such strategies, selling puts would either result in obtaining the utility token at a discount to the current market price or collecting the premium and generating yield.

### Liquidation Hedge

Borrowers on DeFi platforms such as compound and Aave can hedge their positions by selling puts with a strike around the liquidation price of their collateral position on the borrowing platform. This limits potential losses if the price of the asset sinks below the liquidation price and generates yield in the form of the premium in the case that that asset price increases

