# xDitto

xDITTO is a non-rebasing BEP20 token that is swappable for DITTO at a variable rate. It's purpose is to create an asset is tied to the market cap of DITTO, can be easily listed on CEXes, can be used in more yield farms and dapps, and expands DITTO's total reach and market cap. xDITTO is can only be created by locking DITTO meaning that it does not dilute DITTO's market cap.

Minti

Users lock DITTO in the xDITTO smart contract to mint xDITTO. This is done by calling the mint() function with the desired DITTO input amount. In return the user receives xDITTO at the current rate (note that xDITTO has 18 decimals while DITTO has 9).

E.g. approve(XD_ADDRESS, 10000000000000)
mint(XD_ADDRESS,10000000000000)

Redemption

Users can get DITTO by burning xDITTO using the burn function. `burn(amount)` burns `amount` xDITTO and returns DITTO according to the current exchange rate.

Exchange rate

The exchange rate adjusts dynamically as DITTO rebases. To get the DITTO returned for 1 xDITTO call:

`getRedeemAmount(1000000000000000000)`
