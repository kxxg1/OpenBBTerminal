---
title: chains
description: Learn how to get the complete options chain for a ticker using the OBB.equity.options.chains
  function. Explore the available parameters like symbol and provider, and understand
  the data returned, including contract symbol, expiration, strike price, and more.
keywords: 
- options chain
- ticker
- complete options chain
- symbol
- provider
- data
- contract symbol
- expiration
- strike price
- option type
- eod date
- trading volume
- open price
- open interest
- high price
- low price
- implied volatility
- delta
- gamma
- theta
- vega
- bid size
- ask size
- theoretical value
- last trade price
- prev close
- change percent
- rho
- last trade timestamp
- dte
---

<!-- markdownlint-disable MD041 -->

Get the complete options chain for a ticker.

## Syntax

```jsx<span style={color: 'red'}>=OBB.DERIVATIVES.OPTIONS.CHAINS(symbol;[provider];[date])</span>```

### Example

```excel wordwrap
=OBB.DERIVATIVES.OPTIONS.CHAINS("AAPL")
```

---

## Parameters

| Name | Type | Description | Optional |
| ---- | ---- | ----------- | -------- |
| **symbol** | **Text** | **Symbol to get data for.** | **False** |
| provider | Text | Options: intrinio, defaults to intrinio. | True |
| date | Text | Date for which the options chains are returned. (provider: intrinio) | True |

---

## Return Data

| Name | Description |
| ---- | ----------- |
| contract_symbol | Contract symbol for the option.  |
| symbol | Symbol representing the entity requested in the data. Here its the underlying symbol for the option.  |
| expiration | Expiration date of the contract.  |
| strike | Strike price of the contract.  |
| option_type | Call or Put.  |
| eod_date | Date for which the options chains are returned.  |
| close | The close price.  |
| close_bid | The closing bid price for the option that day.  |
| close_ask | The closing ask price for the option that day.  |
| volume | The trading volume.  |
| open | The open price.  |
| open_bid | The opening bid price for the option that day.  |
| open_ask | The opening ask price for the option that day.  |
| open_interest | Open interest on the contract.  |
| high | The high price.  |
| low | The low price.  |
| mark | The mid-price between the latest bid-ask spread.  |
| ask_high | The highest ask price for the option that day.  |
| ask_low | The lowest ask price for the option that day.  |
| bid_high | The highest bid price for the option that day.  |
| bid_low | The lowest bid price for the option that day.  |
| implied_volatility | Implied volatility of the option.  |
| delta | Delta of the option.  |
| gamma | Gamma of the option.  |
| theta | Theta of the option.  |
| vega | Vega of the option.  |
| bid_size | Bid size for the option. (provider: cboe) |
| ask_size | Ask size for the option. (provider: cboe) |
| theoretical | Theoretical value of the option. (provider: cboe) |
| last_trade_price | Last trade price of the option. (provider: cboe) |
| tick | Whether the last tick was up or down in price. (provider: cboe) |
| prev_close | Previous closing price of the option. (provider: cboe) |
| change | Change in  price of the option. (provider: cboe) |
| change_percent | Change, in percent, of the option. (provider: cboe) |
| rho | Rho of the option. (provider: cboe) |
| last_trade_timestamp | Last trade timestamp of the option. (provider: cboe) |
| dte | Days to expiration for the option. (provider: cboe) |
