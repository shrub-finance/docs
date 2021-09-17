# Exercising

Shrub options are _**American Style**_, which means that they may be exercised at any time.

To exercise options the user must either have sufficient funds to pay for the strike price of the option contracts or take a flash loan which the platform will offer.

### Call Options

To exercise, the exerciser will pay the strike price for each option contract that they wish to exercise to the option pool and will receive a corresponding amount of the `quoteAsset` in return \(1 per contract\).

For example:

`User A holds 50 $2 strike MATIC CALL options`

`Option Pool has issued 1000 of these options and holds 1000 locked MATIC` 

#### Before Exercise

|  | User A | Option Pool |
| :--- | :--- | :--- |
| MATIC | 0 | 1000 |
| USDC | 500 | 0 |

#### After Exercise

|  | User A | Option Pool |
| :--- | :--- | :--- |
| MATIC | 50 | 950 |
| USDC | 400 | 100 |

 

### Put Options

To exercise, the exerciser will exchange 1 of the `quoteAsset` per contract for the strike price

For Example:

`User B holds 50 $2 strike MATIC PUT options`

`Option Pool has issued 1000 of these options and holds 2000 locked USDC` 

#### Before Exercise

|  | User B | Option Pool |
| :--- | :--- | :--- |
| MATIC | 50 | 0 |
| USDC | 0 | 2000 |

#### After Exercise

|  | User B | Option Pool |
| :--- | :--- | :--- |
| MATIC | 0 | 50 |
| USDC | 100 | 1900 |

### 

### Flash Loans

If a user does not have sufficient funds to exercise an in-the-money option, they may borrow from the shrub pool via a flash loan to exercise options for a small fee of 0.3%. What is shown in the following examples all takes place in a single transaction.

#### Call Example

`User C holds 50 $1 strike MATIC CALL options but no USDC (market price of MATIC is $1.50)` 

* User C takes a flash loan of 50 USDC
* User C uses the USDC to exercise call options and receives 50 MATIC
* User C swaps 50 MATIC on QuickSwap for 75 USDC
* User C repays the flash loan with 50.15 USDC and is left with 24.85 USDC

#### Put Example

`User D holds 50 $2 strike MATIC Put options but no MATIC (market price of MATIC is $1.50)` 

* User D takes a flash loan of 50 MATIC
* User D uses the MATIC to exercise put options and receives 100 USDC
* User D swaps 100 USDC on QuickSwap for 66.67 MATIC
* User D repays the flash loan with 50.15 MATIC and is left with 16.52 MATIC

