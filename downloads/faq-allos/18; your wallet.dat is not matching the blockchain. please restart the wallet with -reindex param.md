Question: ERROR: Your wallet.dat is not matching the blockchain. Please restart the wallet with -reindex param.

Answer: It seems you probably trying to move coinbase coins that you must move them through a private address (zaddress) first by shielding your coinbases, which is required by Verus blockchain rules.

To do this, you must:
1. go to the "Receive" screen and make a new private address
2. Copy the new private address to your clipboard
3. Go to the "Send" screen and select "Shield a coinbase"
4. Leave "Transparent funds" as the source and paste the new zaddress into the destination
5. Click on "Shield funds"
6. Wait a while until you have a private balance showing on the transactions screen
7. Send again, this time from your private address to any normal transparent receive address that you have.

(submitted by @keda666, solution written by mikeout)