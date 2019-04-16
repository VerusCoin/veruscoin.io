
Question: How do I direct all my mined rewards to a single Verus wallet?

Answer:

IN AGAMA GUI
Step 1 - First get your wallet address you want to mine to:
- If you don't have an address, click "Receive", click "Get New Address" and choose "Transparent Address" from the drop down.
- Still u

Step 2 - Next we need to retrieve our pubkey,
- go to "settings" and click on "<CLI>". 
- In the <CLI> section, click on "Select Native Coin" for a dropdown list and select "VRSC native".
- Below "Type CLI compatible command", enter "validateaddress " and paste the address you copied.
- Click on "Execute"
- From the output find the long string after "pubkey", copy without the quotation marks.

Step 3 - Set your PubKey
- Go to 'Settings', 'App Config (config.json)' and enter your pubkey(THELONGSTRINGCOPIED) into the 'Pubkey VRSC mining key' field.
- Click 'Save app config' to save these settings.

IN VERUS-CLI
Step 1 - First get your wallet address you want to mine to:
You can find an address if you already have previous transactions, or you can create a new one.  To find an address from a previous transaction, use the command line verus listtransactions and copy the address found after "address".
To generate a new wallet address, use the command line verus "getnewaddress" and a new address will be created.

Step 2 - Next, using your new address, enter the command with verus-cli verus validateaddress. From the output find the long string after "pubkey", copy without the quotation marks.

Step 3 - Set your PubKey
Last, use this pubkey when starting your daemon by adding the following line to the end of your command, just before the "&" sign: -pubkey=THELONGSTRINGCOPIED

Your rewards will now be mined to that address.  It would be a good idea to keep notes and associate the wallet address with the pubkey...also to double check that you did validate the correct pubkey for the wallet address, making sure you made no errors.

(submitted by @J Oliver Westbrook, edited by @Oink)
