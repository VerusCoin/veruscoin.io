Question: How does staking work?

Answer:
You'll start staking with the first VRSCs that are not time locked + in your public / transparent wallet + 150 blocks old (or about 2.5 hours).

Your chances to win a block: Your coins in your public/transparent wallet / Total staking supply in public/transparent wallets (which is max. about 485.000 VRSC from the first (sunrise) week as long as the rewards were below 192)

Remember: There will be only one reward every minute. It’s going to be either mining or staking, so on average 720 mining and 720 staking rewards every day. 

Example: I have 300 coins in a public/transparent address / 300.000 in public wallets (let's assume some part is lost/not staking or in private wallets), so that would be 1/1000 x 720 of a chance or around average 1,4 days for a staking block rewards. Hash power does not influence staking reward.

Regarding the Verus debug.log: “<DATE> No eligible staking transaction found“. It means that you are staking but have not received a reward yet. @miketout will change the message soon.

Regarding time locked coins:
The Zcash protocol requires you to send all coins received by mining (on wallet, not pool mining) or staking (reward transactions, also on wallet, not pool staking) once unlocked to a private address and then to a public/transparent address before you can use them either for staking or for making transactions (that’s how you make use of your rewarded coins = coinbase coins). So, once your coins loose their time lock, you can unlock those coins as described in "HOW-TO Shield Verus Coin via the CLI.md". Once you've transferred the coins from your private address back to (one of) your public / transparent address(es) and you’ll automatically start staking.

(submitted by @karero, edited by @Oink)
