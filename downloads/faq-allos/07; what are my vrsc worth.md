Question: What's the value of VRSC?

answer:
Use with: https://veruspay.io/api/ for simple USD VRSC price, or choose options now added!

Options (values are case insensitive): 
      currency - BTC or Fiat code like USD or CAD
      ticker - ARRR or VRSC
      data - volume or price - volume only relevant if exchange is defined
      exch - name of supported exchange, e.g. digitalprice - If no exchange, price is average of all supported for that coin.

If no options are set, the default is average price in USD fiat of VRSC.

Examples:

https://veruspay.io/api/ - This get's the current price of VRSC in USD, weighted against 24hr volume across all exchanges. This is the default return.
https://veruspay.io/api/?exch=digitalprice&currency=cad - This will get the current price on digital price for VRSC and display in CAD fiat
https://veruspay.io/api/?currency=btc - This will get the average price of VRSC in BTC, weighted by 24 hr volume across both exchanges
https://veruspay.io/api/?currency=cad - This gets the current average price of VRSC in CAD, weighted by 24 hr volume across both exchanges
https://veruspay.io/api/?exch=cryptobridge&data=volume - This will get the 24 volume of VRSC on CryptoBridge in the default currency of USD
https://veruspay.io/api/?exch=cryptobridge&data=volume&currency=btc - This does the same but with BTC as the currency result
https://veruspay.io/api/?currency=cad&ticker=arrr - Gets the average price of ARRR.

(submitted by @Godballz, API created by @J Oliver Westbrook)