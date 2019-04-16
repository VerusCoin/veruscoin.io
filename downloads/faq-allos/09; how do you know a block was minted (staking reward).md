Question: How do you know a block was minted (staking reward)?

Answer: 
You can see the following characteristics:
1. a block hash without a lot of leading zeros
2. a last transaction that in your wallet has no fee, is from the same address that it is to, which is also the address the coinbase is to (easiest confirmation) and
3. The POS difficulty is encoded in the low 32 bits of the nonce with 96 of the next nonce bits as zero/reserved, then a random hash at the top half

(submitted by @keda666)
